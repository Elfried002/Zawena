# Technology Stack — Zawena Platform

> Produit : Zawena Platform
>
> Document : Technology Stack
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
2. Philosophie technique
3. Frontend
4. Backend
5. Base de données
6. Authentification
7. Stockage
8. Intelligence Artificielle
9. Déploiement
10. Développement
11. Outils
12. Dépendances principales
13. Critères de sélection
14. Références

---

# 1. Objectif

Ce document décrit la stack technique officielle de Zawena Platform.

Il constitue la référence unique pour les technologies autorisées dans le projet.

Toute nouvelle technologie doit être validée avant son adoption.

---

# 2. Philosophie technique

Les choix techniques de Zawena reposent sur les principes suivants :

- simplicité ;
- maintenabilité ;
- évolutivité ;
- sécurité ;
- performance ;
- communauté active ;
- documentation de qualité.

La multiplication des technologies sans justification est à éviter.

---

# 3. Frontend

## Langage

- TypeScript

---

## Framework

- React 18+

---

## Build Tool

- Vite

---

## Styling

- Tailwind CSS

---

## UI Components

- shadcn/ui

---

## Icons

- Lucide React

---

## Routing

- React Router

---

## State Management

- TanStack Query (server state)
- React Context (global UI state)

---

## Forms

- React Hook Form
- Zod

---

# 4. Backend

## Backend-as-a-Service

- Supabase

---

## Runtime

- Edge Functions (Deno)

---

## API

- REST

---

## Validation

- Zod

---

# 5. Base de données

- PostgreSQL
- Supabase Database

---

# 6. Authentification

- Supabase Auth

Fonctionnalités :

- Email / Mot de passe
- Vérification Email
- Réinitialisation du mot de passe

Évolutions futures :

- OAuth
- MFA
- SSO

---

# 7. Stockage

- Supabase Storage

Utilisation :

- Images
- Documents
- Livrables
- Médias CMS

---

# 8. Intelligence Artificielle

Fournisseur principal :

- OpenAI

Architecture prévue pour permettre le remplacement ou l'ajout d'autres fournisseurs :

- Anthropic
- Google Gemini
- Mistral AI
- Azure OpenAI

---

# 9. Déploiement

Frontend :

- Vercel

Backend :

- Supabase

Versionnement :

- GitHub

CI/CD :

- GitHub Actions

---

# 10. Développement

Gestionnaire de paquets :

- npm

Qualité de code :

- ESLint
- Prettier

Documentation :

- Markdown

---

# 11. Outils

Outils utilisés par l'équipe :

- GitHub
- VS Code
- Lovable
- Opencode
- Supabase CLI
- Figma (Design)
- Excalidraw (Architecture)

---

# 12. Dépendances principales

Bibliothèques recommandées :

- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- React Router
- TanStack Query
- React Hook Form
- Zod
- Lucide React
- date-fns

Toute dépendance supplémentaire doit être justifiée.

---

# 13. Critères de sélection

Une technologie est retenue si elle répond à plusieurs des critères suivants :

- maintenue activement ;
- documentation complète ;
- communauté importante ;
- bonnes performances ;
- compatibilité avec la stack existante ;
- licence adaptée ;
- facilité d'intégration.

---

# 14. Références

- System Architecture
- API Architecture
- Deployment Architecture
- Coding Standards
- Folder Structure