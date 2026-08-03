# ADR-004 — Authentication Architecture

> ADR ID : ADR-004
>
> Titre : Authentication Architecture
>
> Statut : Accepted
>
> Date : 03 Août 2026
>
> Décideurs : Founder, Engineering Team
>
> Type : Security & Architecture Decision

---

# Table des matières

1. Statut
2. Contexte
3. Problématique
4. Facteurs de décision
5. Options étudiées
6. Décision
7. Justification
8. Conséquences
9. Compromis (Trade-offs)
10. Évolutions futures
11. Révision
12. Documents associés

---

# 1. Statut

**Accepted**

Cette décision définit le système officiel d'authentification et de gestion des identités de Zawena Platform.

---

# 2. Contexte

Zawena est une plateforme SaaS multi-tenant manipulant des données sensibles.

L'authentification doit garantir :

- une sécurité élevée ;
- une expérience utilisateur fluide ;
- une intégration native avec la base de données ;
- une gestion des rôles et des permissions ;
- une évolutivité compatible avec les futures fonctionnalités.

Le système doit également limiter la quantité de code de sécurité développé en interne.

---

# 3. Problématique

Quelle solution d'authentification permet d'assurer un niveau de sécurité élevé tout en accélérant le développement et en restant cohérente avec la stack technique de Zawena ?

---

# 4. Facteurs de décision

Les critères retenus sont :

- sécurité ;
- simplicité d'intégration ;
- prise en charge des standards modernes ;
- compatibilité avec PostgreSQL ;
- gestion des rôles ;
- gestion des sessions ;
- évolutivité ;
- coût d'exploitation ;
- maintenance.

---

# 5. Options étudiées

## Supabase Auth

### Avantages

- intégration native avec Supabase ;
- gestion sécurisée des sessions ;
- support OAuth ;
- authentification par e-mail ;
- récupération de mot de passe ;
- MFA disponible ;
- intégration avec Row Level Security.

### Inconvénients

- dépendance à l'écosystème Supabase.

---

## Auth0

### Avantages

- extrêmement complet ;
- nombreuses fonctionnalités avancées.

### Inconvénients

- coût plus élevé ;
- intégration supplémentaire.

---

## Firebase Authentication

### Avantages

- mature ;
- nombreuses méthodes d'authentification.

### Inconvénients

- dépendance à Firebase ;
- moins cohérent avec PostgreSQL.

---

## Authentification développée en interne

### Avantages

- contrôle total.

### Inconvénients

- risques de sécurité élevés ;
- temps de développement important ;
- maintenance complexe.

---

# 6. Décision

Zawena adopte **Supabase Auth** comme solution officielle d'authentification.

Les principes retenus sont :

- authentification basée sur JWT ;
- gestion sécurisée des sessions ;
- Row Level Security (RLS) pour contrôler l'accès aux données ;
- rôles applicatifs gérés par la plateforme ;
- principe du moindre privilège.

Les informations sensibles (mots de passe, jetons, secrets) ne sont jamais stockées en clair.

---

# 7. Justification

## Sécurité

Supabase Auth fournit des mécanismes éprouvés de gestion des identités et réduit les risques liés à une implémentation maison.

---

## Intégration

La solution s'intègre nativement avec :

- PostgreSQL ;
- Row Level Security ;
- Edge Functions ;
- API Supabase.

---

## Productivité

Les fonctionnalités essentielles sont disponibles immédiatement :

- création de compte ;
- connexion ;
- réinitialisation du mot de passe ;
- gestion des sessions ;
- vérification des e-mails.

---

## Évolutivité

L'architecture permet d'ajouter progressivement :

- OAuth (Google, Microsoft, GitHub, etc.) ;
- authentification multifacteur (MFA) ;
- SSO pour les clients Enterprise.

---

# 8. Conséquences

## Positives

- réduction du temps de développement ;
- sécurité renforcée ;
- cohérence avec la stack technique ;
- maintenance simplifiée ;
- intégration native avec les politiques RLS.

---

## Négatives

- dépendance à Supabase Auth ;
- certaines fonctionnalités avancées nécessitent les offres supérieures de Supabase.

---

# 9. Compromis (Trade-offs)

Les principaux compromis sont :

- privilégier une solution managée plutôt qu'un développement spécifique ;
- accepter une dépendance maîtrisée afin de bénéficier d'une meilleure sécurité et d'une maintenance réduite.

Ce compromis est considéré comme acceptable au regard des objectifs du projet.

---

# 10. Évolutions futures

Les évolutions possibles comprennent notamment :

- authentification multifacteur (MFA) obligatoire pour certains rôles ;
- Single Sign-On (SSO) ;
- authentification sans mot de passe (Passkeys / WebAuthn) ;
- politiques adaptatives selon le niveau de risque ;
- gestion avancée des organisations et des équipes.

Toute évolution majeure devra être documentée dans un nouvel ADR.

---

# 11. Révision

Cette décision est revue :

- lors d'une évolution majeure des besoins de sécurité ;
- avant toute migration du système d'identité ;
- au minimum une fois par an.

---

# 12. Documents associés

- Authentication Architecture
- Access Control Policy
- Security Policy
- Identity Management
- Privacy Policy
- ADR-002 Technology Stack
- ADR-003 Database Architecture