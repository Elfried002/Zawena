# Authentication Architecture — Zawena Platform

> Produit : Zawena Platform
>
> Document : Authentication Architecture
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Software Architecture Team

---

# Table des matières

1. Objectif
2. Vue d'ensemble
3. Principes
4. Architecture
5. Cycle d'authentification
6. Gestion des sessions
7. Gestion des utilisateurs
8. Vérification Email
9. Réinitialisation du mot de passe
10. Gestion des rôles
11. Sécurité
12. Journalisation
13. Évolutions futures
14. Références

---

# 1. Objectif

Ce document décrit l'architecture du système d'authentification de Zawena Platform.

Il définit :

- les mécanismes d'authentification ;
- la gestion des sessions ;
- la gestion des comptes ;
- les flux de sécurité ;
- les responsabilités des différents composants.

---

# 2. Vue d'ensemble

Zawena utilise **Supabase Auth** comme fournisseur principal d'identité.

Le système permet :

- connexion sécurisée ;
- déconnexion ;
- récupération du mot de passe ;
- vérification de l'adresse email ;
- gestion des profils utilisateurs ;
- gestion des rôles applicatifs.

L'autorisation (permissions) est documentée séparément dans **permissions.md**.

---

# 3. Principes

Le système repose sur les principes suivants :

## Authentification centralisée

Tous les utilisateurs passent par Supabase Auth.

---

## Séparation des responsabilités

- Authentification → Supabase Auth
- Autorisation → Application
- Permissions → RBAC
- Profils → Base PostgreSQL

---

## Session sécurisée

Les sessions sont contrôlées automatiquement.

---

## Principe du moindre privilège

Chaque utilisateur dispose uniquement des droits nécessaires.

---

# 4. Architecture

```
Utilisateur

↓

Frontend

↓

Supabase Auth

↓

JWT Session

↓

API

↓

Permissions

↓

Modules

↓

Base PostgreSQL
```

---

# 5. Cycle d'authentification

```
Connexion

↓

Validation

↓

Supabase Auth

↓

JWT

↓

Session

↓

Chargement du profil

↓

Chargement des permissions

↓

Dashboard
```

---

# 6. Gestion des sessions

Chaque utilisateur possède une session authentifiée.

La session comprend notamment :

- identifiant utilisateur ;
- rôle principal ;
- organisation ;
- date de création ;
- date d'expiration.

Les sessions expirées doivent être invalidées automatiquement.

---

# 7. Gestion des utilisateurs

Chaque utilisateur possède :

- un identifiant unique (UUID) ;
- une adresse email unique ;
- un profil ;
- un rôle principal ;
- un statut.

Statuts possibles :

- Invité
- Actif
- Suspendu
- Désactivé

---

# 8. Vérification Email

Les nouveaux comptes doivent vérifier leur adresse email avant d'accéder aux fonctionnalités protégées.

Flux :

```
Invitation

↓

Email

↓

Lien sécurisé

↓

Validation

↓

Compte actif
```

---

# 9. Réinitialisation du mot de passe

Le système permet la récupération du mot de passe.

Flux :

```
Demande

↓

Email sécurisé

↓

Lien temporaire

↓

Nouveau mot de passe

↓

Connexion
```

Les liens de réinitialisation possèdent une durée de validité limitée.

---

# 10. Gestion des rôles

L'authentification identifie l'utilisateur.

Les permissions sont ensuite calculées à partir de son rôle.

Exemples de rôles :

- Super Administrator
- Administrator
- Sales
- Project Manager
- Developer
- Support
- Client

Les règles RBAC sont documentées dans :

```
docs/architecture/permissions.md
```

---

# 11. Sécurité

Le système applique notamment :

- HTTPS obligatoire ;
- JWT sécurisés ;
- expiration des sessions ;
- validation des tokens ;
- contrôle des accès ;
- protection contre les attaques par force brute (selon les capacités du fournisseur d'identité) ;
- journalisation des connexions.

Les mots de passe ne sont jamais stockés par l'application.

---

# 12. Journalisation

Les événements suivants doivent être enregistrés :

- connexion ;
- déconnexion ;
- échec de connexion ;
- réinitialisation du mot de passe ;
- changement d'adresse email ;
- activation du compte ;
- suspension d'un utilisateur.

Les journaux d'authentification doivent être protégés contre les modifications.

---

# 13. Évolutions futures

Les évolutions suivantes sont prévues :

- Authentification multifacteur (MFA)
- Single Sign-On (SSO)
- OAuth (Google, Microsoft, GitHub)
- Gestion avancée des appareils
- Sessions simultanées contrôlées
- Authentification sans mot de passe (Passwordless)

Ces fonctionnalités ne font pas partie du MVP.

---

# 14. Références

- System Architecture
- Modules Architecture
- API Architecture
- Permissions Architecture
- Security Policy
- Functional Requirements
- Non-Functional Requirements
- Business Rules