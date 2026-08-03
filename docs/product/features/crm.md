# Feature Specification — CRM (Customer Relationship Management)

> Produit : Zawena Platform
>
> Module : CRM
>
> Identifiant : FEATURE-CRM
>
> Version : 1.0
>
> Statut : Approuvé pour MVP
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Objectif
2. Vue d'ensemble
3. Vision du CRM
4. Valeur métier
5. Personas concernés
6. Architecture métier
7. Cas d'utilisation
8. Fonctionnalités
9. Pipeline commercial
10. Cycle de vie d'une opportunité
11. Écrans
12. Composants UI
13. États
14. Règles métier
15. Permissions
16. Notifications
17. Journalisation
18. Modèle de données
19. APIs
20. Sécurité
21. Performance
22. Accessibilité
23. Responsive
24. KPIs
25. Limites MVP
26. Roadmap V2
27. Références

---

# 1. Objectif

Le CRM est le cœur commercial de Zawena Platform.

Il centralise toutes les interactions entre Zawena et ses prospects, clients et partenaires afin d'assurer un suivi cohérent du premier contact jusqu'à la fidélisation.

Le CRM doit fournir une vision complète de chaque relation commerciale et permettre une collaboration fluide entre les équipes.

---

# 2. Vue d'ensemble

Le CRM n'est pas une simple base de contacts.

Il constitue une plateforme de gestion des relations commerciales permettant de :

- suivre les prospects ;
- gérer les entreprises ;
- gérer les contacts ;
- suivre les opportunités ;
- enregistrer les interactions ;
- produire des devis ;
- déclencher la création de projets ;
- mesurer les performances commerciales.

---

# 3. Vision du CRM

Le CRM est conçu autour des opportunités.

Structure métier :

Entreprise

↓

Contacts

↓

Opportunités

↓

Projet

↓

Client actif

Une même entreprise peut posséder :

- plusieurs contacts ;
- plusieurs opportunités ;
- plusieurs devis ;
- plusieurs projets.

Cette architecture permet d'accompagner une croissance importante sans refonte du modèle de données.

---

# 4. Valeur métier

Le CRM permet à Zawena de :

- suivre chaque opportunité ;
- améliorer le taux de conversion ;
- éviter la perte d'informations ;
- faciliter le travail des commerciaux ;
- fournir une vision commune à toutes les équipes ;
- préparer la vente des futurs SaaS.

---

# 5. Personas concernés

## Principaux

- Sales
- Administrator
- Super Administrator

## Secondaires

- Project Manager
- Support

---

# 6. Architecture métier

Le CRM est organisé autour des modules suivants.

## MVP

- Entreprises
- Contacts
- Prospects
- Opportunités
- Pipeline
- Activités
- Notes
- Historique
- Devis

---

## Évolutions futures

- Appels
- Emails
- Réunions
- Contrats
- Facturation
- Renouvellements
- Produits SaaS
- Abonnements
- Commissions
- IA commerciale

---

# 7. Cas d'utilisation

UC-CRM-001

Créer une entreprise.

---

UC-CRM-002

Créer un contact.

---

UC-CRM-003

Créer une opportunité.

---

UC-CRM-004

Déplacer une opportunité dans le pipeline.

---

UC-CRM-005

Ajouter une activité.

---

UC-CRM-006

Ajouter une note.

---

UC-CRM-007

Créer un devis.

---

UC-CRM-008

Transformer une opportunité gagnée en projet.

---

UC-CRM-009

Consulter l'historique complet d'une relation commerciale.

---

# 8. Fonctionnalités

Le CRM comprend notamment :

## Gestion des entreprises

- création ;
- modification ;
- archivage ;
- recherche.

---

## Gestion des contacts

- informations personnelles ;
- fonction ;
- téléphone ;
- email ;
- entreprise associée.

---

## Gestion des prospects

- qualification ;
- origine ;
- secteur ;
- taille ;
- besoins.

---

## Gestion des opportunités

- montant estimé ;
- probabilité ;
- responsable ;
- statut ;
- échéance.

---

## Activités

- appels ;
- emails ;
- réunions ;
- tâches ;
- relances.

(MVP : activités manuelles)

---

## Notes

Chaque opportunité peut contenir un nombre illimité de notes horodatées.

---

## Historique

Toutes les interactions sont regroupées dans une timeline.

---

## Devis

Création et suivi des devis associés aux opportunités.

---

# 9. Pipeline commercial

Étapes par défaut :

Nouveau Prospect

↓

Qualification

↓

Analyse du besoin

↓

Proposition

↓

Négociation

↓

Gagnée

↓

Projet

ou

Perdue

Chaque étape possède ses propres règles métier.

---

# 10. Cycle de vie d'une opportunité

Création

↓

Qualification

↓

Premier échange

↓

Analyse

↓

Proposition

↓

Réunion

↓

Négociation

↓

Décision

↓

Projet créé

↓

Archivage

---

# 11. Écrans

Le CRM comprend notamment :

- Dashboard CRM
- Liste des entreprises
- Fiche entreprise
- Liste des contacts
- Fiche contact
- Pipeline
- Opportunités
- Fiche opportunité
- Activités
- Notes
- Historique
- Devis

---

# 12. Composants UI

- CRM Layout
- Pipeline Kanban
- Opportunity Card
- Company Card
- Contact Card
- Timeline
- Activity Card
- Notes
- Search Bar
- Filters
- KPI Cards
- Empty State
- Loading State

---

# 13. États

Une opportunité peut être :

- Nouveau
- Qualifié
- En cours
- Proposition envoyée
- Négociation
- Gagnée
- Perdue
- Archivée

---

# 14. Règles métier

## BR-CRM-001

Une opportunité appartient toujours à une entreprise.

---

## BR-CRM-002

Une opportunité possède un responsable.

---

## BR-CRM-003

Une opportunité gagnée peut créer automatiquement un projet après validation.

---

## BR-CRM-004

Les changements de statut sont historisés.

---

## BR-CRM-005

Une opportunité perdue ne peut être supprimée.

Elle est archivée.

---

## BR-CRM-006

Chaque activité est horodatée.

---

# 15. Permissions

Sales

- créer
- modifier
- consulter

---

Administrator

- accès complet au CRM

---

Super Administrator

- accès global

---

Support

- consultation limitée

---

Project Manager

- consultation des opportunités devenues projets

---

# 16. Notifications

Le CRM peut générer des notifications lors :

- création d'une opportunité ;
- changement de statut ;
- nouveau devis ;
- relance programmée ;
- signature d'un contrat ;
- création automatique d'un projet.

---

# 17. Journalisation

Les événements suivants sont enregistrés :

- création ;
- modification ;
- changement de statut ;
- création de devis ;
- suppression logique ;
- attribution d'un responsable.

---

# 18. Modèle de données

Le CRM repose principalement sur les entités suivantes.

Entreprise

↓

Contact

↓

Opportunité

↓

Activité

↓

Note

↓

Devis

↓

Projet

Chaque entité est documentée dans :

docs/architecture/database.md

---

# 19. APIs

Exemples :

GET /crm/companies

GET /crm/contacts

GET /crm/opportunities

POST /crm/opportunities

PATCH /crm/opportunities/{id}

POST /crm/activities

POST /crm/notes

POST /crm/quotes

---

# 20. Sécurité

Le CRM applique :

- contrôle d'accès basé sur les rôles (RBAC) ;
- journalisation des actions sensibles ;
- validation des données côté serveur ;
- protection contre les accès non autorisés ;
- séparation logique des données selon les permissions.

---

# 21. Performance

Le CRM doit permettre :

- la recherche rapide ;
- le filtrage instantané ;
- la pagination ;
- le chargement progressif ;
- l'affichage fluide des pipelines contenant plusieurs centaines d'opportunités.

---

# 22. Accessibilité

Le module respecte les standards définis dans :

docs/design-system/accessibility.md

---

# 23. Responsive

Le CRM est optimisé pour :

- Desktop (prioritaire)
- Laptop
- Tablette

Le support mobile sera limité au MVP.

---

# 24. KPIs

Les principaux indicateurs comprennent :

Commercial

- taux de conversion ;
- valeur du pipeline ;
- chiffre d'affaires prévisionnel ;
- nombre de devis.

---

Performance

- délai moyen de qualification ;
- durée moyenne du cycle commercial ;
- temps de réponse.

---

Qualité

- taux de perte ;
- satisfaction client ;
- données incomplètes.

---

# 25. Limites MVP

Le MVP ne comprend pas :

- synchronisation email ;
- appels VoIP ;
- automatisation complète ;
- scoring IA ;
- prévisions commerciales ;
- abonnements SaaS ;
- commissions ;
- marketplace partenaires.

---

# 26. Roadmap V2

Le CRM évoluera avec :

- AI Sales Assistant ;
- génération automatique des devis ;
- suivi automatique des emails ;
- transcription des réunions ;
- prévision du chiffre d'affaires ;
- scoring automatique des opportunités ;
- workflows commerciaux automatisés ;
- synchronisation avec Microsoft 365 et Google Workspace ;
- gestion des abonnements SaaS ;
- portail commercial.

---

# 27. Références

- docs/product/personas/sales.md
- docs/product/personas/project-manager.md
- docs/company/services.md
- docs/company/pricing-strategy.md
- docs/architecture/database.md
- docs/architecture/api.md
- docs/architecture/permissions.md
- docs/security/access-control.md

---