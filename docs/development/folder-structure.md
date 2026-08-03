# Folder Structure — Zawena Platform

> Produit : Zawena Platform
>
> Document : Folder Structure
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
3. Organisation générale
4. Structure du projet
5. Description des dossiers
6. Organisation par module
7. Gestion des ressources
8. Organisation des tests
9. Conventions
10. Bonnes pratiques
11. Anti-patterns
12. Références

---

# 1. Objectif

Ce document définit l'organisation officielle du code source de Zawena Platform.

Une structure uniforme permet :

- une meilleure lisibilité ;
- une maintenance facilitée ;
- une montée en compétence plus rapide des développeurs ;
- une meilleure évolutivité.

Toute nouvelle fonctionnalité doit respecter cette structure.

---

# 2. Principes

L'organisation du projet repose sur les principes suivants :

- séparation des responsabilités ;
- modularité ;
- faible couplage ;
- forte cohésion ;
- réutilisabilité ;
- simplicité.

Les fichiers doivent être faciles à localiser.

---

# 3. Organisation générale

L'application est organisée autour de trois grandes catégories :

```text
Application

↓

Shared

↓

Infrastructure
```

Chaque catégorie possède une responsabilité clairement définie.

---

# 4. Structure du projet

```text
src/

├── app/
│   ├── routes/
│   ├── providers/
│   ├── layouts/
│   └── config/
│
├── modules/
│   ├── authentication/
│   ├── dashboard/
│   ├── crm/
│   ├── quotes/
│   ├── projects/
│   ├── cms/
│   ├── notifications/
│   └── settings/
│
├── components/
│   ├── ui/
│   ├── common/
│   ├── layout/
│   └── navigation/
│
├── hooks/
│
├── services/
│
├── lib/
│
├── utils/
│
├── types/
│
├── assets/
│
├── styles/
│
└── main.tsx
```

---

# 5. Description des dossiers

## app/

Contient :

- routes ;
- providers ;
- layouts ;
- configuration globale.

---

## modules/

Contient toute la logique métier.

Chaque module est indépendant.

Exemple :

```text
crm/

projects/

quotes/

cms/
```

---

## components/

Composants réutilisables.

Sous-dossiers :

```text
ui/

common/

layout/

navigation/
```

---

## hooks/

Hooks React personnalisés.

Exemple :

```text
useAuth()

useProjects()

useNotifications()
```

---

## services/

Services métier.

Exemples :

- API
- IA
- Email
- Storage

---

## lib/

Bibliothèques internes.

Exemples :

- client Supabase ;
- helpers ;
- configuration.

---

## utils/

Fonctions utilitaires.

Elles ne doivent contenir aucune logique métier.

---

## types/

Types TypeScript partagés.

---

## assets/

Images

Icônes

Illustrations

Polices

---

## styles/

Configuration Tailwind

Styles globaux

Variables CSS

---

# 6. Organisation par module

Chaque module suit la même structure.

Exemple :

```text
projects/

components/

pages/

hooks/

services/

types/

schemas/

utils/
```

Cette organisation est identique pour tous les modules.

---

# 7. Gestion des ressources

Les ressources doivent être organisées par type.

```text
assets/

images/

icons/

illustrations/

fonts/
```

Les fichiers inutilisés doivent être supprimés.

---

# 8. Organisation des tests

Les tests sont placés au plus près du code testé.

Exemple :

```text
ProjectCard.tsx

ProjectCard.test.tsx
```

Les tests d'intégration peuvent être regroupés dans un dossier dédié.

---

# 9. Conventions

Les règles suivantes s'appliquent :

- un dossier = une responsabilité ;
- éviter les dossiers fourre-tout ;
- limiter la profondeur de l'arborescence ;
- privilégier les imports explicites ;
- mutualiser les composants partagés.

---

# 10. Bonnes pratiques

✔ Organiser le projet par domaine métier.

✔ Garder les modules indépendants.

✔ Réutiliser les composants communs.

✔ Centraliser la configuration.

✔ Séparer clairement la logique métier de l'interface.

✔ Maintenir une structure identique entre les modules.

---

# 11. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Dossiers contenant des responsabilités multiples.

✘ Composants réutilisables placés dans un module spécifique.

✘ Fonctions utilitaires contenant de la logique métier.

✘ Imports circulaires.

✘ Structures différentes selon les modules.

✘ Arborescence excessivement profonde.

---

# 12. Références

- Technology Stack
- Modules Architecture
- Coding Standards
- Naming Conventions
- Opencode Rules