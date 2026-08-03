# Git Workflow — Zawena Platform

> Produit : Zawena Platform
>
> Document : Git Workflow
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
3. Stratégie de branches
4. Cycle de développement
5. Pull Requests
6. Convention de commits
7. Gestion des versions
8. Résolution des conflits
9. Branch Protection
10. Bonnes pratiques
11. Anti-patterns
12. Références

---

# 1. Objectif

Ce document définit le workflow Git officiel de Zawena Platform.

Il garantit :

- une collaboration efficace ;
- un historique clair ;
- une meilleure qualité du code ;
- des déploiements fiables.

---

# 2. Principes

Le workflow repose sur :

- une branche principale stable ;
- des branches courtes ;
- des Pull Requests obligatoires ;
- des revues de code ;
- une intégration continue.

Aucun développement ne doit être effectué directement sur la branche principale.

---

# 3. Stratégie de branches

## main

Branche de production.

Elle doit toujours être stable.

---

## develop (optionnelle)

Si le projet grandit, cette branche peut être utilisée comme branche d'intégration.

Pour le MVP, elle n'est pas obligatoire.

---

## feature/*

Création de nouvelles fonctionnalités.

Exemples :

```text
feature/crm-dashboard

feature/project-kanban

feature/client-portal

feature/ai-assistant
```

---

## fix/*

Correction de bugs.

Exemples :

```text
fix/login

fix/email-validation

fix/notification-center
```

---

## hotfix/*

Corrections urgentes en production.

Exemples :

```text
hotfix/auth

hotfix/security-patch
```

---

## refactor/*

Amélioration du code sans modification fonctionnelle.

Exemples :

```text
refactor/project-service

refactor/navigation
```

---

## docs/*

Documentation.

Exemples :

```text
docs/api

docs/design-system

docs/security
```

---

# 4. Cycle de développement

Le cycle recommandé est :

```text
Créer une branche

↓

Développer

↓

Tester

↓

Commit

↓

Push

↓

Pull Request

↓

Code Review

↓

Validation CI

↓

Merge

↓

Déploiement
```

Les branches doivent être supprimées après leur fusion.

---

# 5. Pull Requests

Chaque Pull Request doit :

- avoir un titre explicite ;
- décrire les changements ;
- référencer les User Stories concernées ;
- indiquer les impacts éventuels ;
- passer les tests automatiques.

Une Pull Request ne doit pas être fusionnée sans validation.

---

# 6. Convention de commits

Le projet utilise **Conventional Commits**.

Types autorisés :

```text
feat:

fix:

refactor:

docs:

test:

style:

perf:

build:

ci:

chore:
```

Exemples :

```text
feat(crm): add lead qualification workflow

fix(auth): prevent session expiration issue

docs(api): update authentication endpoints

refactor(projects): simplify task service

test(quotes): add acceptance tests
```

Chaque commit doit représenter une seule intention.

---

# 7. Gestion des versions

Le projet suit **Semantic Versioning**.

Format :

```text
MAJOR.MINOR.PATCH
```

Exemples :

```text
1.0.0

1.1.0

1.1.1
```

- **MAJOR** : changement incompatible.
- **MINOR** : nouvelle fonctionnalité compatible.
- **PATCH** : correction de bug.

---

# 8. Résolution des conflits

Les conflits doivent être résolus :

- dans la branche concernée ;
- avant la fusion ;
- après mise à jour avec la branche principale.

Chaque résolution doit être testée.

---

# 9. Branch Protection

La branche `main` doit être protégée.

Règles recommandées :

- interdiction des push directs ;
- Pull Request obligatoire ;
- revue de code obligatoire ;
- pipeline CI validée ;
- historique linéaire lorsque possible.

---

# 10. Bonnes pratiques

✔ Créer une branche par fonctionnalité.

✔ Faire des commits fréquents.

✔ Écrire des messages de commit explicites.

✔ Maintenir des Pull Requests de taille raisonnable.

✔ Fusionner régulièrement avec la branche principale.

✔ Supprimer les branches fusionnées.

---

# 11. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Développer directement sur `main`.

✘ Commits du type :

```text
update

fix

test

final

misc
```

✘ Pull Requests trop volumineuses.

✘ Mélanger plusieurs fonctionnalités dans une même branche.

✘ Fusionner du code non testé.

---

# 12. Références

- Coding Standards
- Naming Conventions
- Testing Strategy
- Deployment Architecture
- Opencode Rules