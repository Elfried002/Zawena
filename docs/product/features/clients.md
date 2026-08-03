# Feature Specification — Client Portal

> Produit : Zawena Platform
>
> Module : Clients
>
> Identifiant : FEATURE-CLIENTS
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
3. Vision du portail
4. Valeur métier
5. Personas concernés
6. Architecture fonctionnelle
7. Fonctionnalités MVP
8. Fonctionnalités futures
9. Tableau de bord client
10. Mes projets
11. Mes devis
12. Mes contrats
13. Mes documents
14. Support
15. États
16. Règles métier
17. Permissions
18. Notifications
19. Journalisation
20. Modèle de données
21. APIs
22. Sécurité
23. Performance
24. Critères d'acceptation
25. Limites MVP
26. Roadmap
27. Références

---

# 1. Objectif

Le Client Portal offre aux clients un espace sécurisé leur permettant de suivre leurs projets, consulter leurs documents et interagir avec Zawena.

Il améliore la transparence, réduit les échanges dispersés et centralise toutes les informations utiles.

---

# 2. Vue d'ensemble

Chaque client dispose d'un espace personnel accessible après authentification.

Le portail regroupe les informations commerciales, contractuelles et opérationnelles qui concernent exclusivement ce client.

---

# 3. Vision du portail

Le portail est organisé autour des éléments suivants :

- Dashboard
- Mes projets
- Mes devis
- Mes contrats
- Mes documents
- Support
- Notifications
- Profil

---

# 4. Valeur métier

Le portail permet :

- d'améliorer l'expérience client ;
- de renforcer la transparence ;
- de réduire les demandes répétitives ;
- de faciliter la collaboration ;
- de valoriser les prestations de Zawena.

---

# 5. Personas concernés

Principaux :

- Client

Secondaires :

- Support
- Project Manager
- Administrator

---

# 6. Architecture fonctionnelle

Le portail agrège les données provenant de plusieurs modules :

- Projects
- Quotes
- Documents
- Notifications
- Authentication

---

# 7. Fonctionnalités MVP

Le MVP permet de :

- consulter les projets ;
- suivre les jalons ;
- consulter les devis ;
- télécharger les documents ;
- consulter les notifications ;
- gérer son profil.

---

# 8. Fonctionnalités futures

Les évolutions prévues comprennent :

- support intégré ;
- signature électronique ;
- paiement en ligne ;
- messagerie sécurisée ;
- chat temps réel ;
- espace de formation ;
- gestion des abonnements SaaS ;
- AI Client Assistant.

---

# 9. Tableau de bord client

Le Dashboard présente :

- projets actifs ;
- avancement global ;
- derniers documents ;
- notifications récentes ;
- prochains jalons.

---

# 10. Mes projets

Le client peut :

- consulter les informations du projet ;
- suivre les étapes ;
- consulter les livrables ;
- visualiser les jalons ;
- suivre l'avancement.

---

# 11. Mes devis

Le portail affiche :

- devis en cours ;
- devis acceptés ;
- devis refusés ;
- historique.

---

# 12. Mes contrats

Le client peut consulter :

- contrats ;
- avenants ;
- documents associés.

---

# 13. Mes documents

Le portail centralise :

- cahier des charges ;
- documentation ;
- guides ;
- rapports ;
- livrables.

---

# 14. Support

Le MVP affiche les coordonnées et les moyens de contact.

Les tickets seront intégrés en V2.

---

# 15. États

Projet :

- En cours
- Suspendu
- Terminé

Document :

- Disponible
- Archivé

---

# 16. Règles métier

## BR-CLIENT-001

Un client ne peut consulter que les données de son organisation.

## BR-CLIENT-002

Les documents sensibles sont accessibles uniquement aux utilisateurs autorisés.

## BR-CLIENT-003

Les livrables validés sont conservés dans l'historique.

---

# 17. Permissions

Le client peut :

- consulter ;
- télécharger ;
- mettre à jour son profil.

Il ne peut pas modifier les données métier.

---

# 18. Notifications

Le portail informe le client lors :

- d'un nouveau document ;
- d'un changement de statut du projet ;
- d'un nouveau devis ;
- d'un livrable soumis.

---

# 19. Journalisation

Sont enregistrés :

- connexions ;
- téléchargements ;
- validations de livrables ;
- modifications du profil.

---

# 20. Modèle de données

Entités principales :

- Client
- Project
- Document
- Quote
- Contract
- Notification

Les détails sont décrits dans :

docs/architecture/database.md

---

# 21. APIs

Exemples :

GET /client/dashboard

GET /client/projects

GET /client/quotes

GET /client/documents

GET /client/contracts

PATCH /client/profile

---

# 22. Sécurité

Le portail applique :

- authentification obligatoire ;
- RBAC ;
- isolation des données par organisation ;
- journalisation des accès.

---

# 23. Performance

Le portail doit :

- charger rapidement ;
- afficher les documents efficacement ;
- permettre des téléchargements fiables.

---

# 24. Critères d'acceptation

Le module est validé lorsque :

✓ un client peut accéder à son portail ;

✓ seuls ses projets sont visibles ;

✓ les documents sont téléchargeables ;

✓ les notifications sont affichées ;

✓ les permissions sont correctement appliquées.

---

# 25. Limites MVP

Le MVP ne comprend pas :

- paiement en ligne ;
- tickets de support ;
- chat ;
- signature électronique ;
- AI Client Assistant.

---

# 26. Roadmap

V2

- Support
- Signature électronique
- Paiement
- Messagerie

V3

- AI Client Assistant
- Centre de formation
- Gestion des licences
- Marketplace

---

# 27. Références

- docs/product/features/06-projects.md
- docs/product/features/07-quotes.md
- docs/product/features/09-notifications.md
- docs/architecture/database.md
- docs/architecture/api.md

---