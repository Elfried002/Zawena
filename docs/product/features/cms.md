# Feature Specification — CMS (Content Management System)

> Produit : Zawena Platform
>
> Module : CMS
>
> Identifiant : FEATURE-CMS
>
> Version : 1.0
>
> Statut : Approuvé pour MVP
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# 1. Objectif

Le CMS permet aux équipes de Zawena de créer, modifier, organiser, publier et archiver l'ensemble des contenus diffusés sur les canaux numériques de l'entreprise.

Il doit offrir une gestion centralisée des contenus tout en garantissant leur qualité, leur cohérence et leur sécurité.

---

# 2. Vue d'ensemble

Le CMS constitue le moteur éditorial de Zawena Platform.

Tous les contenus publics proviennent du CMS et sont ensuite diffusés sur le site web et, à terme, sur les différents produits de l'écosystème Zawena.

---

# 3. Vision du CMS

Le CMS est conçu autour de **Content Types** réutilisables.

Chaque contenu partage une structure commune (titre, slug, statut, auteur, SEO, dates), à laquelle s'ajoutent des champs spécifiques selon son type.

---

# 4. Valeur métier

Le CMS permet de :

- publier rapidement du contenu ;
- maintenir une identité de marque cohérente ;
- améliorer le référencement naturel (SEO) ;
- valoriser les réalisations de Zawena ;
- générer des prospects grâce au marketing de contenu.

---

# 5. Personas concernés

Principaux :

- Administrator
- Super Administrator

Secondaires :

- Sales
- Project Manager
- Developer (lecture technique)
- Visiteur (consultation des contenus publiés)

---

# 6. Architecture du contenu

Le CMS repose sur trois niveaux :

Contenu

↓

Type de contenu

↓

Publication

Chaque contenu est lié à :

- un auteur ;
- un statut ;
- des métadonnées SEO ;
- des médias.

---

# 7. Types de contenu

## MVP

- Page
- Service
- Article
- Étude de cas
- FAQ
- Page légale

## Versions futures

- Landing Page
- Témoignage
- Événement
- Offre d'emploi
- Newsletter
- Documentation
- Base de connaissances

---

# 8. Fonctionnalités MVP

Le CMS permet de :

- créer un contenu ;
- modifier un contenu ;
- enregistrer un brouillon ;
- publier un contenu ;
- dépublier un contenu ;
- archiver un contenu ;
- rechercher des contenus ;
- filtrer les contenus ;
- gérer les médias associés.

---

# 9. Fonctionnalités futures

Les futures versions intégreront :

- workflows éditoriaux avancés ;
- validation à plusieurs niveaux ;
- gestion des versions ;
- publication programmée avancée ;
- traduction multilingue ;
- IA de rédaction ;
- IA d'optimisation SEO.

---

# 10. Workflow éditorial

Cycle de vie d'un contenu :

Brouillon

↓

En révision

↓

Approuvé

↓

Programmé

↓

Publié

↓

Archivé

Le MVP utilise principalement les états **Brouillon**, **Publié** et **Archivé**.

---

# 11. Gestion des médias

Le CMS permet d'associer aux contenus :

- images ;
- illustrations ;
- logos ;
- icônes ;
- vidéos (URL ou intégration) ;
- documents PDF.

Les fichiers sont stockés dans le système de stockage défini par l'architecture de la plateforme.

---

# 12. SEO

Chaque contenu peut définir :

- SEO Title ;
- Meta Description ;
- Slug ;
- Image Open Graph ;
- Canonical URL ;
- Statut d'indexation.

Les champs SEO sont modifiables indépendamment du contenu principal.

---

# 13. Composants UI

Le module comprend notamment :

- Content Editor
- Rich Text Editor
- Media Picker
- Content List
- Status Badge
- SEO Panel
- Preview
- Filters
- Search Bar
- Pagination

---

# 14. États

Un contenu peut être :

- Brouillon
- Publié
- Archivé

Les états **En révision** et **Programmé** sont prévus pour les futures versions.

---

# 15. Permissions

Les permissions reposent sur le système RBAC.

Exemples :

- cms.read
- cms.create
- cms.update
- cms.publish
- cms.archive
- cms.delete

---

# 16. Journalisation

Les actions suivantes sont enregistrées :

- création ;
- modification ;
- publication ;
- dépublication ;
- archivage ;
- suppression logique.

---

# 17. Modèle de données

Entités principales :

- Content
- ContentType
- Media
- Category
- Tag
- Author

Les détails sont définis dans :

docs/architecture/database.md

---

# 18. APIs

Exemples :

GET /cms/content

GET /cms/content/{id}

POST /cms/content

PATCH /cms/content/{id}

DELETE /cms/content/{id}

GET /cms/media

POST /cms/media

---

# 19. Sécurité

Le CMS applique :

- contrôle d'accès RBAC ;
- validation des entrées ;
- protection contre les contenus malveillants ;
- journalisation des actions sensibles.

---

# 20. Performance

Objectifs :

- chargement rapide des listes ;
- pagination ;
- recherche optimisée ;
- gestion efficace des médias.

---

# 21. Critères d'acceptation

Le module est validé lorsque :

- un contenu peut être créé ;
- un brouillon peut être enregistré ;
- un contenu publié est visible sur le site ;
- un contenu archivé n'est plus accessible publiquement ;
- les médias sont correctement associés ;
- les métadonnées SEO sont enregistrées.

---

# 22. Roadmap

V2

- Gestion des versions
- Publication programmée
- Workflow éditorial
- Traduction multilingue

V3

- AI Content Assistant
- AI SEO Assistant
- Génération automatique de pages
- Base de connaissances intelligente

---

# 23. Références

- docs/product/features/01-website.md
- docs/design-system/
- docs/architecture/api.md
- docs/architecture/database.md
- docs/architecture/modules.md
- docs/security/security-policy.md