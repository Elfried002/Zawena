# User Stories — CMS (Content Management System)

> Produit : Zawena Platform
>
> Module : CMS
>
> Identifiant : USER-STORIES-CMS
>
> Version : 1.0
>
> Statut : MVP
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Objectif
2. Vue d'ensemble
3. Personas concernés
4. Epics
5. User Stories
6. Dépendances
7. Références

---

# 1. Objectif

Ce document décrit les User Stories du module CMS de Zawena Platform.

Le CMS permet aux administrateurs de créer, modifier, organiser, publier et archiver les contenus du site web sans intervention des développeurs.

---

# 2. Vue d'ensemble

Le module CMS permet de gérer :

- les pages ;
- les services ;
- les articles du blog ;
- les études de cas ;
- la FAQ ;
- les pages légales ;
- les médias ;
- les métadonnées SEO.

---

# 3. Personas concernés

## Principaux

- Administrator
- Super Administrator

## Secondaires

- Sales (lecture)
- Developer (lecture)

---

# 4. Epics

## Epic 1 — Gestion des contenus

US-CMS-001 à US-CMS-005

---

## Epic 2 — Publication

US-CMS-006 à US-CMS-009

---

## Epic 3 — Médias

US-CMS-010 à US-CMS-013

---

## Epic 4 — SEO

US-CMS-014 à US-CMS-016

---

## Epic 5 — Organisation

US-CMS-017 à US-CMS-018

---

# 5. User Stories

---

# Epic 1 — Gestion des contenus

## US-CMS-001 — Créer un contenu

### En tant que

Administrator

### Je veux

Créer un nouveau contenu.

### Afin de

Publier de nouvelles informations sur le site.

#### Critères d'acceptation

- Formulaire valide.
- Brouillon enregistré.
- Auteur enregistré.
- Date de création enregistrée.

---

## US-CMS-002 — Modifier un contenu

### En tant que

Administrator

### Je veux

Modifier un contenu existant.

### Afin de

Mettre à jour les informations publiées.

---

## US-CMS-003 — Consulter un contenu

### En tant que

Administrator

### Je veux

Prévisualiser un contenu.

### Afin de

Vérifier son apparence avant publication.

---

## US-CMS-004 — Archiver un contenu

### En tant que

Administrator

### Je veux

Archiver un contenu.

### Afin de

Le retirer du site sans le supprimer définitivement.

---

## US-CMS-005 — Supprimer un contenu

### En tant que

Administrator

### Je veux

Supprimer un contenu.

### Afin de

Nettoyer les contenus obsolètes.

---

# Epic 2 — Publication

## US-CMS-006 — Publier un contenu

### En tant que

Administrator

Je veux publier un contenu.

Afin qu'il soit visible sur le site.

---

## US-CMS-007 — Dépublier un contenu

### En tant que

Administrator

Je veux retirer un contenu publié.

Afin qu'il ne soit plus accessible.

---

## US-CMS-008 — Enregistrer un brouillon

### En tant que

Administrator

Je veux sauvegarder un brouillon.

Afin de poursuivre sa rédaction ultérieurement.

---

## US-CMS-009 — Prévisualiser avant publication

### En tant que

Administrator

Je veux voir le rendu final.

Afin de contrôler la qualité du contenu.

---

# Epic 3 — Médias

## US-CMS-010 — Téléverser une image

### En tant que

Administrator

Je veux ajouter une image.

Afin d'illustrer un contenu.

---

## US-CMS-011 — Associer un média

### En tant que

Administrator

Je veux associer un média à un contenu.

Afin d'améliorer sa présentation.

---

## US-CMS-012 — Supprimer un média

### En tant que

Administrator

Je veux retirer un média inutilisé.

Afin de maintenir une médiathèque propre.

---

## US-CMS-013 — Consulter la médiathèque

### En tant que

Administrator

Je veux parcourir les médias existants.

Afin de réutiliser des ressources.

---

# Epic 4 — SEO

## US-CMS-014 — Définir le titre SEO

### En tant que

Administrator

Je veux renseigner un titre SEO.

Afin d'améliorer le référencement.

---

## US-CMS-015 — Définir la méta-description

### En tant que

Administrator

Je veux définir une méta-description.

Afin d'optimiser l'affichage dans les moteurs de recherche.

---

## US-CMS-016 — Définir le slug

### En tant que

Administrator

Je veux personnaliser l'URL.

Afin d'obtenir une adresse lisible et optimisée.

---

# Epic 5 — Organisation

## US-CMS-017 — Rechercher un contenu

### En tant que

Administrator

Je veux rechercher rapidement un contenu.

Afin de le retrouver facilement.

---

## US-CMS-018 — Filtrer les contenus

### En tant que

Administrator

Je veux filtrer les contenus.

Afin de retrouver uniquement ceux correspondant à mes critères.

---

# 6. Dépendances

Ce document dépend des éléments suivants :

- docs/product/features/cms.md
- docs/design-system/
- docs/architecture/database.md
- docs/architecture/api.md

---

# 7. Références

- CMS Feature Specification
- Design System
- SEO Strategy
- Architecture Database
- Architecture API