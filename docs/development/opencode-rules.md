# AI Development Rules (Opencode Rules) — Zawena Platform

> Produit : Zawena Platform
>
> Document : AI Development Rules
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
2. Vision
3. Agents IA concernés
4. Principes généraux
5. Règles de génération de code
6. Règles d'architecture
7. Règles React
8. Règles TypeScript
9. Règles Supabase
10. Règles UI
11. Règles de sécurité
12. Documentation
13. Tests
14. Workflow IA
15. Interdictions
16. Checklist
17. Références

---

# 1. Objectif

Ce document définit les règles que doivent respecter tous les assistants IA intervenant sur Zawena Platform.

Il garantit :

- cohérence ;
- qualité ;
- maintenabilité ;
- sécurité ;
- conformité avec l'architecture officielle.

Toute génération de code doit respecter ce document.

---

# 2. Vision

Les assistants IA sont considérés comme des collaborateurs techniques.

Ils assistent les développeurs mais ne remplacent jamais :

- les décisions d'architecture ;
- les validations métier ;
- les revues de code ;
- les validations de sécurité.

L'humain reste responsable du code produit.

---

# 3. Agents IA concernés

Ces règles s'appliquent notamment à :

- Lovable
- Opencode
- ChatGPT
- Claude Code
- GitHub Copilot
- Cursor
- Windsurf
- Gemini CLI
- tout autre agent de génération de code

---

# 4. Principes généraux

Avant toute génération de code, l'IA doit :

- comprendre la demande ;
- identifier le module concerné ;
- respecter l'architecture existante ;
- éviter les duplications ;
- privilégier la réutilisation.

Si une information manque, elle doit être explicitement signalée.

---

# 5. Règles de génération de code

Le code généré doit :

- compiler sans erreur ;
- respecter TypeScript Strict Mode ;
- suivre les conventions de nommage ;
- respecter le Design System ;
- rester lisible.

L'IA ne doit jamais inventer des APIs, des composants ou des modèles de données qui n'existent pas dans la documentation du projet.

---

# 6. Règles d'architecture

L'IA doit :

- respecter l'architecture modulaire ;
- créer les fichiers dans les bons dossiers ;
- éviter les dépendances circulaires ;
- limiter le couplage entre modules.

La logique métier ne doit jamais être placée dans les composants UI.

---

# 7. Règles React

Les composants doivent :

- être fonctionnels ;
- rester petits ;
- avoir une responsabilité unique ;
- être composables.

Les hooks personnalisés doivent encapsuler la logique réutilisable.

L'IA doit éviter les optimisations prématurées.

---

# 8. Règles TypeScript

L'IA doit :

- utiliser des types explicites lorsque nécessaire ;
- éviter `any` ;
- privilégier `unknown` lorsqu'un type est inconnu ;
- réutiliser les types existants.

Les types dupliqués sont interdits.

---

# 9. Règles Supabase

Toute interaction avec Supabase doit :

- respecter les politiques de sécurité (RLS) ;
- utiliser les clients officiels ;
- valider les données ;
- gérer les erreurs.

Les clés de service ne doivent jamais être exposées côté client.

---

# 10. Règles UI

Toute interface générée doit :

- utiliser les composants du Design System ;
- être responsive ;
- être accessible ;
- respecter la palette officielle ;
- suivre les règles UX.

L'IA ne doit pas créer de nouveaux composants UI sans justification.

---

# 11. Règles de sécurité

L'IA ne doit jamais :

- exposer des secrets ;
- contourner les contrôles d'accès ;
- supprimer des validations ;
- désactiver des protections de sécurité.

Toute fonctionnalité sensible doit être documentée.

---

# 12. Documentation

Toute modification importante doit être accompagnée de la mise à jour de la documentation concernée.

Si un nouveau module est créé, la documentation correspondante doit être ajoutée ou mise à jour.

---

# 13. Tests

Toute génération de code doit prendre en compte les tests.

Lorsque cela est pertinent, l'IA doit proposer :

- des tests unitaires ;
- des tests d'intégration ;
- des tests E2E.

Le code généré ne doit pas dégrader la couverture de tests.

---

# 14. Workflow IA

Avant toute proposition, l'IA suit le processus suivant :

```text
Lire la documentation

↓

Comprendre la demande

↓

Identifier le module concerné

↓

Vérifier les composants existants

↓

Générer le code

↓

Vérifier TypeScript

↓

Vérifier ESLint

↓

Vérifier les tests

↓

Mettre à jour la documentation si nécessaire
```

---

# 15. Interdictions

L'IA ne doit jamais :

✘ Inventer des exigences métier.

✘ Inventer des APIs.

✘ Inventer des tables SQL.

✘ Inventer des routes.

✘ Modifier l'architecture sans justification.

✘ Supprimer des contrôles de sécurité.

✘ Ignorer les conventions du projet.

✘ Générer du code mort ou inutilisé.

✘ Ajouter une dépendance sans justification.

---

# 16. Checklist

Avant toute proposition de code, vérifier :

□ La demande est comprise.

□ L'architecture est respectée.

□ Les conventions de nommage sont respectées.

□ Les composants existants sont réutilisés.

□ Les types TypeScript sont corrects.

□ Les erreurs sont gérées.

□ Les permissions sont vérifiées.

□ Les composants sont accessibles.

□ Les tests sont pris en compte.

□ La documentation est mise à jour si nécessaire.

---

# 17. Références

- Technology Stack
- Folder Structure
- Naming Conventions
- Coding Standards
- Git Workflow
- Testing Strategy
- Design System
- Security Policy
- Architecture Documentation