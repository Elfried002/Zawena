# User Stories — Quotes (Gestion des Devis)

> Produit : Zawena Platform
>
> Module : Quotes
>
> Identifiant : USER-STORIES-QUOTES
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

Ce document décrit les User Stories du module Quotes.

Le module Quotes permet de créer, modifier, envoyer, suivre et convertir les devis commerciaux en contrats puis en projets.

---

# 2. Vue d'ensemble

Le module couvre :

- création de devis ;
- gestion des lignes de prestations ;
- calcul automatique des montants ;
- génération PDF ;
- envoi au client ;
- suivi du statut ;
- acceptation/refus ;
- conversion en projet.

---

# 3. Personas concernés

## Principaux

- Sales
- Administrator

## Secondaires

- Project Manager
- Client
- Super Administrator

---

# 4. Epics

## Epic 1 — Création

US-QUOTE-001 à US-QUOTE-005

---

## Epic 2 — Gestion

US-QUOTE-006 à US-QUOTE-010

---

## Epic 3 — Validation

US-QUOTE-011 à US-QUOTE-014

---

## Epic 4 — Conversion

US-QUOTE-015 à US-QUOTE-018

---

# 5. User Stories

---

# Epic 1 — Création

## US-QUOTE-001 — Créer un devis

En tant que Sales

Je veux créer un devis

Afin de proposer une offre commerciale à un prospect.

Critères d'acceptation

- Numéro unique généré.
- Opportunité associée.
- Statut "Brouillon".
- Auteur enregistré.

---

## US-QUOTE-002 — Ajouter une ligne de prestation

Afin de détailler les services proposés.

---

## US-QUOTE-003 — Ajouter une option

Afin de proposer des prestations complémentaires.

---

## US-QUOTE-004 — Définir les conditions commerciales

Afin d'informer le client des modalités.

---

## US-QUOTE-005 — Générer automatiquement les totaux

Afin d'éviter les erreurs de calcul.

---

# Epic 2 — Gestion

## US-QUOTE-006 — Modifier un devis

---

## US-QUOTE-007 — Dupliquer un devis

---

## US-QUOTE-008 — Générer un PDF

---

## US-QUOTE-009 — Télécharger un devis

---

## US-QUOTE-010 — Envoyer un devis au client

---

# Epic 3 — Validation

## US-QUOTE-011 — Consulter le statut

---

## US-QUOTE-012 — Accepter un devis

---

## US-QUOTE-013 — Refuser un devis

---

## US-QUOTE-014 — Archiver un devis

---

# Epic 4 — Conversion

## US-QUOTE-015 — Convertir un devis accepté en contrat

---

## US-QUOTE-016 — Convertir un contrat en projet

---

## US-QUOTE-017 — Consulter l'historique des versions

---

## US-QUOTE-018 — Consulter les statistiques des devis

---

# 6. Mapping avec les Feature Specifications

| User Story | Feature |
|------------|---------|
| US-QUOTE-001 | FEATURE-QUOTES |
| US-QUOTE-002 | FEATURE-QUOTES |
| US-QUOTE-003 | FEATURE-QUOTES |
| US-QUOTE-004 | FEATURE-QUOTES |
| US-QUOTE-005 | FEATURE-QUOTES |
| US-QUOTE-006 | FEATURE-QUOTES |
| US-QUOTE-007 | FEATURE-QUOTES |
| US-QUOTE-008 | FEATURE-QUOTES |
| US-QUOTE-009 | FEATURE-QUOTES |
| US-QUOTE-010 | FEATURE-QUOTES |
| US-QUOTE-011 | FEATURE-QUOTES |
| US-QUOTE-012 | FEATURE-QUOTES |
| US-QUOTE-013 | FEATURE-QUOTES |
| US-QUOTE-014 | FEATURE-QUOTES |
| US-QUOTE-015 | FEATURE-QUOTES |
| US-QUOTE-016 | FEATURE-QUOTES |
| US-QUOTE-017 | FEATURE-QUOTES |
| US-QUOTE-018 | FEATURE-QUOTES |

---

# 7. Dépendances

Ce document dépend des éléments suivants :

- docs/product/features/quotes.md
- docs/product/features/crm.md
- docs/product/features/projects.md
- docs/architecture/database.md
- docs/architecture/api.md

---

# 8. Références

- Quotes Feature Specification
- CRM Feature Specification
- Projects Feature Specification
- Business Rules
- Architecture Database

---