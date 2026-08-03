# Feature Specification — Quotes (Gestion des Devis)

> Produit : Zawena Platform
>
> Module : Quotes
>
> Identifiant : FEATURE-QUOTES
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
6. Cycle de vie d'un devis
7. Structure d'un devis
8. Fonctionnalités MVP
9. Fonctionnalités futures
10. États
11. Règles métier
12. Permissions
13. Notifications
14. Journalisation
15. Modèle de données
16. APIs
17. Sécurité
18. Performance
19. Critères d'acceptation
20. Limites MVP
21. Roadmap
22. Références

---

# 1. Objectif

Le module Quotes permet de créer, gérer, suivre et transformer les devis commerciaux de Zawena.

Il constitue le lien entre le CRM et les projets.

Chaque devis formalise une proposition commerciale adaptée aux besoins du prospect ou du client.

---

# 2. Vue d'ensemble

Le module centralise toutes les propositions commerciales.

Il permet de :

- créer des devis ;
- gérer plusieurs versions ;
- suivre leur statut ;
- transformer un devis accepté en contrat puis en projet.

---

# 3. Vision du module

Le devis est un objet métier complet.

Il est toujours lié à :

- une entreprise ;
- un contact ;
- une opportunité ;
- un responsable commercial.

---

# 4. Valeur métier

Le module permet de :

- standardiser les propositions commerciales ;
- accélérer le traitement des demandes ;
- réduire les erreurs ;
- suivre les négociations ;
- améliorer le taux de conversion.

---

# 5. Personas concernés

Principaux :

- Sales
- Administrator

Secondaires :

- Project Manager
- Client
- Super Administrator

---

# 6. Cycle de vie d'un devis

Opportunité

↓

Brouillon

↓

Validation interne

↓

Envoyé

↓

Consulté

↓

Négociation

↓

Accepté

↓

Contrat

↓

Projet

ou

Refusé

↓

Archivé

---

# 7. Structure d'un devis

Chaque devis comprend :

- numéro unique ;
- client ;
- entreprise ;
- opportunité associée ;
- version ;
- lignes de prestations ;
- options ;
- montant HT ;
- taxes ;
- montant TTC ;
- devise ;
- conditions de paiement ;
- durée de validité ;
- délais de réalisation ;
- observations.

---

# 8. Fonctionnalités MVP

Le MVP permet de :

- créer un devis ;
- modifier un devis ;
- ajouter des lignes ;
- calculer automatiquement les montants ;
- générer un PDF ;
- envoyer un devis ;
- suivre le statut ;
- accepter ou refuser un devis ;
- créer un projet après acceptation.

---

# 9. Fonctionnalités futures

Évolutions prévues :

- modèles de devis ;
- bibliothèque de prestations ;
- remises ;
- options interactives ;
- signature électronique ;
- paiement en ligne ;
- génération assistée par IA.

---

# 10. États

Le devis peut être :

- Brouillon
- En validation
- Envoyé
- Consulté
- En négociation
- Accepté
- Refusé
- Expiré
- Archivé

---

# 11. Règles métier

## BR-QUOTE-001

Un devis est obligatoirement lié à une opportunité.

---

## BR-QUOTE-002

Chaque devis possède un numéro unique.

---

## BR-QUOTE-003

Le montant total est calculé automatiquement.

---

## BR-QUOTE-004

Un devis accepté ne peut plus être modifié.

Une nouvelle version doit être créée si des changements sont nécessaires.

---

## BR-QUOTE-005

L'acceptation d'un devis permet la création du contrat puis du projet.

---

## BR-QUOTE-006

Toutes les versions d'un devis sont conservées.

---

# 12. Permissions

Sales

- créer ;
- modifier ;
- envoyer.

Administrator

- gestion complète.

Project Manager

- consultation.

Client

- consultation ;
- acceptation (selon le mode de validation retenu).

Super Administrator

- accès global.

---

# 13. Notifications

Le système notifie :

- création d'un devis ;
- envoi ;
- consultation ;
- acceptation ;
- refus ;
- expiration.

---

# 14. Journalisation

Les événements enregistrés comprennent :

- création ;
- modification ;
- changement de version ;
- envoi ;
- téléchargement ;
- acceptation ;
- refus.

---

# 15. Modèle de données

Entités principales :

- Quote
- QuoteVersion
- QuoteItem
- QuoteOption
- QuoteStatus

Les détails sont définis dans :

docs/architecture/database.md

---

# 16. APIs

Exemples :

GET /quotes

GET /quotes/{id}

POST /quotes

PATCH /quotes/{id}

POST /quotes/{id}/send

POST /quotes/{id}/accept

POST /quotes/{id}/reject

---

# 17. Sécurité

Le module applique :

- RBAC ;
- validation des données ;
- protection des documents ;
- journalisation des actions.

---

# 18. Performance

Objectifs :

- génération rapide des PDF ;
- calcul instantané des montants ;
- recherche optimisée ;
- chargement fluide des listes.

---

# 19. Critères d'acceptation

Le module est validé lorsque :

✓ un devis peut être créé ;

✓ les montants sont calculés correctement ;

✓ un PDF peut être généré ;

✓ les statuts évoluent correctement ;

✓ un devis accepté peut déclencher la création d'un projet ;

✓ les versions sont conservées.

---

# 20. Limites MVP

Le MVP ne comprend pas :

- signature électronique ;
- paiement en ligne ;
- bibliothèque de prestations ;
- remises avancées ;
- IA de génération.

---

# 21. Roadmap

V2

- Signature électronique
- Catalogue de prestations
- Modèles de devis
- Gestion des remises

V3

- AI Quote Assistant
- Estimation automatique
- Paiement en ligne
- Analyse prédictive du taux de conversion

---

# 22. Références

- docs/product/features/03-crm.md
- docs/product/features/06-projects.md
- docs/architecture/database.md
- docs/architecture/api.md
- docs/security/access-control.md

---