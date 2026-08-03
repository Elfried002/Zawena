# Functional Requirements — Zawena Platform

> Produit : Zawena Platform
>
> Document : Functional Requirements
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Objectif
2. Portée
3. Structure des exigences
4. Exigences fonctionnelles
5. Traçabilité
6. Dépendances
7. Références

---

# 1. Objectif

Ce document centralise l'ensemble des exigences fonctionnelles (Functional Requirements - FR) de Zawena Platform.

Chaque exigence représente un comportement attendu du système.

Les exigences décrites ici servent de référence pour :

- les Feature Specifications ;
- les User Stories ;
- les User Flows ;
- les Business Rules ;
- les Acceptance Criteria ;
- les cas de test.

---

# 2. Portée

Les exigences fonctionnelles couvrent les modules suivants :

- Website
- Authentication
- Dashboard
- CRM
- Quotes
- Projects
- Client Portal
- CMS
- Notifications
- Settings

---

# 3. Structure des exigences

Chaque exigence est identifiée selon le format :

FR-XXX

Exemple :

FR-001

FR-002

FR-003

Les exigences sont classées par module.

---

# 4. Exigences fonctionnelles

---

# Website

## FR-WEB-001

Le système doit afficher un site vitrine accessible sans authentification.

Priorité : Critique

---

## FR-WEB-002

Le système doit permettre la consultation des services proposés.

Priorité : Critique

---

## FR-WEB-003

Le système doit permettre aux visiteurs de consulter les réalisations.

---

## FR-WEB-004

Le système doit permettre la consultation du blog.

---

## FR-WEB-005

Le système doit permettre l'envoi d'un formulaire de contact.

---

## FR-WEB-006

Le système doit permettre une demande de devis.

---

## FR-WEB-007

Le système doit rediriger les utilisateurs vers l'authentification.

---

# Authentication

## FR-AUTH-001

Le système doit authentifier les utilisateurs.

---

## FR-AUTH-002

Le système doit gérer les sessions.

---

## FR-AUTH-003

Le système doit permettre la récupération du mot de passe.

---

## FR-AUTH-004

Le système doit vérifier l'adresse email.

---

## FR-AUTH-005

Le système doit gérer les profils utilisateurs.

---

## FR-AUTH-006

Le système doit appliquer les rôles.

---

## FR-AUTH-007

Le système doit appliquer les permissions.

---

# Dashboard

## FR-DASH-001

Le système doit afficher un tableau de bord personnalisé.

---

## FR-DASH-002

Le système doit afficher les indicateurs clés.

---

## FR-DASH-003

Le système doit afficher les notifications.

---

## FR-DASH-004

Le système doit permettre une recherche globale.

---

## FR-DASH-005

Le système doit afficher les activités récentes.

---

# CRM

## FR-CRM-001

Le système doit gérer les Leads.

---

## FR-CRM-002

Le système doit gérer les Prospects.

---

## FR-CRM-003

Le système doit gérer les Entreprises.

---

## FR-CRM-004

Le système doit gérer les Contacts.

---

## FR-CRM-005

Le système doit gérer les Opportunités.

---

## FR-CRM-006

Le système doit gérer le Pipeline commercial.

---

## FR-CRM-007

Le système doit gérer les Activités.

---

## FR-CRM-008

Le système doit gérer les Notes.

---

## FR-CRM-009

Le système doit permettre l'export des données CRM.

---

# Quotes

## FR-QUOTE-001

Le système doit permettre la création d'un devis.

---

## FR-QUOTE-002

Le système doit calculer automatiquement les montants.

---

## FR-QUOTE-003

Le système doit générer un devis au format PDF.

---

## FR-QUOTE-004

Le système doit permettre l'envoi d'un devis.

---

## FR-QUOTE-005

Le système doit suivre le statut des devis.

---

## FR-QUOTE-006

Le système doit convertir un devis accepté en contrat.

---

## FR-QUOTE-007

Le système doit créer automatiquement un projet après validation.

---

# Projects

## FR-PROJ-001

Le système doit permettre la création d'un projet.

---

## FR-PROJ-002

Le système doit gérer les équipes.

---

## FR-PROJ-003

Le système doit gérer les phases.

---

## FR-PROJ-004

Le système doit gérer les jalons.

---

## FR-PROJ-005

Le système doit gérer les tâches.

---

## FR-PROJ-006

Le système doit gérer les sous-tâches.

---

## FR-PROJ-007

Le système doit gérer les livrables.

---

## FR-PROJ-008

Le système doit gérer les documents.

---

## FR-PROJ-009

Le système doit gérer les discussions.

---

## FR-PROJ-010

Le système doit clôturer un projet.

---

# Client Portal

## FR-CLIENT-001

Le système doit fournir un portail sécurisé aux clients.

---

## FR-CLIENT-002

Le système doit permettre le suivi des projets.

---

## FR-CLIENT-003

Le système doit permettre le téléchargement des documents.

---

## FR-CLIENT-004

Le système doit permettre la validation des livrables.

---

## FR-CLIENT-005

Le système doit afficher les devis et contrats.

---

# CMS

## FR-CMS-001

Le système doit gérer les contenus.

---

## FR-CMS-002

Le système doit gérer les médias.

---

## FR-CMS-003

Le système doit gérer le référencement SEO.

---

## FR-CMS-004

Le système doit permettre la publication.

---

## FR-CMS-005

Le système doit permettre l'archivage des contenus.

---

# Notifications

## FR-NOTIF-001

Le système doit générer des notifications automatiques.

---

## FR-NOTIF-002

Le système doit envoyer des emails.

---

## FR-NOTIF-003

Le système doit afficher les notifications In-App.

---

## FR-NOTIF-004

Le système doit permettre la gestion des préférences.

---

## FR-NOTIF-005

Le système doit conserver un historique.

---

# Settings

## FR-SET-001

Le système doit gérer les organisations.

---

## FR-SET-002

Le système doit gérer les utilisateurs.

---

## FR-SET-003

Le système doit gérer les rôles.

---

## FR-SET-004

Le système doit gérer les permissions.

---

## FR-SET-005

Le système doit gérer les paramètres de sécurité.

---

## FR-SET-006

Le système doit gérer les intégrations.

---

## FR-SET-007

Le système doit gérer le branding.

---

## FR-SET-008

Le système doit gérer les journaux d'audit.

---

# 5. Traçabilité

Chaque exigence fonctionnelle est liée aux documents suivants :

Functional Requirement

↓

Feature Specification

↓

User Story

↓

User Flow

↓

Business Rule

↓

Acceptance Criteria

↓

Cas de test

---

# 6. Dépendances

Ce document dépend de :

- docs/product/prd.md
- docs/product/mvp-definition.md
- docs/product/features/
- docs/product/user-stories/
- docs/product/user-flows/

---

# 7. Références

- Product Vision
- PRD
- MVP Definition
- Feature Specifications
- User Stories
- User Flows
- Roadmap

---