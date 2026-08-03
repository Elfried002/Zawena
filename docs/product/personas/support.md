# Persona — Support Client (Support)

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
8. Outils utilisés
9. Capabilities
10. Fréquence d'utilisation
11. Actions critiques
12. Permissions
13. Restrictions
14. Workflows métier
15. KPIs
16. Risques
17. Journalisation
18. Agents IA utilisés
19. Modules futurs
20. Appareils utilisés
21. Contexte d'utilisation
22. User Stories associées
23. User Flows associés
24. Critères de succès
25. Références

---

# 1. Objectif

Le Support Client accompagne les clients avant, pendant et après la livraison d'un projet.

Il est chargé de répondre aux demandes d'assistance, d'assurer le suivi des incidents et de garantir une expérience client de qualité.

Le Support constitue le principal point de contact opérationnel entre les clients et Zawena après la mise en production.

---

# 2. Présentation

Nom du persona

Support

---

Type

Utilisateur interne

---

Authentification

Obligatoire

---

Accès

Support & Assistance

---

Objectif principal

Résoudre rapidement les demandes des clients tout en garantissant leur satisfaction.

---

# 3. Profil

Le Support possède :

- une excellente communication ;
- une bonne compréhension des produits Zawena ;
- une capacité d'analyse ;
- un sens du service client.

Il travaille quotidiennement avec :

- les clients ;
- les chefs de projet ;
- les développeurs ;
- les administrateurs.

---

# 4. Responsabilités

Le Support est responsable de :

- traiter les tickets ;
- répondre aux demandes clients ;
- qualifier les incidents ;
- suivre leur résolution ;
- maintenir la base de connaissances ;
- escalader les incidents critiques ;
- accompagner les utilisateurs.

---

# 5. Objectifs métier

Le Support cherche à :

- réduire les délais de réponse ;
- améliorer la satisfaction client ;
- résoudre les incidents dès le premier contact lorsque c'est possible ;
- maintenir une documentation à jour.

---

# 6. Tableau de bord

Le tableau de bord présente :

## Vue générale

- tickets ouverts ;
- tickets critiques ;
- tickets en attente ;
- tickets résolus aujourd'hui ;
- nouveaux messages ;
- SLA en cours.

---

## Indicateurs

- temps moyen de première réponse ;
- temps moyen de résolution ;
- satisfaction client ;
- volume de tickets ;
- incidents par catégorie.

---

## Actions rapides

- Créer un ticket
- Répondre à un client
- Escalader un incident
- Partager un document
- Clôturer un ticket

---

# 7. Modules utilisés

Le Support utilise :

- Dashboard
- Tickets
- Clients
- Base de connaissances
- Documents
- Notifications
- CRM (lecture)
- Rapports

---

# 8. Outils utilisés

Le Support travaille principalement avec :

- Gestion des tickets
- Base de connaissances
- Chat
- Email
- Tableau de bord
- Historique client

---

# 9. Capabilities

Le Support possède les capacités suivantes :

- Ticket Management
- Incident Management
- Customer Communication
- Knowledge Base Management
- Documentation
- Escalation Management

---

# 10. Fréquence d'utilisation

Tickets

★★★★★

---

Dashboard

★★★★★

---

Base de connaissances

★★★★☆

---

CRM

★★★☆☆

---

Rapports

★★★☆☆

---

# 11. Actions critiques

Le Support peut :

- créer un ticket ;
- modifier un ticket ;
- attribuer un ticket ;
- escalader un incident ;
- clôturer un ticket ;
- publier un article dans la base de connaissances (selon permissions).

Toutes ces actions sont journalisées.

---

# 12. Permissions

Le Support peut :

✓ consulter les informations des clients liées à un ticket ;

✓ répondre aux tickets ;

✓ consulter l'historique des échanges ;

✓ créer des articles de documentation ;

✓ consulter les rapports de support.

---

# 13. Restrictions

Le Support ne peut pas :

✗ modifier les paramètres système ;

✗ supprimer un client ;

✗ modifier les rôles ;

✗ accéder aux secrets applicatifs ;

✗ intervenir directement sur l'infrastructure.

---

# 14. Workflows métier

Création d'un ticket

↓

Qualification

↓

Analyse

↓

Résolution

↓

Validation client

↓

Clôture

↓

Mise à jour de la base de connaissances

---

# 15. KPIs

Le Support est évalué sur :

- temps moyen de première réponse ;
- temps moyen de résolution ;
- taux de résolution au premier contact ;
- satisfaction client (CSAT) ;
- respect des SLA.

---

# 16. Risques

Les principaux risques sont :

- mauvaise qualification des incidents ;
- délais de réponse élevés ;
- communication insuffisante ;
- perte de confiance du client.

---

# 17. Journalisation

Les actions enregistrées comprennent :

- création de ticket ;
- changement de statut ;
- réponse envoyée ;
- escalade ;
- clôture ;
- consultation d'informations sensibles.

---

# 18. Agents IA utilisés

Le Support pourra utiliser :

- AI Support Assistant
- AI Ticket Classifier
- AI Knowledge Assistant
- AI Response Generator
- AI Incident Summarizer
- AI Translation Assistant

Les réponses proposées par les Agents IA sont toujours validées avant envoi.

---

# 19. Modules futurs

Les futures versions intégreront :

- Portail client de support
- Chat temps réel
- Assistant vocal
- Détection automatique des incidents
- SLA avancés
- Centre d'aide intelligent

---

# 20. Appareils utilisés

Principalement :

- ordinateur portable ;
- ordinateur de bureau.

---

# 21. Contexte d'utilisation

Le Support intervient :

- pendant les heures d'ouverture ;
- lors des mises en production ;
- lors d'incidents ;
- dans le cadre du suivi client.

---

# 22. User Stories associées

Voir :

- user-stories/support.md
- user-stories/tickets.md
- user-stories/knowledge-base.md

---

# 23. User Flows associés

Voir :

- user-flows/support.md
- user-flows/ticket.md
- user-flows/incident.md

---

# 24. Critères de succès

Le Support atteint ses objectifs lorsque :

- les tickets sont résolus rapidement ;
- les clients sont satisfaits ;
- les SLA sont respectés ;
- les connaissances sont documentées ;
- les incidents récurrents diminuent.

---

# 25. Références

Documents associés :

- docs/architecture/permissions.md
- docs/security/access-control.md
- features/notifications.md
- features/clients.md
- features/dashboard.md

---