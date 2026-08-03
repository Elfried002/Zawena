# Naming Conventions — Zawena Platform

> Produit : Zawena Platform
>
> Document : Naming Conventions
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Engineering Team

---

# Table des matières

1. Objectif
2. Principes
3. Langue officielle
4. Conventions générales
5. Fichiers
6. Dossiers
7. Composants React
8. Hooks
9. Fonctions
10. Variables
11. Constantes
12. Types et Interfaces
13. Énumérations
14. Base de données
15. API
16. Git
17. Bonnes pratiques
18. Anti-patterns
19. Références

---

# 1. Objectif

Ce document définit les conventions de nommage utilisées dans tout le projet Zawena.

L'objectif est de garantir :

- un code lisible ;
- une nomenclature cohérente ;
- une maintenance facilitée ;
- une meilleure collaboration.

Toutes les nouvelles contributions doivent respecter ces conventions.

---

# 2. Principes

Les noms doivent être :

- explicites ;
- cohérents ;
- descriptifs ;
- prévisibles ;
- faciles à rechercher.

Éviter les abréviations inutiles.

---

# 3. Langue officielle

Toute la base de code est écrite en anglais.

Sont concernés :

- dossiers ;
- fichiers ;
- variables ;
- composants ;
- fonctions ;
- tables SQL ;
- APIs.

Les contenus destinés aux utilisateurs peuvent être traduits.

---

# 4. Conventions générales

| Élément | Convention |
|----------|------------|
| Dossiers | kebab-case |
| Fichiers | kebab-case |
| Composants React | PascalCase |
| Variables | camelCase |
| Fonctions | camelCase |
| Hooks | camelCase avec préfixe `use` |
| Types | PascalCase |
| Interfaces | PascalCase |
| Enums | PascalCase |
| Constantes | UPPER_SNAKE_CASE |
| Tables SQL | snake_case (pluriel) |
| Colonnes SQL | snake_case |
| Routes API | kebab-case |

---

# 5. Fichiers

Utiliser le **kebab-case**.

Exemples :

```text
project-card.tsx

client-profile.tsx

create-project-form.tsx

quote-service.ts

date-utils.ts
```

Ne jamais utiliser :

```text
ProjectCard.tsx

project_card.tsx

Project_Card.tsx
```

Les exceptions sont les fichiers qui exportent directement un composant React principal si l'équipe choisit cette convention. Si cette exception est retenue, elle doit être appliquée de manière uniforme.

---

# 6. Dossiers

Les dossiers utilisent également le **kebab-case**.

Exemples :

```text
project-management/

client-portal/

shared-components/

auth/
```

---

# 7. Composants React

Les composants utilisent le **PascalCase**.

Exemples :

```tsx
ProjectCard

ClientProfile

CreateProjectDialog

QuoteTable

NotificationCenter
```

Le nom du composant doit refléter sa responsabilité.

---

# 8. Hooks

Les hooks commencent toujours par `use`.

Exemples :

```tsx
useAuth

useProjects

useCurrentUser

useNotifications

useCreateQuote
```

Les hooks doivent représenter une responsabilité unique.

---

# 9. Fonctions

Les fonctions utilisent le **camelCase**.

Exemples :

```tsx
createProject()

updateQuote()

calculateTotal()

sendInvitation()

publishArticle()
```

Le nom doit commencer par un verbe.

---

# 10. Variables

Les variables utilisent également le **camelCase**.

Exemples :

```tsx
projectId

currentUser

quoteStatus

selectedClient

isLoading

hasPermission
```

Les booléens commencent de préférence par :

- is
- has
- can
- should

---

# 11. Constantes

Les constantes globales utilisent le **UPPER_SNAKE_CASE**.

Exemples :

```tsx
MAX_UPLOAD_SIZE

DEFAULT_PAGE_SIZE

API_TIMEOUT

SUPPORTED_LANGUAGES
```

---

# 12. Types et Interfaces

Utiliser le **PascalCase**.

Exemples :

```tsx
Project

Quote

Client

DashboardStats

Notification
```

Pour les interfaces, privilégier des noms descriptifs plutôt que des préfixes techniques.

---

# 13. Énumérations

Les enums utilisent le **PascalCase**.

Exemple :

```tsx
ProjectStatus

UserRole

QuoteStatus

NotificationType
```

Les valeurs d'enum doivent rester cohérentes dans tout le projet.

---

# 14. Base de données

Tables :

```text
projects

companies

users

notifications
```

Colonnes :

```text
created_at

updated_at

deleted_at

project_id

company_id
```

Clés primaires :

```text
id
```

Clés étrangères :

```text
project_id

user_id

company_id
```

---

# 15. API

Les routes API utilisent des noms explicites.

Exemples :

```text
/api/v1/projects

/api/v1/quotes

/api/v1/auth/login

/api/v1/cms/pages
```

Les verbes HTTP décrivent l'action.

---

# 16. Git

Branches :

```text
feature/project-management

feature/client-portal

fix/login

hotfix/email-validation

refactor/dashboard

docs/design-system
```

Commits (Conventional Commits) :

```text
feat:

fix:

docs:

refactor:

test:

style:

perf:

build:

ci:

chore:
```

---

# 17. Bonnes pratiques

✔ Utiliser des noms explicites.

✔ Garder la même convention partout.

✔ Préférer des noms métier plutôt que techniques.

✔ Utiliser des verbes pour les actions.

✔ Utiliser des noms au singulier pour les types et au pluriel pour les collections.

✔ Garder les noms courts mais suffisamment descriptifs.

---

# 18. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Abréviations obscures.

```text
usr

prj

cmp
```

---

✘ Variables d'une seule lettre (hors boucles simples).

---

✘ Mélanger plusieurs conventions.

---

✘ Noms ambigus.

```text
data

temp

value

object
```

---

✘ Utiliser des noms différents pour le même concept selon les modules.

---

# 19. Références

- Technology Stack
- Folder Structure
- Coding Standards
- Git Workflow
- API Architecture
- Database Architecture