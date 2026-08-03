# Navigation System — Zawena Platform

> Produit : Zawena Platform
>
> Document : Navigation System
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
2. Principes de navigation
3. Architecture de navigation
4. Header
5. Sidebar
6. Menus
7. Breadcrumbs
8. Recherche globale
9. Navigation mobile
10. États de navigation
11. Bonnes pratiques
12. Références

---

# 1. Objectif

Ce document définit le système de navigation utilisé dans Zawena Platform.

Il garantit une navigation :

- cohérente ;
- intuitive ;
- rapide ;
- accessible ;
- responsive.

Toutes les interfaces doivent respecter les règles décrites dans ce document.

---

# 2. Principes de navigation

La navigation repose sur les principes suivants :

- simplicité ;
- cohérence ;
- visibilité ;
- prévisibilité ;
- rapidité d'accès ;
- limitation du nombre de clics.

Les utilisateurs doivent toujours savoir :

- où ils se trouvent ;
- où ils peuvent aller ;
- comment revenir en arrière.

---

# 3. Architecture de navigation

La plateforme est organisée autour de quatre espaces principaux.

```text
Website

↓

Authentication

↓

Dashboard

↓

Client Portal
```

Chaque espace possède sa propre navigation tout en conservant les mêmes principes d'utilisation.

---

# 4. Header

Le Header est présent sur toutes les interfaces authentifiées.

Il contient :

- Logo
- Nom de l'organisation
- Recherche globale
- Notifications
- Profil utilisateur
- Menu utilisateur

Le Header reste visible lors du défilement lorsque cela améliore l'expérience utilisateur.

---

# 5. Sidebar

La Sidebar constitue la navigation principale du Dashboard.

Exemple :

```text
Dashboard

CRM

Quotes

Projects

CMS

Notifications

Settings
```

### Comportement

Desktop :

- visible en permanence ;
- réductible (mode compact).

Mobile :

- masquée par défaut ;
- affichée sous forme de panneau latéral.

Les éléments visibles dépendent des permissions de l'utilisateur.

---

# 6. Menus

Les menus doivent être organisés par domaine métier.

Exemple :

```text
CRM

├── Leads
├── Prospects
├── Companies
├── Contacts
└── Opportunities
```

Les menus doivent :

- limiter la profondeur de navigation ;
- utiliser des libellés explicites ;
- conserver un ordre logique.

Les sous-menus sont repliables.

---

# 7. Breadcrumbs

Les Breadcrumbs permettent de situer l'utilisateur dans la hiérarchie de l'application.

Exemple :

```text
Dashboard

>

Projects

>

Projet Alpha

>

Livrables
```

Règles :

- affichés sur les écrans moyens et grands ;
- masqués si l'espace est insuffisant ;
- chaque niveau (sauf le dernier) est cliquable.

---

# 8. Recherche globale

La recherche globale est accessible depuis le Header.

Elle permet de rechercher notamment :

- Leads
- Entreprises
- Contacts
- Opportunités
- Devis
- Projets
- Documents
- Pages CMS

La recherche doit :

- être rapide ;
- tolérer les fautes simples ;
- proposer des résultats pertinents.

---

# 9. Navigation mobile

Sur mobile :

- Sidebar remplacée par un menu latéral ;
- Header simplifié ;
- menus optimisés pour le tactile ;
- priorité aux actions principales.

Les éléments interactifs doivent respecter des dimensions adaptées aux écrans tactiles.

---

# 10. États de navigation

Les éléments de navigation possèdent plusieurs états.

## Default

État normal.

---

## Hover

Indique que l'élément est interactif.

---

## Active

Indique la page actuellement affichée.

---

## Focus

Visible lors de la navigation au clavier.

---

## Disabled

Indique qu'une action n'est pas disponible.

---

## Expanded / Collapsed

Utilisé pour les menus et sous-menus.

Les transitions doivent être fluides et cohérentes.

---

# 11. Bonnes pratiques

Les développeurs doivent :

- limiter les niveaux de navigation ;
- maintenir les menus cohérents entre les modules ;
- conserver les mêmes icônes et libellés ;
- afficher clairement la page active ;
- garantir une navigation complète au clavier ;
- éviter les menus surchargés.

Toute nouvelle entrée de navigation doit être validée avant son intégration.

---

# 12. Références

- UI Foundation
- Layout System
- Grid System
- Responsive Design
- Components
- Dashboard
- Accessibility
- UX Guidelines