# Persona — Administrateur

> Produit : Zawena Platform
>
> Version : 1.0
>
> Statut : Approuvé
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Objectif
2. Présentation
3. Profil
4. Responsabilités
5. Objectifs métier
6. Tableau de bord
7. Modules utilisés
8. Fréquence d'utilisation
9. Actions critiques
10. Permissions
11. Restrictions
12. Workflows métier
13. KPIs
14. Risques
15. Journalisation
16. Interactions avec les Agents IA
17. Appareils utilisés
18. Contexte d'utilisation
19. User Stories associées
20. User Flows associés
21. Critères de succès
22. Références

---

# 1. Objectif

L'Administrateur est responsable de la gestion opérationnelle quotidienne de Zawena Platform.

Il pilote les activités internes sans disposer des privilèges absolus réservés au Super Administrateur.

Il garantit le bon fonctionnement des opérations commerciales, des projets et des contenus.

---

# 2. Présentation

Nom du persona

Administrator

---

Type

Utilisateur interne

---

Authentification

Obligatoire

---

Accès

Back Office

---

Objectif principal

Administrer efficacement les opérations quotidiennes de Zawena.

---

# 3. Profil

L'Administrateur est un collaborateur permanent de Zawena.

Il possède une bonne connaissance :

- des services ;
- des clients ;
- des processus internes ;
- des outils numériques.

Il intervient quotidiennement sur la plateforme.

---

# 4. Responsabilités

L'Administrateur est chargé de :

- gérer les prospects ;
- gérer les clients ;
- gérer les devis ;
- gérer les projets ;
- publier les contenus du site ;
- suivre les indicateurs d'activité ;
- répondre aux demandes de contact ;
- superviser les notifications.

Il veille au bon déroulement des opérations sans intervenir sur l'infrastructure technique.

---

# 5. Objectifs métier

Ses objectifs sont :

- assurer un suivi efficace des prospects ;
- réduire les délais de traitement ;
- garantir la qualité des données ;
- maintenir le site internet à jour ;
- améliorer l'expérience client ;
- faciliter la collaboration interne.

---

# 6. Tableau de bord

Le tableau de bord Administrateur affiche notamment :

## Vue d'ensemble

- nouveaux prospects ;
- nouveaux clients ;
- devis en attente ;
- projets actifs ;
- tâches prioritaires ;
- notifications importantes.

---

## Indicateurs

- nombre de visiteurs ;
- taux de conversion ;
- devis envoyés ;
- projets en cours ;
- satisfaction client.

---

## Actions rapides

- Créer un devis
- Ajouter un client
- Publier un article
- Créer un projet
- Envoyer un message
- Planifier une réunion

---

# 7. Modules utilisés

L'Administrateur accède aux modules suivants :

- Dashboard
- CRM
- Clients
- Projets
- Devis
- CMS
- Blog
- Formulaires
- Notifications
- Calendrier
- Paramètres (partiels)

---

# 8. Fréquence d'utilisation

Dashboard

★★★★★

---

CRM

★★★★★

---

Devis

★★★★★

---

Projets

★★★★★

---

CMS

★★★★☆

---

Paramètres

★★☆☆☆

---

Rapports

★★★☆☆

---

# 9. Actions critiques

L'Administrateur peut :

- créer un client ;
- modifier un devis ;
- créer un projet ;
- clôturer un projet ;
- publier un article ;
- attribuer un projet ;
- répondre aux formulaires.

Toutes ces actions sont enregistrées dans les journaux d'audit.

---

# 10. Permissions

L'Administrateur peut :

✓ créer

✓ modifier

✓ archiver

✓ consulter

✓ exporter

✓ attribuer

✓ publier

---

Il ne peut pas :

✗ supprimer définitivement des données sensibles ;

✗ modifier les paramètres système critiques ;

✗ gérer les rôles globaux ;

✗ accéder aux secrets applicatifs ;

✗ modifier les paramètres de sécurité avancés.

---

# 11. Restrictions

Certaines opérations nécessitent la validation d'un Super Administrateur.

Exemples :

- suppression définitive d'un client ;
- suppression d'un projet ;
- modification des permissions globales ;
- désactivation d'un compte Administrateur ;
- restauration d'une sauvegarde.

---

# 12. Workflows métier

Les principaux workflows sont :

Prospect

↓

Qualification

↓

Devis

↓

Client

↓

Projet

↓

Livraison

↓

Suivi

---

Chaque étape est documentée dans les User Flows correspondants.

---

# 13. KPIs

L'Administrateur est évalué notamment sur :

- délai moyen de traitement des prospects ;
- délai d'envoi des devis ;
- taux de conversion ;
- nombre de projets suivis ;
- satisfaction client ;
- qualité des données CRM ;
- taux de résolution des demandes.

---

# 14. Risques

Une erreur de l'Administrateur peut entraîner :

- perte d'informations ;
- erreurs de facturation ;
- mauvaise communication ;
- retard projet ;
- mauvaise expérience client.

Certaines actions nécessitent donc une confirmation explicite.

---

# 15. Journalisation

Toutes les opérations sensibles sont enregistrées :

- création ;
- modification ;
- suppression ;
- export ;
- publication ;
- changement d'état.

Chaque journal contient :

- utilisateur ;
- date ;
- heure ;
- adresse IP ;
- action ;
- ressource concernée.

---

# 16. Interactions avec les Agents IA

L'Administrateur pourra utiliser un Agent IA pour :

- résumer les nouveaux prospects ;
- générer un devis initial ;
- proposer un planning de projet ;
- rédiger des réponses aux emails ;
- produire des comptes rendus de réunion ;
- générer des articles de blog ;
- analyser les KPIs.

L'IA agit comme un assistant.

La validation finale reste humaine.

---

# 17. Appareils utilisés

Principalement :

- ordinateur portable ;
- ordinateur de bureau.

Secondairement :

- smartphone.

---

# 18. Contexte d'utilisation

L'Administrateur travaille principalement :

- depuis les bureaux de Zawena ;
- en télétravail ;
- lors de rendez-vous clients ;
- pendant les heures ouvrées.

---

# 19. User Stories associées

Voir :

- user-stories/dashboard.md
- user-stories/crm.md
- user-stories/projects.md
- user-stories/cms.md
- user-stories/quotes.md

---

# 20. User Flows associés

Voir :

- user-flows/admin.md
- user-flows/project.md
- user-flows/quote.md
- user-flows/cms.md

---

# 21. Critères de succès

L'Administrateur est considéré comme performant lorsque :

- les prospects sont rapidement traités ;
- les devis sont envoyés dans les délais ;
- les projets sont correctement suivis ;
- les contenus restent à jour ;
- les clients disposent d'informations fiables ;
- les opérations sont réalisées sans erreur majeure.

---

# 22. Références

Documents associés :

- 04-personas.md
- docs/architecture/permissions.md
- docs/architecture/auth.md
- docs/security/access-control.md
- features/dashboard.md
- features/crm.md
- features/projects.md
- features/cms.md

---