# Responsive Design — Zawena Platform

> Produit : Zawena Platform
>
> Document : Responsive Design
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Design System Team

---

# Table des matières

1. Objectif
2. Principes
3. Approche Mobile-First
4. Breakpoints
5. Adaptation des layouts
6. Comportement des composants
7. Navigation responsive
8. Responsive des tableaux
9. Responsive des formulaires
10. Responsive du Dashboard
11. Bonnes pratiques
12. Références

---

# 1. Objectif

Ce document définit les règles de conception responsive utilisées par Zawena Platform.

L'objectif est d'offrir une expérience utilisateur cohérente sur :

- Smartphone
- Tablette
- Ordinateur portable
- Écran de bureau
- Grand écran

Toutes les interfaces doivent être conçues selon une approche Mobile-First.

---

# 2. Principes

Le Responsive Design repose sur les principes suivants :

- Mobile-First
- Progressive Enhancement
- Layouts fluides
- Composants adaptatifs
- Lisibilité constante
- Navigation optimisée

Les interfaces ne doivent jamais dépendre d'une résolution spécifique.

---

# 3. Approche Mobile-First

Le développement commence toujours par la version mobile.

Les adaptations pour les écrans plus larges sont ajoutées progressivement.

Ordre de conception :

```text
Mobile

↓

Tablette

↓

Desktop

↓

Grand écran
```

Les composants doivent fonctionner correctement sur mobile avant toute optimisation desktop.

---

# 4. Breakpoints

Zawena adopte les breakpoints standards de Tailwind CSS.

| Breakpoint | Largeur minimale | Usage |
|------------|-----------------:|-------|
| Base | < 640 px | Smartphones |
| `sm` | ≥ 640 px | Smartphones paysage |
| `md` | ≥ 768 px | Tablettes |
| `lg` | ≥ 1024 px | Ordinateurs portables |
| `xl` | ≥ 1280 px | Écrans de bureau |
| `2xl` | ≥ 1536 px | Très grands écrans |

Les nouveaux composants doivent utiliser ces breakpoints.

---

# 5. Adaptation des layouts

## Mobile

- Sidebar masquée
- Menu hamburger
- Une seule colonne
- Cartes empilées

---

## Tablette

- Sidebar repliable
- Deux colonnes lorsque pertinent
- Navigation simplifiée

---

## Desktop

- Sidebar visible
- Dashboard complet
- Grille sur 12 colonnes
- Navigation permanente

---

## Grand écran

- Contenu centré
- Largeur maximale contrôlée
- Utilisation optimisée de l'espace

---

# 6. Comportement des composants

Tous les composants doivent s'adapter automatiquement.

Exemples :

## Boutons

- largeur complète sur mobile lorsque nécessaire ;
- largeur automatique sur desktop.

---

## Cartes

- empilement vertical sur mobile ;
- disposition en grille sur desktop.

---

## Modales

- plein écran ou largeur importante sur mobile ;
- largeur limitée sur desktop.

---

## Menus

- menu déroulant ou plein écran sur mobile ;
- menu contextuel sur desktop.

---

# 7. Navigation responsive

## Mobile

- Menu hamburger
- Navigation simplifiée
- Icônes prioritaires

---

## Desktop

- Sidebar permanente
- Recherche visible
- Navigation complète

---

## Breadcrumbs

Les breadcrumbs sont :

- masqués si l'espace est insuffisant ;
- affichés sur tablette et desktop.

---

# 8. Responsive des tableaux

Les tableaux doivent rester utilisables sur tous les appareils.

Lorsque l'espace est limité :

- défilement horizontal contrôlé ;
- colonnes secondaires masquées si nécessaire ;
- actions regroupées dans un menu.

Les données critiques doivent toujours rester visibles.

---

# 9. Responsive des formulaires

## Mobile

- Champs sur une seule colonne
- Boutons pleine largeur lorsque pertinent

---

## Desktop

- Plusieurs colonnes possibles
- Alignement horizontal des champs liés
- Actions regroupées

Les formulaires doivent rester lisibles sans zoom.

---

# 10. Responsive du Dashboard

Le Dashboard adapte automatiquement :

- les widgets ;
- les graphiques ;
- les tableaux ;
- les cartes ;
- les KPI.

Les informations prioritaires restent visibles sur toutes les tailles d'écran.

---

# 11. Bonnes pratiques

Les développeurs doivent :

- privilégier les unités relatives ;
- utiliser les breakpoints officiels ;
- éviter les dimensions fixes ;
- tester les interfaces sur plusieurs tailles d'écran ;
- garantir une navigation fluide quel que soit l'appareil.

Chaque nouvelle interface doit être validée sur mobile, tablette et desktop avant sa mise en production.

---

# 12. Références

- UI Foundation
- Layout System
- Grid System
- Navigation
- Components
- Forms
- Dashboard
- Accessibility
- UX Guidelines