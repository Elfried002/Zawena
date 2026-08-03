# Product Requirements Document (PRD)

> Produit : Zawena Platform
>
> Version : 1.0
>
> Statut : En cours de développement
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Présentation
2. Objectifs
3. Vision Produit
4. Périmètre
5. Utilisateurs
6. Modules du MVP
7. Architecture documentaire
8. Principes Produit
9. Critères de succès
10. Références

---

# 1. Présentation

## Contexte

Zawena Platform est la plateforme centrale de Zawena.

À son lancement, elle constitue l'environnement de travail interne permettant de gérer :

- le site internet ;
- les prospects ;
- les demandes de devis ;
- les clients ;
- les projets ;
- le contenu du site ;
- l'administration de la plateforme.

À long terme, Zawena Platform deviendra le socle technique de l'ensemble des produits SaaS développés par Zawena.

---

## Objectif principal

Créer une plateforme unique permettant :

- de présenter les services de Zawena ;
- d'acquérir des prospects ;
- de gérer les opérations internes ;
- de centraliser les données ;
- de servir de fondation aux futurs produits SaaS.

---

# 2. Objectifs

Le MVP poursuit plusieurs objectifs.

## Business

- Obtenir les premiers clients.
- Générer des demandes de devis.
- Professionnaliser l'image de Zawena.
- Structurer les opérations internes.

---

## Produit

Construire une architecture modulaire.

Créer des composants réutilisables.

Préparer les futurs SaaS.

---

## Technique

Mettre en place :

- une architecture évolutive ;
- un système d'authentification robuste ;
- une base de données extensible ;
- un Design System commun.

---

# 3. Vision Produit

La vision détaillée est disponible dans :

```
02-product-vision.md
```

En résumé :

Aujourd'hui :

Une plateforme de gestion interne.

↓

Demain :

Une plateforme regroupant plusieurs logiciels SaaS.

↓

À terme :

Un véritable écosystème logiciel connecté.

---

# 4. Périmètre

Le MVP comprend uniquement les fonctionnalités nécessaires au lancement commercial de Zawena.

Sont inclus :

- Site vitrine
- CRM
- Gestion des devis
- Gestion des projets
- CMS
- Dashboard Administrateur
- Authentification
- Gestion des utilisateurs
- Paramètres

Les fonctionnalités avancées seront développées progressivement.

---

# 5. Utilisateurs

Le produit s'adresse principalement à trois catégories d'utilisateurs.

## Visiteur

Découvre Zawena.

Consulte les services.

Demande un devis.

Prend contact.

---

## Client

Suit ses projets.

Consulte ses devis.

Accède à son espace.

Communique avec Zawena.

---

## Administrateur

Pilote l'ensemble de la plateforme.

Gère les utilisateurs.

Gère les contenus.

Suit les performances.

Administre les projets.

---

Les personas détaillés sont documentés dans :

```
04-personas.md
```

---

# 6. Modules du MVP

Le MVP est constitué des modules suivants.

## Site Internet

Présentation de l'entreprise.

---

## CRM

Gestion des prospects.

---

## Gestion des devis

Création.

Validation.

Suivi.

---

## Gestion des projets

Pilotage des missions.

---

## CMS

Gestion du contenu.

---

## Dashboard

Pilotage global.

---

## Authentification

Connexion.

Gestion des comptes.

Permissions.

---

## Paramètres

Configuration de la plateforme.

---

Chaque module possède sa propre documentation dans :

```
features/
```

---

# 7. Architecture documentaire

La documentation produit est organisée comme suit.

```
docs/product/

01-prd.md

02-product-vision.md

03-product-goals.md

04-personas.md

features/

user-stories/

user-flows/

08-functional-requirements.md

09-non-functional-requirements.md

10-business-rules.md

11-acceptance-criteria.md

12-mvp-definition.md

13-release-plan.md

14-roadmap.md

15-sitemap.md
```

---

# 8. Principes Produit

Tous les développements doivent respecter les principes suivants.

## Modularité

Chaque fonctionnalité est indépendante.

---

## Simplicité

Ne développer que ce qui apporte de la valeur.

---

## Réutilisation

Les composants sont conçus pour être partagés entre les futurs produits.

---

## Sécurité

Security by Design.

---

## Performance

Temps de chargement réduit.

Architecture optimisée.

---

## Documentation

Toute nouvelle fonctionnalité est documentée avant son développement.

---

# 9. Critères de succès

Le MVP sera considéré comme réussi lorsque :

✓ Le site internet est en production.

✓ Les demandes de devis sont entièrement gérées depuis la plateforme.

✓ Les prospects sont centralisés dans le CRM.

✓ Les projets peuvent être suivis.

✓ Le CMS permet de modifier les contenus.

✓ L'administration est opérationnelle.

✓ Les premiers clients utilisent la plateforme.

---

# 10. Références

## Vision Produit

02-product-vision.md

---

## Objectifs

03-product-goals.md

---

## Personas

04-personas.md

---

## Fonctionnalités

features/

---

## User Stories

user-stories/

---

## User Flows

user-flows/

---

## Architecture

docs/architecture/

---

## Design System

docs/design-system/

---

## Développement

docs/development/

---