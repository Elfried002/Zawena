# Modules Architecture — Zawena Platform

> Produit : Zawena Platform
>
> Document : Modules Architecture
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
3. Principes de modularité
4. Architecture des modules
5. Description des modules
6. Dépendances
7. Communication inter-modules
8. Événements métier
9. Règles d'architecture
10. Évolutivité
11. Références

---

# 1. Objectif

Ce document décrit l'organisation interne des modules de Zawena Platform.

Il définit :

- les responsabilités de chaque module ;
- leurs interactions ;
- leurs dépendances ;
- les événements échangés ;
- les limites de chaque domaine fonctionnel.

---

# 2. Vue d'ensemble

Zawena est organisé sous forme de modules indépendants.

Chaque module possède :

- son domaine métier ;
- ses composants ;
- ses services ;
- ses APIs ;
- ses modèles de données ;
- ses règles métier.

L'objectif est de limiter le couplage entre les domaines afin de faciliter l'évolution du produit.

---

# 3. Principes de modularité

L'architecture repose sur les principes suivants :

## Responsabilité unique

Chaque module traite un domaine métier spécifique.

---

## Faible couplage

Les modules communiquent via des APIs ou des événements.

---

## Forte cohésion

Les composants d'un même module sont fortement liés à leur domaine.

---

## Réutilisabilité

Les composants communs sont mutualisés lorsque cela est pertinent.

---

## Extensibilité

De nouveaux modules peuvent être ajoutés sans remettre en cause l'architecture existante.

---

# 4. Architecture des modules

```text
                       ZAWENA PLATFORM
                              │
 ┌────────────────────────────┼────────────────────────────┐
 │                            │                            │
 ▼                            ▼                            ▼
Website                 Authentication               Dashboard
 │                            │                            │
 └──────────────┬─────────────┴─────────────┬──────────────┘
                ▼                           ▼
              CRM                       Notifications
                │
                ▼
             Quotes
                │
                ▼
            Projects
                │
                ▼
          Client Portal
                │
                ▼
               CMS
                │
                ▼
            Settings
```

---

# 5. Description des modules

## Website

### Responsabilités

- Présentation de Zawena
- Services
- Blog
- FAQ
- Contact
- Demande de devis

### Dépendances

- CMS
- CRM

---

## Authentication

### Responsabilités

- Connexion
- Déconnexion
- Sessions
- Réinitialisation
- Vérification Email

### Dépendances

Aucune dépendance fonctionnelle.

Tous les autres modules utilisent ce service.

---

## Dashboard

### Responsabilités

- Vue d'ensemble
- KPIs
- Navigation
- Activités
- Recherche globale

### Dépendances

- CRM
- Projects
- Quotes
- Notifications

---

## CRM

### Responsabilités

- Leads
- Prospects
- Entreprises
- Contacts
- Opportunités
- Pipeline
- Activités

### Dépendances

- Quotes
- Notifications

---

## Quotes

### Responsabilités

- Création des devis
- PDF
- Validation
- Signature
- Historique

### Dépendances

- CRM
- Projects
- Notifications

---

## Projects

### Responsabilités

- Gestion des projets
- Phases
- Jalons
- Kanban
- Livrables
- Documents

### Dépendances

- Quotes
- Client Portal
- Notifications

---

## Client Portal

### Responsabilités

- Consultation
- Validation
- Téléchargements
- Suivi

### Dépendances

- Projects
- Authentication

---

## CMS

### Responsabilités

- Pages
- Blog
- FAQ
- Services
- SEO
- Médias

### Dépendances

- Website

---

## Notifications

### Responsabilités

- Emails
- Notifications In-App
- Historique
- Préférences

### Dépendances

Tous les modules peuvent produire des événements consommés par Notifications.

---

## Settings

### Responsabilités

- Organisation
- Utilisateurs
- Permissions
- Branding
- Intégrations
- Journaux d'audit

### Dépendances

- Authentication
- Notifications

---

# 6. Dépendances entre modules

| Module | Dépend de |
|---------|-----------|
| Website | CMS, CRM |
| Authentication | Aucun |
| Dashboard | CRM, Projects, Quotes, Notifications |
| CRM | Notifications |
| Quotes | CRM, Projects |
| Projects | Quotes, Notifications |
| Client Portal | Projects |
| CMS | Aucun |
| Notifications | Aucun (consomme des événements) |
| Settings | Authentication |

---

# 7. Communication inter-modules

Les modules communiquent principalement via :

## APIs REST

Pour les opérations synchrones.

Exemples :

- récupération d'un projet ;
- création d'un devis ;
- consultation d'un client.

---

## Événements métier

Pour les opérations asynchrones.

Exemples :

```
LeadCreated

↓

OpportunityWon

↓

QuoteAccepted

↓

ProjectCreated

↓

DeliverableValidated
```

---

## Base de données

Les modules partagent une base PostgreSQL.

Chaque module reste responsable de ses propres données.

Les relations inter-modules doivent être limitées et clairement documentées.

---

# 8. Événements métier

Les principaux événements échangés sont :

### CRM

- LeadCreated
- LeadQualified
- ProspectCreated
- OpportunityCreated
- OpportunityWon
- OpportunityLost

---

### Quotes

- QuoteCreated
- QuoteSent
- QuoteAccepted
- QuoteRejected

---

### Projects

- ProjectCreated
- TaskCreated
- TaskCompleted
- DeliverableUploaded
- DeliverableValidated
- ProjectCompleted

---

### Client Portal

- ClientLoggedIn
- DocumentDownloaded
- DeliverableReviewed

---

### CMS

- ContentCreated
- ContentPublished
- ContentArchived

---

### Notifications

- NotificationCreated
- NotificationSent
- NotificationRead

---

### Settings

- UserInvited
- RoleUpdated
- PermissionUpdated
- IntegrationConfigured

---

# 9. Règles d'architecture

Les modules doivent respecter les règles suivantes :

- un module ne doit pas accéder directement aux données internes d'un autre module ;
- les échanges doivent passer par des interfaces documentées ;
- les dépendances circulaires sont interdites ;
- les événements métier doivent être immuables ;
- chaque module doit rester testable indépendamment.

---

# 10. Évolutivité

L'architecture doit permettre d'ajouter de nouveaux modules sans modifier les modules existants.

Exemples de modules futurs :

- Billing
- Payments
- Marketplace
- AI Agents
- Analytics
- Mobile API

Ces modules devront respecter les mêmes principes de modularité.

---

# 11. Références

- System Architecture
- Database Architecture
- API Architecture
- Authentication Architecture
- Permissions Architecture
- Functional Requirements
- Business Rules
- User Flows