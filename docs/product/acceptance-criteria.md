# Acceptance Criteria — Zawena Platform

> Produit : Zawena Platform
>
> Document : Acceptance Criteria
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
2. Structure des critères d'acceptation
3. Critères d'acceptation
4. Traçabilité
5. Références

---

# 1. Objectif

Ce document définit les critères d'acceptation (Acceptance Criteria) permettant de valider que chaque fonctionnalité de Zawena Platform répond aux exigences métier et techniques.

Les critères d'acceptation servent de référence pour :

- les développeurs ;
- les testeurs (QA) ;
- les Product Owners ;
- les revues fonctionnelles ;
- les tests d'acceptation utilisateur (UAT).

---

# 2. Structure des critères d'acceptation

Chaque critère suit le format :

AC-XXX-YYY

Exemple :

AC-CRM-001

AC-PROJ-014

AC-CMS-006

Les scénarios utilisent la syntaxe Gherkin :

Given
When
Then

---

# 3. Critères d'acceptation

# Website

## AC-WEB-001 — Envoi d'un formulaire de contact

Feature

Website

Business Rule

BR-WEB-001

### Scenario

Given

Un visiteur consulte la page Contact.

When

Il complète tous les champs obligatoires et soumet le formulaire.

Then

- le formulaire est accepté ;
- un Lead est créé dans le CRM ;
- un message de confirmation est affiché.

---

## AC-WEB-002 — Demande de devis

Given

Le visiteur remplit le formulaire de devis.

When

Le formulaire est validé.

Then

- une demande est enregistrée ;
- un Lead est créé ;
- une notification est envoyée au commercial.

---

# Authentication

## AC-AUTH-001 — Connexion

Given

Un utilisateur possède un compte actif.

When

Il saisit des identifiants valides.

Then

- la connexion est autorisée ;
- une session est créée ;
- le Dashboard est affiché.

---

## AC-AUTH-002 — Mot de passe oublié

Given

Un utilisateur demande une réinitialisation.

When

Son adresse email est valide.

Then

- un lien sécurisé est envoyé ;
- le lien permet de définir un nouveau mot de passe.

---

# CRM

## AC-CRM-001 — Création d'un Lead

Given

Un commercial crée un Lead.

When

Les informations obligatoires sont renseignées.

Then

- le Lead est enregistré ;
- un identifiant unique est généré ;
- le statut est « Nouveau ».

---

## AC-CRM-002 — Qualification d'un Lead

Given

Un Lead existe.

When

Le commercial le qualifie.

Then

- son statut devient « Qualifié » ;
- il peut être converti en Prospect.

---

## AC-CRM-003 — Conversion en Prospect

Given

Un Lead est qualifié.

When

Le commercial lance la conversion.

Then

- un Prospect est créé ;
- l'historique est conservé.

---

# Quotes

## AC-QUOTE-001 — Création d'un devis

Given

Une opportunité existe.

When

Le commercial crée un devis.

Then

- un numéro unique est attribué ;
- le devis est enregistré ;
- son statut est « Brouillon ».

---

## AC-QUOTE-002 — Acceptation d'un devis

Given

Le client consulte un devis.

When

Il accepte le devis.

Then

- le statut devient « Accepté » ;
- un contrat est généré ;
- un projet est créé automatiquement.

---

# Projects

## AC-PROJ-001 — Création d'un projet

Given

Un devis est accepté.

When

Le système traite la validation.

Then

- un projet est créé ;
- un chef de projet est affecté ;
- le client est associé.

---

## AC-PROJ-002 — Validation d'un livrable

Given

Un livrable est soumis.

When

Le client le valide.

Then

- le statut devient « Accepté » ;
- l'historique est mis à jour ;
- le chef de projet reçoit une notification.

---

# Client Portal

## AC-CLIENT-001 — Consultation d'un projet

Given

Le client est connecté.

When

Il ouvre un projet.

Then

- seules les données autorisées sont visibles ;
- les documents sont accessibles.

---

# CMS

## AC-CMS-001 — Publication d'un contenu

Given

Un contenu est prêt.

When

L'administrateur clique sur « Publier ».

Then

- le contenu devient public ;
- il est visible sur le site.

---

# Notifications

## AC-NOTIF-001 — Génération d'une notification

Given

Un événement métier est déclenché.

When

Le moteur de notifications traite l'événement.

Then

- une notification est créée ;
- elle est distribuée selon les préférences utilisateur.

---

# Settings

## AC-SET-001 — Invitation d'un utilisateur

Given

Un administrateur invite un utilisateur.

When

L'email est valide.

Then

- une invitation est envoyée ;
- un compte en attente est créé.

---

# 4. Traçabilité

Chaque Acceptance Criteria est relié à :

Acceptance Criteria

↓

Business Rule

↓

Functional Requirement

↓

Feature Specification

↓

User Story

↓

User Flow

↓

Cas de test

---

# 5. Références

- PRD
- MVP Definition
- Functional Requirements
- Business Rules
- Feature Specifications
- User Stories
- User Flows