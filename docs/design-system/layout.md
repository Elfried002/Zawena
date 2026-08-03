# Layout System — Zawena Platform

> Produit : Zawena Platform
>
> Document : Layout System
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Design System Team

---

# Table des matières

1. Objectif
2. Principes du Layout
3. Types de Layouts
4. Structure générale
5. Zones principales
6. Conteneurs
7. Espacements
8. Hauteurs et largeurs
9. Gestion des pages
10. Bonnes pratiques
11. Références

---

# 1. Objectif

Ce document définit l'organisation générale des interfaces de Zawena Platform.

Il garantit que toutes les pages utilisent une structure cohérente afin d'améliorer :

- la lisibilité ;
- la navigation ;
- la maintenabilité ;
- l'expérience utilisateur.

---

# 2. Principes du Layout

Tous les layouts doivent respecter les principes suivants :

- cohérence visuelle ;
- simplicité ;
- réutilisabilité ;
- responsive design ;
- séparation claire des zones fonctionnelles.

Chaque page doit être construite à partir d'un layout officiel.

---

# 3. Types de Layouts

La plateforme utilise plusieurs layouts selon le contexte.

## Public Layout

Utilisé pour :

- Accueil
- Services
- Réalisations
- Blog
- FAQ
- Contact
- Demande de devis

Structure :

```text
Header

↓

Hero (si nécessaire)

↓

Main Content

↓

Footer
```

---

## Authentication Layout

Utilisé pour :

- Connexion
- Mot de passe oublié
- Réinitialisation
- Vérification Email

Structure :

```text
Logo

↓

Formulaire

↓

Actions secondaires
```

L'interface doit rester minimaliste afin de concentrer l'attention sur l'action principale.

---

## Dashboard Layout

Utilisé pour toute l'application interne.

Structure :

```text
Header

↓

Sidebar

↓

Main Content

↓

Right Panel (optionnel)
```

---

## Client Portal Layout

Structure similaire au Dashboard mais simplifiée.

Le client ne voit que les modules qui lui sont accessibles.

---

# 4. Structure générale

Le Dashboard est organisé comme suit :

```text
+---------------------------------------------------------------+
| Header                                                        |
+-------------+-------------------------------------------------+
| Sidebar     |                                                 |
|             |               Main Content                      |
|             |                                                 |
|             |                                                 |
+-------------+-------------------------------------------------+
```

La Sidebar reste visible sur ordinateur.

Sur mobile, elle devient un menu latéral repliable.

---

# 5. Zones principales

## Header

Contient :

- Logo
- Navigation principale
- Recherche globale
- Notifications
- Profil utilisateur

---

## Sidebar

Contient :

- Navigation principale
- Accès rapides
- Modules
- Paramètres

La Sidebar peut être réduite.

---

## Main Content

Contient :

- titre de page ;
- breadcrumbs ;
- actions principales ;
- contenu métier.

---

## Right Panel (optionnel)

Peut afficher :

- activités récentes ;
- aide contextuelle ;
- détails d'un élément ;
- historique.

---

## Footer

Principalement utilisé sur le site public.

Il contient :

- liens utiles ;
- informations légales ;
- réseaux sociaux ;
- copyright.

---

# 6. Conteneurs

Chaque page utilise un conteneur principal.

Les conteneurs doivent :

- limiter la largeur maximale du contenu ;
- conserver des marges constantes ;
- rester responsives.

Les composants ne doivent jamais toucher directement les bords de l'écran.

---

# 7. Espacements

Les espacements doivent suivre une échelle cohérente.

Exemple :

```text
XS

S

M

L

XL

2XL
```

Les mêmes espacements sont utilisés dans toute la plateforme.

Les valeurs exactes sont définies dans les tokens du Design System.

---

# 8. Hauteurs et largeurs

Les dimensions des principaux éléments doivent rester cohérentes.

Exemples :

- Header : hauteur fixe.
- Sidebar : largeur fixe avec mode réduit.
- Cartes : largeur adaptable.
- Tableaux : largeur disponible.
- Dialogues : largeur limitée selon leur contenu.

Les composants doivent privilégier les dimensions relatives plutôt que fixes lorsque cela est possible.

---

# 9. Gestion des pages

Chaque page doit respecter la structure suivante :

```text
Titre

↓

Description (optionnelle)

↓

Actions principales

↓

Filtres (si nécessaire)

↓

Contenu principal

↓

Pagination ou informations complémentaires
```

Cette organisation facilite la compréhension et la navigation.

---

# 10. Bonnes pratiques

Les interfaces doivent :

- éviter les surcharges visuelles ;
- conserver des alignements réguliers ;
- utiliser les mêmes marges sur toutes les pages ;
- éviter les défilements horizontaux ;
- privilégier les composants réutilisables.

Tout nouveau layout doit être validé avant son intégration.

---

# 11. Références

- UI Foundation
- Grid System
- Responsive Design
- Navigation
- Components
- Dashboard
- UX Guidelines