# ADR-003 — Database Architecture

> ADR ID : ADR-003
>
> Titre : Database Architecture
>
> Statut : Accepted
>
> Date : 03 Août 2026
>
> Décideurs : Founder, Engineering Team
>
> Type : Architecture Decision

---

# Table des matières

1. Statut
2. Contexte
3. Problématique
4. Facteurs de décision
5. Options étudiées
6. Décision
7. Justification
8. Conséquences
9. Compromis (Trade-offs)
10. Évolutions futures
11. Révision
12. Documents associés

---

# 1. Statut

**Accepted**

Cette décision définit l'architecture officielle de gestion des données de Zawena Platform.

---

# 2. Contexte

Zawena est une plateforme SaaS multi-utilisateurs nécessitant une base de données :

- relationnelle ;
- sécurisée ;
- évolutive ;
- performante ;
- compatible avec Supabase ;
- capable de gérer des relations complexes entre les entités métier.

Les données manipulées comprennent notamment :

- utilisateurs ;
- entreprises ;
- projets ;
- clients ;
- tâches ;
- documents ;
- historiques ;
- journaux d'audit.

---

# 3. Problématique

Quelle architecture de base de données permet de garantir la cohérence des données, la sécurité, les performances et l'évolutivité de Zawena ?

---

# 4. Facteurs de décision

Les critères retenus sont :

- intégrité des données ;
- conformité ACID ;
- performances ;
- sécurité ;
- évolutivité ;
- facilité de maintenance ;
- compatibilité avec Supabase ;
- richesse des fonctionnalités SQL.

---

# 5. Options étudiées

## PostgreSQL

### Avantages

- conformité SQL ;
- transactions ACID ;
- excellentes performances ;
- extensible ;
- très mature ;
- compatible avec Supabase.

### Inconvénients

- modèle relationnel demandant une bonne conception.

---

## MySQL

### Avantages

- très populaire ;
- bonnes performances.

### Inconvénients

- fonctionnalités avancées plus limitées que PostgreSQL.

---

## MongoDB

### Avantages

- schéma flexible ;
- développement rapide pour certains cas d'usage.

### Inconvénients

- moins adapté aux relations complexes ;
- intégrité relationnelle plus difficile à garantir.

---

## Firebase Firestore

### Avantages

- temps réel ;
- simplicité.

### Inconvénients

- NoSQL ;
- requêtes complexes plus limitées ;
- dépendance forte à l'écosystème Firebase.

---

# 6. Décision

Zawena adopte **PostgreSQL**, fourni et administré via **Supabase**, comme système officiel de gestion de base de données.

Les principes retenus sont :

- modèle relationnel ;
- normalisation lorsque pertinente ;
- clés primaires UUID ;
- contraintes d'intégrité ;
- indexation adaptée ;
- Row Level Security (RLS) ;
- migrations versionnées.

---

# 7. Justification

Le choix de PostgreSQL repose notamment sur :

## Robustesse

PostgreSQL est reconnu pour sa stabilité et sa fiabilité en production.

---

## Intégrité

Le modèle relationnel garantit la cohérence des données grâce aux contraintes, aux transactions et aux clés étrangères.

---

## Sécurité

L'intégration avec Supabase permet notamment :

- Row Level Security ;
- politiques d'accès fines ;
- authentification intégrée ;
- journalisation.

---

## Évolutivité

La base peut évoluer avec le produit sans remise en cause majeure de l'architecture.

---

## Écosystème

PostgreSQL bénéficie :

- d'une communauté importante ;
- d'une excellente documentation ;
- d'un large support par les outils modernes.

---

# 8. Conséquences

## Positives

- données cohérentes ;
- excellente sécurité ;
- maintenance facilitée ;
- évolutivité ;
- compatibilité avec les outils analytiques.

---

## Négatives

- nécessité d'une conception rigoureuse du schéma ;
- migrations à gérer avec discipline.

---

# 9. Compromis (Trade-offs)

Les principaux compromis sont :

- privilégier la cohérence des données plutôt que la flexibilité d'un modèle NoSQL ;
- accepter une phase de modélisation plus importante afin de réduire les problèmes futurs.

Ces compromis sont cohérents avec les besoins métier de Zawena.

---

# 10. Évolutions futures

L'architecture pourra évoluer selon :

- l'augmentation du volume de données ;
- les besoins analytiques ;
- l'apparition de nouveaux cas d'usage (par exemple, ajout d'une base vectorielle pour des fonctionnalités IA) ;
- les contraintes réglementaires.

Toute évolution majeure fera l'objet d'un nouvel ADR.

---

# 11. Révision

Cette décision est revue :

- après une évolution majeure de l'architecture de données ;
- avant une migration importante ;
- au minimum une fois par an.

---

# 12. Documents associés

- Database Design
- Data Model
- Data Dictionary
- Security Policy
- Backup Strategy
- ADR-002 Technology Stack
- ADR-004 Authentication