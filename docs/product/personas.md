# Personas

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
2. Pourquoi les personas sont importants
3. Les catégories d'utilisateurs
4. Hiérarchie des rôles
5. Évolution des personas
6. Références

---

# 1. Objectif

Ce document présente les différents profils d'utilisateurs (personas) de Zawena Platform.

Chaque persona possède son propre document décrivant :

- ses responsabilités ;
- ses objectifs ;
- ses besoins ;
- ses parcours utilisateurs ;
- ses permissions ;
- ses frustrations ;
- ses indicateurs de réussite.

L'objectif est de concevoir chaque fonctionnalité en tenant compte des besoins réels des utilisateurs.

---

# 2. Pourquoi les personas sont importants

Toutes les décisions produit doivent être prises en fonction des utilisateurs.

Les personas permettent notamment de :

- comprendre les attentes de chaque profil ;
- concevoir des interfaces adaptées ;
- définir les niveaux de permissions ;
- écrire les User Stories ;
- concevoir les User Flows ;
- prioriser les fonctionnalités.

Chaque nouvelle fonctionnalité doit répondre au besoin d'au moins un persona identifié.

---

# 3. Les catégories d'utilisateurs

Le MVP de Zawena Platform comprend plusieurs catégories de personas.

## Personas externes

Ces utilisateurs interagissent avec Zawena depuis le site internet ou l'espace client.

### Visitor

Visiteur anonyme découvrant Zawena.

Documentation :

personas/visitor.md

---

### Prospect

Entreprise ou particulier ayant manifesté un intérêt pour les services de Zawena.

Documentation :

personas/prospect.md

---

### Client

Client ayant signé un contrat avec Zawena.

Documentation :

personas/client.md

---

### Partner

Partenaire commercial ou technologique.

Documentation :

personas/partner.md

---

## Personas internes

Ces utilisateurs travaillent au sein de Zawena.

### Administrator

Administrateur de la plateforme.

Documentation :

personas/administrator.md

---

### Super Administrator

Responsable de l'administration globale.

Documentation :

personas/super-administrator.md

---

### Sales

Responsable commercial.

Documentation :

personas/sales.md

---

### Project Manager

Chef de projet.

Documentation :

personas/project-manager.md

---

### Developer

Développeur.

Documentation :

personas/developer.md

---

### Support

Support client.

Documentation :

personas/support.md

---

# 4. Hiérarchie des rôles

Les rôles sont organisés selon les niveaux de responsabilité suivants.

Niveau 1

Visitor

↓

Prospect

↓

Client

---

Niveau 2

Support

Sales

Project Manager

Developer

---

Niveau 3

Administrator

---

Niveau 4

Super Administrator

Chaque rôle possède des permissions adaptées à ses responsabilités.

Les règles détaillées sont documentées dans :

docs/architecture/permissions.md

---

# 5. Évolution des personas

À mesure que Zawena Platform évoluera, de nouveaux profils pourront être ajoutés.

Exemples :

- Finance
- Marketing
- RH
- Consultant IA
- Analyste Cybersécurité
- Responsable Conformité
- Auditeur
- Invité
- Fournisseur

La structure documentaire permet d'ajouter facilement de nouveaux personas sans modifier les documents existants.

---

# 6. Références

Documents associés :

- personas/
- user-stories/
- user-flows/
- docs/architecture/auth.md
- docs/architecture/permissions.md
- docs/product/08-functional-requirements.md
- docs/product/10-business-rules.md

---