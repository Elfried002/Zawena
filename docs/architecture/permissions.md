# Permissions Architecture — Zawena Platform

> Produit : Zawena Platform
>
> Document : Permissions Architecture
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
3. Modèle d'autorisation
4. Architecture RBAC
5. Rôles
6. Ressources
7. Permissions
8. Cycle d'autorisation
9. Hiérarchie des rôles
10. Sécurité
11. Audit
12. Évolutions futures
13. Références

---

# 1. Objectif

Ce document décrit le système d'autorisation de Zawena Platform.

Il définit :

- les rôles ;
- les permissions ;
- les ressources protégées ;
- les politiques d'accès ;
- les mécanismes de contrôle.

L'objectif est de garantir que chaque utilisateur accède uniquement aux ressources qui lui sont autorisées.

---

# 2. Vue d'ensemble

Zawena utilise un modèle RBAC (Role-Based Access Control).

Le système repose sur trois concepts principaux :

- Utilisateur
- Rôle
- Permission

Chaque utilisateur possède un rôle principal.

Chaque rôle possède un ensemble de permissions.

Les permissions déterminent les actions autorisées sur les ressources de la plateforme.

---

# 3. Modèle d'autorisation

```
Utilisateur

↓

Rôle

↓

Permissions

↓

Ressources

↓

Action autorisée
```

Les permissions sont évaluées avant chaque opération protégée.

---

# 4. Architecture RBAC

```
users

↓

roles

↓

role_permissions

↓

permissions

↓

resources
```

Chaque rôle peut posséder plusieurs permissions.

Une permission peut être attribuée à plusieurs rôles.

---

# 5. Rôles

Les rôles du MVP sont :

## Super Administrator

Responsabilités :

- administration complète ;
- gestion des organisations ;
- gestion des utilisateurs ;
- configuration globale.

---

## Administrator

Responsabilités :

- gestion quotidienne ;
- CRM ;
- projets ;
- CMS ;
- utilisateurs.

---

## Sales

Responsabilités :

- CRM ;
- Leads ;
- Opportunités ;
- Devis.

---

## Project Manager

Responsabilités :

- gestion des projets ;
- livrables ;
- équipes ;
- planning.

---

## Developer

Responsabilités :

- tâches ;
- livrables ;
- documents techniques.

---

## Support

Responsabilités :

- assistance client ;
- suivi des tickets ;
- consultation limitée.

---

## Client

Responsabilités :

- consultation ;
- validation des livrables ;
- téléchargement des documents.

---

# 6. Ressources

Les ressources protégées comprennent :

- Dashboard
- CRM
- Leads
- Prospects
- Companies
- Contacts
- Opportunities
- Quotes
- Projects
- Tasks
- Deliverables
- Documents
- CMS
- Notifications
- Settings
- Users
- Roles
- Integrations

---

# 7. Permissions

Les permissions suivent le format :

```
resource.action
```

Exemples :

```
crm.read

crm.create

crm.update

crm.delete

projects.read

projects.update

quotes.send

quotes.accept

users.invite

users.disable

settings.update

cms.publish
```

Les actions disponibles sont :

- read
- create
- update
- delete
- approve
- validate
- publish
- archive
- invite
- assign
- export
- configure

---

# 8. Cycle d'autorisation

```
Utilisateur connecté

↓

Session valide

↓

Chargement du rôle

↓

Chargement des permissions

↓

Vérification de la permission

↓

Autorisation

↓

Exécution

↓

Journalisation
```

Si la permission est absente :

↓

403 Forbidden

---

# 9. Hiérarchie des rôles

```
Super Administrator

↓

Administrator

↓

Project Manager

↓

Sales

↓

Developer

↓

Support

↓

Client
```

Le rôle supérieur n'hérite pas automatiquement des permissions du rôle inférieur.

Les permissions sont attribuées explicitement afin d'éviter les privilèges involontaires.

---

# 10. Sécurité

Le système applique les principes suivants :

- moindre privilège ;
- vérification côté serveur ;
- contrôle sur chaque requête protégée ;
- validation des permissions avant toute modification ;
- aucune permission implicite.

Les politiques RLS de Supabase complètent les contrôles applicatifs.

---

# 11. Audit

Les événements suivants doivent être journalisés :

- création d'un rôle ;
- modification d'un rôle ;
- suppression d'un rôle ;
- changement de permissions ;
- accès refusés ;
- élévation de privilèges.

Les journaux d'audit doivent être consultables uniquement par les administrateurs autorisés.

---

# 12. Évolutions futures

Les évolutions prévues comprennent :

- rôles personnalisés ;
- permissions dynamiques ;
- groupes d'utilisateurs ;
- délégation temporaire de permissions ;
- contrôle d'accès basé sur les attributs (ABAC) ;
- permissions multi-organisations.

Ces fonctionnalités sont prévues après le MVP.

---

# 13. Références

- System Architecture
- Modules Architecture
- Authentication Architecture
- Database Architecture
- API Architecture
- Security Policy
- Business Rules
- Functional Requirements