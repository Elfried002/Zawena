# Business Rules — Zawena Platform

> Produit : Zawena Platform
>
> Document : Business Rules
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
3. Classification des règles métier
4. Business Rules
5. Priorité des règles
6. Gestion des exceptions
7. Traçabilité
8. Références

---

# 1. Objectif

Ce document centralise toutes les règles métier de Zawena Platform.

Une règle métier définit une contrainte, une obligation ou un comportement que le système doit respecter pour garantir le bon fonctionnement des processus métier.

Les Business Rules sont indépendantes de l'interface utilisateur et s'appliquent à tous les modules.

---

# 2. Portée

Les règles métier couvrent :

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

# 3. Classification des règles métier

Les règles sont regroupées par domaine.

Format :

BR-XXX-YYY

Exemple :

BR-CRM-001

BR-PROJ-015

BR-SET-004

---

# 4. Business Rules

# Website

## BR-WEB-001

Toute demande de contact doit créer un Lead dans le CRM.

Priorité : Critique

---

## BR-WEB-002

Toute demande de devis doit être associée à un prospect.

---

## BR-WEB-003

Les formulaires ne peuvent être soumis que si les champs obligatoires sont renseignés.

---

# Authentication

## BR-AUTH-001

Un utilisateur doit posséder un compte actif pour se connecter.

---

## BR-AUTH-002

Une session expirée interdit tout accès aux ressources protégées.

---

## BR-AUTH-003

Chaque utilisateur possède un rôle principal.

---

## BR-AUTH-004

Toutes les permissions sont déterminées par le rôle attribué.

---

# CRM

## BR-CRM-001

Chaque Lead possède un identifiant unique.

---

## BR-CRM-002

Un Lead qualifié devient Prospect.

---

## BR-CRM-003

Un Prospect peut être converti en Entreprise.

---

## BR-CRM-004

Une Opportunité est toujours liée à une Entreprise.

---

## BR-CRM-005

Une Opportunité possède un seul statut actif.

---

## BR-CRM-006

Une Opportunité gagnée autorise la création d'un devis.

---

## BR-CRM-007

Une Opportunité perdue ne peut plus évoluer dans le pipeline sans réouverture.

---

## BR-CRM-008

Toutes les activités commerciales doivent être historisées.

---

# Quotes

## BR-QUOTE-001

Un devis doit être associé à une Opportunité.

---

## BR-QUOTE-002

Le numéro de devis est unique.

---

## BR-QUOTE-003

Les montants sont recalculés automatiquement après chaque modification.

---

## BR-QUOTE-004

Un devis accepté ne peut plus être modifié.

---

## BR-QUOTE-005

Un devis refusé est archivé.

---

## BR-QUOTE-006

Un devis accepté déclenche automatiquement la création d'un contrat.

---

## BR-QUOTE-007

Un contrat validé déclenche automatiquement la création d'un projet.

---

# Projects

## BR-PROJ-001

Chaque projet appartient à un seul client.

---

## BR-PROJ-002

Chaque projet possède un chef de projet.

---

## BR-PROJ-003

Une tâche est assignée à un seul responsable.

---

## BR-PROJ-004

Une tâche ne peut être clôturée que si toutes ses sous-tâches sont terminées.

---

## BR-PROJ-005

Un livrable doit être validé ou refusé par le client.

---

## BR-PROJ-006

Un projet terminé passe automatiquement au statut « À archiver ».

---

## BR-PROJ-007

Toutes les modifications importantes sont historisées.

---

# Client Portal

## BR-CLIENT-001

Le client ne peut consulter que ses propres projets.

---

## BR-CLIENT-002

Le client ne peut télécharger que les documents qui lui sont autorisés.

---

## BR-CLIENT-003

Chaque validation d'un livrable est enregistrée.

---

# CMS

## BR-CMS-001

Un contenu publié est visible immédiatement sur le site.

---

## BR-CMS-002

Un contenu archivé n'est plus visible publiquement.

---

## BR-CMS-003

Chaque contenu possède un auteur.

---

## BR-CMS-004

Chaque modification crée une nouvelle version.

---

# Notifications

## BR-NOTIF-001

Chaque événement métier peut générer une notification.

---

## BR-NOTIF-002

Les préférences utilisateur déterminent les canaux de diffusion.

---

## BR-NOTIF-003

Une notification lue reste disponible dans l'historique.

---

# Settings

## BR-SET-001

Seuls les administrateurs autorisés peuvent modifier les paramètres globaux.

---

## BR-SET-002

Toute modification des paramètres critiques est journalisée.

---

## BR-SET-003

Les rôles déterminent les permissions disponibles.

---

## BR-SET-004

Une intégration ne peut être activée qu'après validation de sa configuration.

---

# 5. Priorité des règles

Les règles sont classées selon leur importance.

Critique

Le système ne peut pas fonctionner sans cette règle.

Élevée

La règle est indispensable au fonctionnement métier.

Moyenne

La règle améliore le fonctionnement.

Faible

La règle apporte un confort d'utilisation.

---

# 6. Gestion des exceptions

Toute exception à une règle métier doit :

- être documentée ;
- être justifiée ;
- être validée par le Product Owner ;
- être tracée dans le journal d'audit lorsque nécessaire.

---

# 7. Traçabilité

Chaque Business Rule doit être reliée à :

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

Acceptance Criteria

↓

Cas de test

---

# 8. Références

- PRD
- MVP Definition
- Functional Requirements
- Non-Functional Requirements
- Feature Specifications
- User Stories
- User Flows
- Acceptance Criteria