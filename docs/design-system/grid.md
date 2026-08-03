# Grid System — Zawena Platform

> Produit : Zawena Platform
>
> Document : Grid System
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
2. Principes
3. Structure de la grille
4. Colonnes
5. Conteneurs
6. Espacements (Gutters)
7. Alignement
8. Utilisation
9. Responsive
10. Bonnes pratiques
11. Références

---

# 1. Objectif

Ce document définit le système de grille utilisé par Zawena Platform.

Le Grid System garantit :

- une mise en page cohérente ;
- un alignement uniforme ;
- une interface responsive ;
- une meilleure maintenabilité du code.

Toutes les pages de la plateforme doivent être construites à partir de cette grille.

---

# 2. Principes

Le système de grille repose sur les principes suivants :

- Responsive First
- Colonnes flexibles
- Alignement constant
- Espacements homogènes
- Réutilisabilité

La grille doit fonctionner sur :

- Mobile
- Tablette
- Desktop
- Écrans larges

---

# 3. Structure de la grille

La grille est composée de :

- Conteneur principal
- Colonnes
- Gouttières (Gutters)
- Marges externes

Schéma simplifié :

```text
+------------------------------------------------------------+
| Margin | Column | Gutter | Column | Gutter | Column | ... |
+------------------------------------------------------------+
```

---

# 4. Colonnes

Le Design System utilise une grille de **12 colonnes**.

Cette grille permet de créer facilement :

- pages simples ;
- tableaux ;
- tableaux de bord ;
- formulaires ;
- cartes ;
- statistiques.

Exemples :

```text
12 / 12

6 / 6

8 / 4

9 / 3

4 / 4 / 4

3 / 3 / 3 / 3
```

Les colonnes sont réparties automatiquement selon l'espace disponible.

---

# 5. Conteneurs

Chaque page utilise un conteneur principal.

Les conteneurs doivent :

- centrer le contenu ;
- limiter la largeur maximale ;
- conserver des marges régulières ;
- rester fluides sur les grands écrans.

Les conteneurs ne doivent jamais dépasser la largeur définie par le Design System.

---

# 6. Espacements (Gutters)

Les gouttières séparent les colonnes.

Les espacements doivent être constants dans toute l'application.

Les tailles utilisées suivent l'échelle officielle du Design System :

```text
XS

S

M

L

XL
```

Les valeurs exactes sont définies dans les Design Tokens.

---

# 7. Alignement

Tous les composants doivent respecter les mêmes règles d'alignement.

Alignement horizontal :

- Gauche
- Centre
- Droite

Alignement vertical :

- Haut
- Centre
- Bas

Les composants d'une même section doivent partager le même axe d'alignement.

---

# 8. Utilisation

## Dashboard

Les widgets utilisent la grille afin de rester adaptatifs.

Exemple :

```text
+--------+--------+--------+--------+

 KPI 1     KPI 2     KPI 3     KPI 4

+--------+--------+--------+--------+
```

---

## Formulaires

Les champs peuvent occuper :

- toute la largeur ;
- la moitié ;
- un tiers.

Le choix dépend du contexte et de la lisibilité.

---

## Cartes

Les cartes s'alignent automatiquement sur la grille.

Les hauteurs peuvent varier, mais les largeurs doivent rester cohérentes.

---

## Tableaux

Les tableaux utilisent toute la largeur disponible du conteneur.

Les actions principales restent visibles sans défilement horizontal lorsque cela est possible.

---

# 9. Responsive

La grille s'adapte automatiquement selon la taille de l'écran.

Principes :

- Mobile : empilement vertical.
- Tablette : répartition simplifiée.
- Desktop : utilisation complète des 12 colonnes.
- Écrans larges : contenu centré avec largeur maximale.

Les points de rupture (breakpoints) sont définis dans le document Responsive.

---

# 10. Bonnes pratiques

Les développeurs doivent :

- utiliser la grille officielle ;
- éviter les largeurs arbitraires ;
- privilégier les composants réutilisables ;
- conserver des espacements réguliers ;
- éviter les décalages visuels.

Toute exception doit être justifiée.

---

# 11. Références

- UI Foundation
- Layout System
- Responsive Design
- Components
- Dashboard
- UX Guidelines