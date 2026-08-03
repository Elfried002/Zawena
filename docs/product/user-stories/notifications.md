# User Stories — Notifications

> Produit : Zawena Platform
>
> Module : Notifications
>
> Identifiant : USER-STORIES-NOTIFICATIONS
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
6. Mapping avec les Feature Specifications
7. Dépendances
8. Références

---

# 1. Objectif

Ce document décrit les User Stories du module Notifications.

Le moteur de notifications informe les utilisateurs des événements importants générés par les différents modules de Zawena Platform.

---

# 2. Vue d'ensemble

Le module permet de :

- recevoir des notifications ;
- consulter l'historique ;
- marquer une notification comme lue ;
- gérer ses préférences ;
- recevoir des emails automatiques.

---

# 3. Personas concernés

## Principaux

- Administrator
- Sales
- Project Manager
- Developer
- Support
- Client
- Partner

## Secondaires

- Super Administrator

---

# 4. Epics

## Epic 1 — Centre de notifications

US-NOTIF-001 à US-NOTIF-005

---

## Epic 2 — Gestion des notifications

US-NOTIF-006 à US-NOTIF-009

---

## Epic 3 — Préférences

US-NOTIF-010 à US-NOTIF-012

---

# 5. User Stories

---

# Epic 1 — Centre de notifications

## US-NOTIF-001 — Consulter le centre de notifications

En tant que Utilisateur

Je veux accéder au centre de notifications

Afin de consulter les événements récents.

Critères d'acceptation

- Liste chargée.
- Tri par date.
- Pagination si nécessaire.

---

## US-NOTIF-002 — Voir le nombre de notifications non lues

Afin d'identifier rapidement les nouveaux événements.

---

## US-NOTIF-003 — Consulter une notification

Afin d'obtenir le détail d'un événement.

---

## US-NOTIF-004 — Ouvrir la ressource liée

Afin d'accéder directement au projet, devis ou document concerné.

---

## US-NOTIF-005 — Rechercher une notification

Afin de retrouver un événement précis.

---

# Epic 2 — Gestion des notifications

## US-NOTIF-006 — Marquer une notification comme lue

---

## US-NOTIF-007 — Marquer toutes les notifications comme lues

---

## US-NOTIF-008 — Archiver une notification

---

## US-NOTIF-009 — Recevoir une notification email

---

# Epic 3 — Préférences

## US-NOTIF-010 — Consulter mes préférences

---

## US-NOTIF-011 — Modifier mes préférences

---

## US-NOTIF-012 — Activer ou désactiver les emails

---

# 6. Mapping avec les Feature Specifications

| User Story | Feature |
|------------|---------|
| US-NOTIF-001 | FEATURE-NOTIFICATIONS |
| US-NOTIF-002 | FEATURE-NOTIFICATIONS |
| US-NOTIF-003 | FEATURE-NOTIFICATIONS |
| US-NOTIF-004 | FEATURE-NOTIFICATIONS |
| US-NOTIF-005 | FEATURE-NOTIFICATIONS |
| US-NOTIF-006 | FEATURE-NOTIFICATIONS |
| US-NOTIF-007 | FEATURE-NOTIFICATIONS |
| US-NOTIF-008 | FEATURE-NOTIFICATIONS |
| US-NOTIF-009 | FEATURE-NOTIFICATIONS |
| US-NOTIF-010 | FEATURE-NOTIFICATIONS |
| US-NOTIF-011 | FEATURE-NOTIFICATIONS |
| US-NOTIF-012 | FEATURE-NOTIFICATIONS |

---

# 7. Dépendances

- docs/product/features/notifications.md
- docs/product/features/authentication.md
- docs/architecture/api.md
- docs/architecture/database.md

---

# 8. Références

- Notifications Feature Specification
- Authentication Feature Specification
- Architecture Database
- Architecture API
- Design System

---