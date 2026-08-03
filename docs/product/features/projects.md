# Feature Specification — Projects

> Produit : Zawena Platform
>
> Module : Projects
>
> Identifiant : FEATURE-PROJECTS
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
3. Vision du module
4. Valeur métier
5. Personas concernés
6. Architecture du projet
7. Phases du projet
8. Jalons (Milestones)
9. Tâches et sous-tâches
10. Livrables
11. Documents
12. Discussions
13. Activités
14. Vues disponibles
15. Fonctionnalités MVP
16. Fonctionnalités futures
17. États
18. Règles métier
19. Permissions
20. Notifications
21. Journalisation
22. Modèle de données
23. APIs
24. Sécurité
25. Performance
26. Critères d'acceptation
27. Limites MVP
28. Roadmap
29. Références

---

# 1. Objectif

Le module Projects permet de planifier, organiser, exécuter, suivre et clôturer les projets réalisés par Zawena pour ses clients.

Il constitue le centre opérationnel de l'entreprise.

Chaque projet rassemble l'ensemble des informations, documents, tâches, livrables et échanges nécessaires à sa bonne exécution.

---

# 2. Vue d'ensemble

Le module Projects transforme une opportunité commerciale validée en un projet structuré.

Il permet :

- d'organiser le travail ;
- d'affecter les ressources ;
- de suivre l'avancement ;
- de communiquer avec les équipes ;
- de centraliser la documentation ;
- de préparer la livraison.

---

# 3. Vision du module

Chaque projet représente une source unique de vérité.

Toutes les informations liées à un projet doivent être accessibles depuis une seule interface.

Le projet devient le point central de collaboration entre les équipes internes, les clients et les partenaires autorisés.

---

# 4. Valeur métier

Le module Projects permet :

- de respecter les délais ;
- d'améliorer la qualité des livrables ;
- de réduire les pertes d'information ;
- de suivre la progression ;
- d'améliorer la satisfaction client ;
- de standardiser les méthodes de travail.

---

# 5. Personas concernés

Principaux :

- Project Manager
- Developer
- Administrator

Secondaires :

- Client
- Support
- Partner
- Super Administrator

---

# 6. Architecture du projet

Chaque projet comprend :

- Informations générales
- Équipe
- Phases
- Jalons
- Tâches
- Sous-tâches
- Livrables
- Documents
- Discussions
- Activités
- Historique

Les futures versions pourront intégrer :

- Budget
- Temps passé
- Ressources
- Facturation
- Gestion des risques
- Dépendances
- Sprint Planning

---

# 7. Phases du projet

Cycle de vie standard :

Création

↓

Kick-off

↓

Analyse

↓

Conception

↓

Développement

↓

Tests

↓

Validation

↓

Déploiement

↓

Formation

↓

Support

↓

Clôture

Toutes les phases ne sont pas obligatoires pour chaque projet.

---

# 8. Jalons (Milestones)

Les jalons représentent les étapes importantes.

Exemples :

- Kick-off terminé
- Analyse validée
- Maquettes validées
- Développement terminé
- Tests validés
- Déploiement réalisé
- Formation effectuée
- Projet clôturé

Chaque jalon possède :

- un responsable ;
- une date prévue ;
- une date réelle ;
- un statut.

---

# 9. Tâches et sous-tâches

Une tâche appartient à :

Projet

↓

Phase

↓

Tâche

↓

Sous-tâche

Chaque tâche possède :

- titre ;
- description ;
- responsable ;
- priorité ;
- statut ;
- échéance.

Priorités :

- Faible
- Normale
- Haute
- Critique

---

# 10. Livrables

Les livrables représentent les résultats attendus.

Exemples :

- Site web
- Application
- Documentation
- Rapport d'audit
- Formation
- Code source
- API
- Maquette

Chaque livrable peut être :

- En préparation
- Soumis
- En validation
- Validé
- Rejeté

---

# 11. Documents

Le projet centralise tous les documents :

- Contrat
- Devis
- Cahier des charges
- Architecture
- Documentation
- Rapports
- Livrables
- Comptes rendus

Les documents sont versionnés dans les futures versions.

---

# 12. Discussions

Chaque projet dispose d'un espace d'échange.

Les discussions permettent :

- commentaires ;
- mentions ;
- pièces jointes ;
- suivi des décisions.

Toutes les discussions sont liées au projet.

---

# 13. Activités

Toutes les actions importantes alimentent une timeline.

Exemples :

- Projet créé
- Tâche ajoutée
- Tâche terminée
- Document ajouté
- Livrable validé
- Projet clôturé

---

# 14. Vues disponibles

Le module propose plusieurs représentations :

MVP :

- Liste
- Kanban
- Calendrier

Versions futures :

- Timeline
- Gantt
- Tableau
- Charge équipe
- Portfolio

---

# 15. Fonctionnalités MVP

Le MVP permet :

- créer un projet ;
- modifier un projet ;
- attribuer une équipe ;
- créer des tâches ;
- gérer les jalons ;
- partager des documents ;
- suivre l'avancement ;
- clôturer un projet.

---

# 16. Fonctionnalités futures

Évolutions prévues :

- gestion budgétaire ;
- suivi du temps ;
- dépendances entre tâches ;
- gestion des risques ;
- gestion des ressources ;
- sprint planning ;
- gestion multi-projets ;
- tableaux de bord avancés.

---

# 17. États

Projet :

- Brouillon
- Actif
- Suspendu
- Terminé
- Archivé

Tâche :

- À faire
- En cours
- Bloquée
- Terminée

Livrable :

- En préparation
- En validation
- Validé
- Rejeté

---

# 18. Règles métier

## BR-PROJ-001

Un projet provient d'une opportunité gagnée ou d'un contrat validé.

---

## BR-PROJ-002

Chaque projet possède un Chef de Projet.

---

## BR-PROJ-003

Un projet est associé à un seul client.

---

## BR-PROJ-004

Chaque tâche possède un responsable.

---

## BR-PROJ-005

La clôture d'un projet nécessite la validation des livrables obligatoires.

---

## BR-PROJ-006

Toutes les modifications importantes sont historisées.

---

# 19. Permissions

Project Manager

- gestion complète des projets.

Developer

- gestion des tâches attribuées ;
- consultation des projets.

Client

- consultation des projets autorisés ;
- validation des livrables.

Support

- consultation ;
- suivi post-livraison.

Administrator

- gestion globale.

Super Administrator

- accès complet.

---

# 20. Notifications

Des notifications sont envoyées lors :

- création d'un projet ;
- attribution d'une tâche ;
- échéance proche ;
- validation d'un livrable ;
- changement de statut ;
- clôture.

---

# 21. Journalisation

Les événements enregistrés comprennent :

- création ;
- modification ;
- suppression logique ;
- changement de statut ;
- validation ;
- attribution ;
- clôture.

---

# 22. Modèle de données

Entités principales :

Projet

↓

Phase

↓

Jalon

↓

Tâche

↓

Sous-tâche

↓

Livrable

↓

Document

↓

Discussion

↓

Activité

Le détail du modèle est défini dans :

docs/architecture/database.md

---

# 23. APIs

Exemples :

GET /projects

GET /projects/{id}

POST /projects

PATCH /projects/{id}

DELETE /projects/{id}

POST /projects/{id}/tasks

POST /projects/{id}/milestones

POST /projects/{id}/deliverables

---

# 24. Sécurité

Le module applique :

- RBAC ;
- contrôle d'accès par projet ;
- journalisation ;
- validation des entrées ;
- protection des documents.

---

# 25. Performance

Objectifs :

- ouverture rapide d'un projet ;
- affichage fluide des tâches ;
- recherche rapide ;
- pagination ;
- chargement progressif.

---

# 26. Critères d'acceptation

Le module est validé lorsque :

✓ un projet peut être créé ;

✓ des tâches peuvent être attribuées ;

✓ les jalons sont suivis ;

✓ les livrables sont gérés ;

✓ les documents sont centralisés ;

✓ les rôles sont respectés ;

✓ l'historique est disponible.

---

# 27. Limites MVP

Le MVP ne comprend pas :

- gestion budgétaire ;
- suivi du temps ;
- Gantt ;
- gestion des risques ;
- portefeuille de projets ;
- IA de planification.

---

# 28. Roadmap

V2

- Gantt
- Time Tracking
- Budget
- Ressources
- Dépendances
- Sprint Planning

---

V3

- AI Project Manager
- Détection automatique des risques
- Planification intelligente
- Rapports automatiques
- Prévision des retards

---

V4

- Multi-portefeuille
- Capacity Planning
- Resource Optimizer
- Digital Twin Project

---

# 29. Références

- docs/product/personas/project-manager.md
- docs/product/personas/developer.md
- docs/product/features/03-crm.md
- docs/product/features/07-quotes.md
- docs/architecture/database.md
- docs/architecture/api.md
- docs/security/access-control.md

---