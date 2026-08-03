# Coding Standards — Zawena Platform

> Produit : Zawena Platform
>
> Document : Coding Standards
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
3. Standards généraux
4. TypeScript
5. React
6. Architecture
7. Gestion des erreurs
8. Performance
9. Sécurité
10. Documentation
11. Qualité du code
12. Revue de code
13. Bonnes pratiques
14. Anti-patterns
15. Références

---

# 1. Objectif

Ce document définit les standards de développement utilisés dans Zawena Platform.

L'objectif est de produire un code :

- lisible ;
- maintenable ;
- sécurisé ;
- performant ;
- cohérent.

Tous les développeurs doivent respecter ces règles.

---

# 2. Principes

Le développement repose sur les principes suivants :

- simplicité ;
- lisibilité ;
- modularité ;
- réutilisabilité ;
- testabilité ;
- sécurité.

Chaque décision de développement doit privilégier la maintenabilité à long terme.

---

# 3. Standards généraux

Le code doit être :

- formaté automatiquement ;
- linté avant chaque commit ;
- entièrement typé ;
- documenté lorsque nécessaire.

Chaque fichier doit avoir une responsabilité unique.

Les fonctions doivent rester courtes et faciles à comprendre.

---

# 4. TypeScript

TypeScript est obligatoire.

## Règles

✔ Utiliser des types explicites lorsque cela améliore la compréhension.

✔ Préférer les interfaces ou types adaptés au contexte.

✔ Éviter `any`.

✔ Préférer `unknown` lorsqu'un type est inconnu.

✔ Activer le mode strict.

✔ Utiliser les utilitaires TypeScript (`Partial`, `Pick`, `Omit`, `Record`, etc.) lorsque cela simplifie le code.

---

# 5. React

Les composants doivent être :

- fonctionnels ;
- réutilisables ;
- composables.

## Hooks

Respecter les Rules of Hooks.

Les hooks personnalisés doivent encapsuler la logique réutilisable.

---

## State

Utiliser :

- React Context pour l'état global léger ;
- TanStack Query pour les données serveur ;
- l'état local lorsque suffisant.

Éviter la duplication d'état.

---

## Props

Les composants doivent recevoir uniquement les props nécessaires.

Éviter le "prop drilling" lorsque des solutions plus adaptées existent.

---

# 6. Architecture

Le code doit respecter l'architecture modulaire définie dans :

```
docs/architecture/modules.md
```

Chaque module doit rester indépendant.

La logique métier ne doit jamais être placée dans les composants UI.

Les services doivent encapsuler les accès aux APIs et aux fournisseurs externes.

---

# 7. Gestion des erreurs

Les erreurs doivent être :

- capturées ;
- journalisées ;
- compréhensibles.

Ne jamais afficher directement des erreurs techniques aux utilisateurs.

Les exceptions doivent être traitées au niveau approprié.

---

# 8. Performance

Les développeurs doivent :

- éviter les re-rendus inutiles ;
- optimiser les listes volumineuses ;
- charger les ressources à la demande lorsque pertinent ;
- utiliser le cache de TanStack Query pour les données serveur.

L'optimisation prématurée est à éviter ; elle doit être guidée par des mesures.

---

# 9. Sécurité

Le code doit respecter les règles suivantes :

- validation côté client et côté serveur ;
- contrôle des permissions avant toute action sensible ;
- aucune information sensible dans le code source ;
- utilisation des variables d'environnement pour les secrets ;
- protection contre les injections et les entrées invalides.

Les règles détaillées sont définies dans le dossier `docs/security/`.

---

# 10. Documentation

Le code doit être suffisamment explicite pour limiter les commentaires.

Les commentaires sont réservés :

- aux décisions complexes ;
- aux contraintes techniques ;
- aux cas particuliers.

La documentation technique doit être mise à jour en même temps que le code.

---

# 11. Qualité du code

Le projet applique :

- ESLint ;
- Prettier ;
- TypeScript Strict Mode.

Avant chaque fusion, le code doit :

- compiler sans erreur ;
- passer les tests ;
- respecter les règles de linting.

---

# 12. Revue de code

Chaque Pull Request doit être revue avant sa fusion.

La revue vérifie notamment :

- lisibilité ;
- respect des standards ;
- architecture ;
- sécurité ;
- performances ;
- tests.

Les remarques doivent être constructives et documentées.

---

# 13. Bonnes pratiques

✔ Écrire un code simple.

✔ Préférer la composition à l'héritage.

✔ Éviter la duplication.

✔ Utiliser des noms explicites.

✔ Écrire des fonctions courtes.

✔ Séparer clairement la logique métier de l'interface.

✔ Supprimer le code inutilisé.

✔ Maintenir les dépendances à jour.

---

# 14. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Utiliser `any` sans justification.

✘ Dupliquer la logique métier.

✘ Fonctions trop longues.

✘ Composants gigantesques.

✘ Commentaires décrivant un code évident.

✘ Ignorer les erreurs retournées par les APIs.

✘ Mélanger logique métier, accès aux données et interface dans un même composant.

---

# 15. Références

- Technology Stack
- Folder Structure
- Naming Conventions
- Testing Strategy
- Security Policy
- Modules Architecture