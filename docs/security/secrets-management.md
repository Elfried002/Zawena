# Secrets Management — Zawena Platform

> Produit : Zawena Platform
>
> Document : Secrets Management
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Security Team

---

# Table des matières

1. Objectif
2. Principes
3. Classification des secrets
4. Stockage
5. Variables d'environnement
6. Rotation des secrets
7. Accès aux secrets
8. Gestion des incidents
9. Audit
10. Security Controls
11. Bonnes pratiques
12. Anti-patterns
13. Références

---

# 1. Objectif

Ce document définit les règles de gestion des secrets de Zawena Platform.

Les objectifs sont :

- protéger les informations sensibles ;
- limiter les risques de fuite ;
- garantir une rotation contrôlée ;
- assurer la traçabilité des accès.

---

# 2. Principes

La gestion des secrets repose sur :

- Least Privilege
- Need-to-Know
- Zero Trust
- Rotation régulière
- Séparation des environnements

Les secrets ne doivent jamais être considérés comme permanents.

---

# 3. Classification des secrets

Les principaux secrets utilisés par Zawena sont :

## Niveau Critique

- Supabase Service Role Key
- Clés OpenAI
- Clés Anthropic
- Clés SMTP
- Clés Stripe
- Clés Paystack
- Jetons d'administration

---

## Niveau Élevé

- Variables internes
- Secrets CI/CD
- Tokens GitHub

---

## Niveau Standard

- Clés publiques
- Configuration non sensible

---

# 4. Stockage

Les secrets doivent être stockés uniquement dans des systèmes sécurisés.

Exemples :

- Variables d'environnement Vercel
- Secrets GitHub Actions
- Configuration sécurisée Supabase

Les secrets ne doivent jamais être stockés :

- dans Git ;
- dans le code source ;
- dans la documentation ;
- dans des captures d'écran.

---

# 5. Variables d'environnement

Les variables sont séparées par environnement.

## Development

Variables de développement uniquement.

---

## Staging

Variables dédiées aux tests.

---

## Production

Variables de production.

Les valeurs de production ne doivent jamais être réutilisées en développement.

---

# 6. Rotation des secrets

Les secrets doivent pouvoir être renouvelés.

La rotation est réalisée :

- après un incident ;
- lors d'une suspicion de fuite ;
- selon une politique définie par l'organisation.

Après chaque rotation :

- vérifier le fonctionnement ;
- invalider les anciennes valeurs ;
- documenter l'opération.

---

# 7. Accès aux secrets

L'accès est limité aux personnes autorisées.

Chaque accès doit être :

- justifié ;
- journalisé lorsque possible ;
- révoqué lorsqu'il n'est plus nécessaire.

Les comptes partagés sont interdits.

---

# 8. Gestion des incidents

En cas de compromission :

1. Identifier le secret concerné.
2. Révoquer immédiatement le secret.
3. Générer une nouvelle valeur.
4. Mettre à jour les services concernés.
5. Vérifier les journaux.
6. Documenter l'incident.

---

# 9. Audit

Des audits réguliers doivent vérifier :

- les secrets inutilisés ;
- les secrets expirés ;
- les permissions ;
- les configurations des environnements.

---

# 10. Security Controls

## SEC-SM-001

Contrôle :

Aucun secret dans le dépôt Git.

Priorité :

Critique

Implémentation :

GitHub Secret Scanning

---

## SEC-SM-002

Contrôle :

Séparation des secrets par environnement.

Priorité :

Critique

Implémentation :

Vercel + GitHub + Supabase

---

## SEC-SM-003

Contrôle :

Rotation des secrets.

Priorité :

Élevée

Implémentation :

Politique interne

---

## SEC-SM-004

Contrôle :

Journalisation des accès sensibles.

Priorité :

Élevée

Implémentation :

Audit Logs

---

## SEC-SM-005

Contrôle :

Révocation immédiate après compromission.

Priorité :

Critique

Implémentation :

Runbook Incident Response

---

# 11. Bonnes pratiques

✔ Utiliser des variables d'environnement.

✔ Limiter les accès.

✔ Documenter les rotations.

✔ Révoquer rapidement les secrets compromis.

✔ Séparer les environnements.

✔ Utiliser des outils de détection de secrets.

---

# 12. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Stocker une clé API dans le code.

✘ Envoyer des secrets par messagerie non sécurisée.

✘ Réutiliser les mêmes secrets entre plusieurs environnements.

✘ Partager des comptes administrateurs.

✘ Publier des captures d'écran contenant des secrets.

✘ Utiliser des secrets expirés.

---

# 13. Références

- Security Policy
- Access Control
- Secure Development
- Incident Response
- Deployment Strategy
- OWASP Secrets Management Cheat Sheet