# Database Architecture — Zawena Platform

> Produit : Zawena Platform
>
> Document : Database Architecture
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
3. Technologies
4. Principes de conception
5. Organisation des données
6. Entités principales
7. Relations entre les entités
8. Conventions de nommage
9. Clés et contraintes
10. Intégrité des données
11. Indexation
12. Suppression des données
13. Audit
14. Sécurité
15. Sauvegarde
16. Évolutivité
17. Références

---

# 1. Objectif

Ce document décrit l'architecture de la base de données de Zawena Platform.

Il définit :

- les principes de modélisation ;
- les conventions de conception ;
- les entités métier ;
- les relations ;
- les contraintes ;
- les politiques de sécurité ;
- les stratégies d'évolution.

Il constitue la référence principale pour toute évolution du schéma PostgreSQL.

---

# 2. Vue d'ensemble

Zawena utilise **PostgreSQL** via **Supabase** comme base de données relationnelle principale.

Les objectifs sont :

- garantir l'intégrité des données ;
- assurer des performances élevées ;
- faciliter les évolutions ;
- permettre une forte traçabilité ;
- simplifier la maintenance.

---

# 3. Technologies

## Base de données

- PostgreSQL

## Plateforme

- Supabase

## ORM (si utilisé)

- À définir (Drizzle ORM ou Prisma selon les décisions d'architecture)

## Migrations

- SQL versionné
- Supabase CLI

---

# 4. Principes de conception

La base de données respecte les principes suivants :

## Normalisation

Les données doivent être normalisées afin de limiter les duplications.

---

## Intégrité référentielle

Toutes les relations utilisent des clés étrangères lorsque cela est pertinent.

---

## Faible couplage

Chaque module reste responsable de ses propres tables.

---

## Auditabilité

Les opérations importantes doivent être historisées.

---

## Évolutivité

Le modèle doit permettre l'ajout de nouveaux modules sans refonte majeure.

---

# 5. Organisation des données

Les données sont organisées par domaine métier.

```
Authentication

CRM

Quotes

Projects

Client Portal

CMS

Notifications

Settings
```

Chaque domaine possède son propre ensemble de tables.

---

# 6. Entités principales

## Authentication

- users
- sessions
- user_profiles

---

## CRM

- leads
- prospects
- companies
- contacts
- opportunities
- activities
- notes

---

## Quotes

- quotes
- quote_items

---

## Projects

- projects
- project_members
- project_phases
- milestones
- tasks
- subtasks
- deliverables
- project_documents

---

## Client Portal

- client_accounts
- client_notifications

---

## CMS

- pages
- blog_posts
- services
- faq
- case_studies
- media_library

---

## Notifications

- notifications
- notification_preferences

---

## Settings

- organizations
- roles
- permissions
- integrations
- audit_logs

---

# 7. Relations entre les entités

## CRM

```
Company

↓

Contacts

↓

Opportunities

↓

Quotes
```

---

## Quotes

```
Quote

↓

Quote Items
```

---

## Projects

```
Project

↓

Phases

↓

Milestones

↓

Tasks

↓

Subtasks
```

---

## Client Portal

```
Client

↓

Projects

↓

Deliverables
```

---

# 8. Conventions de nommage

## Tables

- snake_case
- pluriel

Exemples

```
users

companies

project_members

quote_items
```

---

## Colonnes

snake_case

Exemple

```
first_name

created_at

updated_at

deleted_at
```

---

## Clés primaires

Toutes les tables utilisent :

```
id UUID
```

---

## Clés étrangères

Nommage :

```
company_id

project_id

quote_id

user_id
```

---

# 9. Clés et contraintes

Chaque table doit disposer de :

- clé primaire ;
- contraintes NOT NULL lorsque nécessaire ;
- clés étrangères ;
- contraintes UNIQUE lorsque requis ;
- valeurs par défaut adaptées.

Exemples :

- email unique ;
- numéro de devis unique ;
- slug unique.

---

# 10. Intégrité des données

Les règles suivantes s'appliquent :

- aucune donnée orpheline ;
- suppression contrôlée ;
- validation des références ;
- cohérence des statuts métier.

Les transactions critiques doivent être atomiques.

---

# 11. Indexation

Des index doivent être créés sur les colonnes fréquemment utilisées.

Exemples :

```
email

status

created_at

company_id

project_id

quote_id
```

Les index doivent être documentés lors de la création des tables.

---

# 12. Suppression des données

Par défaut :

Soft Delete.

Colonnes utilisées :

```
deleted_at

deleted_by
```

La suppression physique est réservée :

- aux données temporaires ;
- aux opérations d'administration ;
- aux procédures de maintenance.

---

# 13. Audit

Les opérations suivantes doivent être historisées :

- création ;
- modification ;
- suppression logique ;
- changement de permissions ;
- changements critiques.

Les journaux d'audit doivent inclure :

- utilisateur ;
- date ;
- action ;
- ancien état ;
- nouvel état.

---

# 14. Sécurité

Les données sont protégées par :

- Row Level Security (RLS) ;
- politiques d'accès ;
- authentification Supabase ;
- rôles applicatifs ;
- chiffrement des communications.

Les données sensibles ne doivent jamais être exposées aux utilisateurs non autorisés.

---

# 15. Sauvegarde

Les sauvegardes doivent être :

- automatiques ;
- régulières ;
- testées ;
- documentées.

Une procédure de restauration doit être disponible.

---

# 16. Évolutivité

Le modèle doit permettre :

- l'ajout de nouveaux modules ;
- l'ajout de nouvelles tables ;
- l'ajout de nouveaux champs ;
- les migrations sans interruption majeure ;
- le support futur du multi-tenant.

Toute évolution doit être réalisée via une migration versionnée.

---

# 17. Références

- System Architecture
- Modules Architecture
- API Architecture
- Authentication Architecture
- Security Policy
- Functional Requirements
- Business Rules
- Development Standards