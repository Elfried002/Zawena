# User Experience (UX) Guidelines — Zawena Platform

> Produit : Zawena Platform
>
> Document : User Experience (UX) Guidelines
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Product & UX Team

---

# Table des matières

1. Objectif
2. Vision UX
3. Principes UX
4. Parcours utilisateur
5. Architecture de l'information
6. Charge cognitive
7. Feedback utilisateur
8. États d'interface
9. Gestion des erreurs
10. Confirmation des actions
11. Recherche et navigation
12. Performance perçue
13. Accessibilité
14. Personnalisation
15. Bonnes pratiques
16. Anti-patterns
17. Références

---

# 1. Objectif

Ce document définit les principes d'expérience utilisateur de Zawena Platform.

Son objectif est de garantir une expérience :

- cohérente ;
- intuitive ;
- efficace ;
- accessible ;
- orientée vers la productivité.

Toutes les fonctionnalités développées pour Zawena doivent respecter ces principes.

---

# 2. Vision UX

Zawena est conçu pour aider les utilisateurs à accomplir leurs tâches avec un minimum d'effort.

L'expérience utilisateur doit être :

- simple ;
- fluide ;
- prévisible ;
- rassurante ;
- rapide.

L'interface doit s'adapter à l'utilisateur, et non l'inverse.

---

# 3. Principes UX

Les décisions de conception reposent sur les principes suivants.

## Simplicité

Réduire les étapes inutiles.

---

## Cohérence

Les mêmes actions produisent toujours les mêmes résultats.

---

## Clarté

Les informations importantes sont immédiatement visibles.

---

## Prévisibilité

L'utilisateur doit anticiper le résultat de ses actions.

---

## Contrôle

L'utilisateur garde le contrôle de ses données et de ses actions.

---

## Feedback

Chaque interaction fournit un retour approprié.

---

## Tolérance aux erreurs

L'application aide l'utilisateur à éviter et corriger les erreurs.

---

# 4. Parcours utilisateur

Chaque parcours doit être :

- logique ;
- progressif ;
- limité au nombre d'étapes nécessaires.

Avant de créer un nouvel écran, vérifier :

- quel est l'objectif de l'utilisateur ;
- quelles informations sont indispensables ;
- quelles actions sont prioritaires.

---

# 5. Architecture de l'information

Les informations doivent suivre une hiérarchie claire.

Ordre recommandé :

```text
Titre

↓

Contexte

↓

Actions principales

↓

Contenu

↓

Informations secondaires

↓

Historique
```

Les éléments critiques doivent apparaître avant les informations secondaires.

---

# 6. Charge cognitive

L'interface doit réduire l'effort mental.

Les bonnes pratiques sont :

- limiter les choix simultanés ;
- regrouper les informations similaires ;
- utiliser des libellés explicites ;
- masquer les options avancées tant qu'elles ne sont pas nécessaires.

Les utilisateurs ne doivent jamais être submergés par l'information.

---

# 7. Feedback utilisateur

Chaque action importante doit produire un retour.

Exemples :

- chargement ;
- succès ;
- erreur ;
- avertissement ;
- progression.

Le feedback doit être :

- rapide ;
- compréhensible ;
- non intrusif.

---

# 8. États d'interface

Chaque écran doit prévoir les états suivants.

## Loading

Les contenus utilisent des Skeletons lorsque cela est pertinent.

---

## Empty State

L'interface explique pourquoi aucune donnée n'est affichée et propose une action lorsque cela est possible.

Exemple :

```text
Vous n'avez encore créé aucun projet.

[Créer un projet]
```

---

## Error State

Les erreurs expliquent :

- ce qui s'est passé ;
- les conséquences ;
- les actions possibles.

---

## Success State

Les réussites sont confirmées de manière visible mais discrète.

---

# 9. Gestion des erreurs

Les erreurs doivent :

- utiliser un langage clair ;
- éviter le jargon technique ;
- proposer une solution lorsque cela est possible.

Exemple :

```text
Impossible d'enregistrer le devis.

Vérifiez votre connexion puis réessayez.
```

Les erreurs ne doivent jamais bloquer inutilement l'utilisateur.

---

# 10. Confirmation des actions

Les confirmations sont réservées aux actions importantes.

Exemples :

- suppression ;
- archivage ;
- désactivation ;
- publication.

Les actions réversibles ne nécessitent pas toujours une confirmation.

Lorsque cela est possible, privilégier une fonctionnalité d'annulation (Undo).

---

# 11. Recherche et navigation

Les utilisateurs doivent retrouver rapidement une information.

L'application doit proposer :

- recherche globale ;
- filtres ;
- tri ;
- pagination ;
- breadcrumbs.

Les chemins de navigation doivent rester courts.

---

# 12. Performance perçue

L'expérience utilisateur dépend autant de la perception que du temps réel.

Le système doit :

- afficher rapidement une interface ;
- utiliser des Skeletons ;
- charger progressivement les données ;
- éviter les écrans vides pendant les traitements.

L'utilisateur doit toujours comprendre que l'application fonctionne.

---

# 13. Accessibilité

L'expérience utilisateur doit être inclusive.

Toutes les interfaces doivent respecter les règles définies dans :

```
docs/design-system/accessibility.md
```

L'accessibilité fait partie intégrante de l'expérience utilisateur.

---

# 14. Personnalisation

Lorsque cela est pertinent, les utilisateurs peuvent personnaliser :

- leur Dashboard ;
- les filtres par défaut ;
- les préférences de notification ;
- certains paramètres d'affichage.

La personnalisation ne doit jamais compromettre la cohérence générale de la plateforme.

---

# 15. Bonnes pratiques

✔ Concevoir en fonction des objectifs des utilisateurs.

✔ Réduire le nombre de clics.

✔ Utiliser un langage simple.

✔ Afficher uniquement les informations utiles.

✔ Fournir un feedback immédiat.

✔ Faciliter la récupération après une erreur.

✔ Garantir une expérience cohérente entre les modules.

---

# 16. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Multiplier les fenêtres de confirmation.

✘ Cacher les actions importantes.

✘ Utiliser des messages techniques.

✘ Modifier fréquemment la disposition des écrans.

✘ Imposer des parcours complexes pour des tâches simples.

✘ Afficher des informations inutiles.

✘ Interrompre l'utilisateur sans raison.

---

# 17. Références

- UI Foundation
- Layout System
- Navigation System
- Components Library
- Forms
- Dashboard
- Accessibility Guidelines
- Product Vision
- User Flows