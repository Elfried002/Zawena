# User Flows — Visitor

> Produit : Zawena Platform
>
> Module : Website
>
> Identifiant : USER-FLOWS-VISITOR
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
4. Parcours utilisateur
5. Cas alternatifs
6. Cas d'erreur
7. Dépendances
8. Références

---

# 1. Objectif

Ce document décrit les différents parcours d'un visiteur sur le site public de Zawena.

Il détaille les interactions possibles depuis l'arrivée sur le site jusqu'à la prise de contact ou la demande de devis.

---

# 2. Vue d'ensemble

Le visiteur peut :

- découvrir Zawena ;
- consulter les services ;
- lire les articles du blog ;
- consulter les réalisations ;
- envoyer un message ;
- demander un devis ;
- accéder à la page de connexion.

---

# 3. Personas concernés

- Visitor
- Prospect

---

# 4. Parcours utilisateur

---

# Flow 1 — Découverte de Zawena

## Objectif

Permettre au visiteur de comprendre rapidement ce que propose Zawena.

### Déclencheur

Le visiteur accède au site.

### Parcours principal

Accueil

↓

Hero

↓

Présentation

↓

Services

↓

Réalisations

↓

CTA

↓

Contact

### Résultat

Le visiteur comprend l'offre de Zawena et poursuit sa navigation.

---

# Flow 2 — Découverte des services

### Déclencheur

Le visiteur clique sur « Services ».

### Parcours

Accueil

↓

Liste des services

↓

Sélection d'un service

↓

Page détaillée

↓

CTA

↓

Demande de devis

### Résultat

Le visiteur découvre les prestations adaptées à son besoin.

---

# Flow 3 — Consultation des réalisations

### Parcours

Accueil

↓

Réalisations

↓

Étude de cas

↓

Résultats

↓

Contact

---

# Flow 4 — Lecture du blog

### Parcours

Accueil

↓

Blog

↓

Liste des articles

↓

Article

↓

Article associé

↓

Contact

---

# Flow 5 — Consultation de la FAQ

### Parcours

Accueil

↓

FAQ

↓

Recherche

↓

Réponse

↓

Retour navigation

---

# Flow 6 — Demande de devis

### Déclencheur

Clique sur « Demander un devis ».

### Parcours

Formulaire

↓

Validation

↓

Création du Lead

↓

Confirmation

↓

Notification Sales

### Résultat

Une nouvelle opportunité commerciale est créée dans le CRM.

---

# Flow 7 — Prise de contact

### Parcours

Contact

↓

Formulaire

↓

Validation

↓

Envoi

↓

Confirmation

↓

Notification interne

---

# Flow 8 — Accès à la connexion

### Parcours

Accueil

↓

Connexion

↓

Authentication

↓

Dashboard

---

# 5. Cas alternatifs

## Aucun résultat

Le visiteur ne trouve pas l'information recherchée.

↓

FAQ

↓

Contact

---

## Abandon du formulaire

Le visiteur quitte le formulaire avant validation.

↓

Aucune donnée enregistrée.

---

## Retour arrière

Le visiteur retourne à la page précédente.

↓

Navigation conservée.

---

# 6. Cas d'erreur

## Formulaire invalide

↓

Messages d'erreur

↓

Correction

↓

Nouvelle validation

---

## Erreur serveur

↓

Message d'erreur

↓

Nouvel essai

---

## Page inexistante

↓

Erreur 404

↓

Retour accueil

---

# 7. Dépendances

- docs/product/features/website.md
- docs/product/user-stories/website.md
- docs/architecture/api.md
- docs/design-system/navigation.md

---

# 8. Références

- Website Feature Specification
- Website User Stories
- Sitemap
- Design System

---