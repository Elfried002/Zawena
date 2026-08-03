# API Architecture — Zawena Platform

> Produit : Zawena Platform
>
> Document : API Architecture
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
3. Principes de conception
4. Architecture API
5. Organisation des endpoints
6. Cycle de vie d'une requête
7. Authentification
8. Gestion des erreurs
9. Pagination
10. Filtrage et tri
11. Versionnement
12. Performance
13. Sécurité
14. Journalisation
15. Références

---

# 1. Objectif

Ce document décrit l'architecture des APIs de Zawena Platform.

Il définit :

- les principes de conception ;
- l'organisation des endpoints ;
- les conventions ;
- les formats d'échange ;
- les règles de sécurité ;
- les bonnes pratiques.

---

# 2. Vue d'ensemble

Zawena expose une API REST utilisée par :

- Website
- Dashboard
- Client Portal
- Intégrations
- Applications futures

Toutes les APIs suivent les mêmes conventions afin de garantir une expérience de développement cohérente.

---

# 3. Principes de conception

Les APIs respectent les principes suivants :

## RESTful

Les ressources sont représentées par des endpoints.

---

## Stateless

Chaque requête est indépendante.

---

## JSON

Toutes les données sont échangées au format JSON.

---

## API First

Les APIs constituent le contrat principal entre le frontend et le backend.

---

## Cohérence

Les conventions de nommage sont identiques dans tous les modules.

---

# 4. Architecture API

```
Frontend

↓

API Layer

↓

Business Logic

↓

Database

↓

Storage
```

Les APIs ne doivent jamais accéder directement à l'interface utilisateur.

Toute logique métier est implémentée dans la couche applicative.

---

# 5. Organisation des endpoints

## Authentication

```
/api/auth
```

Exemples :

```
POST   /login

POST   /logout

POST   /forgot-password

POST   /reset-password

GET    /profile
```

---

## CRM

```
/api/crm
```

```
GET    /leads

POST   /leads

PATCH  /leads/{id}

DELETE /leads/{id}
```

Même organisation pour :

- prospects
- companies
- contacts
- opportunities
- activities

---

## Quotes

```
/api/quotes
```

```
GET

POST

PATCH

DELETE
```

Endpoints spécifiques :

```
POST /quotes/{id}/send

POST /quotes/{id}/accept

POST /quotes/{id}/reject

POST /quotes/{id}/pdf
```

---

## Projects

```
/api/projects
```

Sous-ressources :

```
tasks

deliverables

documents

members

milestones

phases
```

---

## CMS

```
/api/cms
```

```
pages

blog

services

faq

media
```

---

## Notifications

```
/api/notifications
```

---

## Settings

```
/api/settings
```

---

# 6. Cycle de vie d'une requête

```
Client

↓

API

↓

Validation

↓

Authentification

↓

Autorisation

↓

Business Logic

↓

Database

↓

Réponse JSON
```

Toute requête suit ce processus.

---

# 7. Authentification

Les APIs protégées nécessitent :

- utilisateur authentifié ;
- session valide ;
- permissions suffisantes.

L'authentification est assurée par Supabase Auth.

Les détails sont documentés dans :

```
docs/architecture/auth.md
```

---

# 8. Gestion des erreurs

Les erreurs doivent être cohérentes.

Exemple :

```
200 OK

201 Created

204 No Content

400 Bad Request

401 Unauthorized

403 Forbidden

404 Not Found

409 Conflict

422 Unprocessable Entity

500 Internal Server Error
```

Le corps de réponse doit contenir :

```
{
  "success": false,
  "error": {
    "code": "...",
    "message": "...",
    "details": []
  }
}
```

---

# 9. Pagination

Les listes importantes utilisent une pagination.

Paramètres :

```
page

limit

sort

order
```

Réponse :

```
items

page

limit

total

totalPages
```

---

# 10. Filtrage et tri

Les endpoints doivent permettre :

```
?status=open

?search=client

?sort=created_at

?order=desc
```

Le comportement doit être identique sur tous les modules.

---

# 11. Versionnement

Toutes les APIs sont versionnées.

Format :

```
/api/v1/
```

Exemple :

```
/api/v1/crm/leads
```

Les évolutions incompatibles nécessitent une nouvelle version.

---

# 12. Performance

Les APIs doivent :

- limiter le volume de données retournées ;
- éviter les requêtes inutiles ;
- privilégier les traitements côté serveur ;
- utiliser des index adaptés.

Les réponses doivent respecter les exigences définies dans les Non-Functional Requirements.

---

# 13. Sécurité

Toutes les APIs appliquent :

- HTTPS ;
- validation des données ;
- contrôle des permissions ;
- protection contre les accès non autorisés ;
- journalisation des opérations critiques.

Les politiques RLS de Supabase complètent les contrôles applicatifs.

---

# 14. Journalisation

Les événements suivants doivent être enregistrés :

- erreurs ;
- authentifications ;
- appels critiques ;
- modifications importantes ;
- accès refusés.

Les journaux doivent permettre le diagnostic sans exposer d'informations sensibles.

---

# 15. Références

- System Architecture
- Modules Architecture
- Database Architecture
- Authentication Architecture
- Security Policy
- Functional Requirements
- Non-Functional Requirements
- Business Rules