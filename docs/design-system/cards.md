# Cards — Zawena Platform

> Produit : Zawena Platform
>
> Document : Cards
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
3. Anatomie d'une Card
4. Variantes
5. Tailles
6. États
7. Utilisation
8. Accessibilité
9. Responsive
10. Bonnes pratiques
11. Anti-patterns
12. Références

---

# 1. Objectif

Les Cards permettent de regrouper des informations liées dans un conteneur visuellement identifiable.

Elles améliorent :

- la lisibilité ;
- l'organisation des données ;
- la hiérarchie visuelle ;
- la réutilisabilité des interfaces.

Toutes les cartes utilisées dans Zawena doivent respecter ce document.

---

# 2. Principes

Une Card doit :

- regrouper un seul sujet ;
- posséder une hiérarchie claire ;
- être facilement scannable ;
- fonctionner sur mobile et desktop ;
- rester indépendante des autres cartes.

Une Card ne doit jamais contenir plusieurs actions principales concurrentes.

---

# 3. Anatomie d'une Card

Une Card peut être composée des éléments suivants :

```text
┌─────────────────────────────────────────────┐
│  Header                                     │
│  Titre                                      │
│  Description                                │
├─────────────────────────────────────────────┤
│                                             │
│               Content                       │
│                                             │
├─────────────────────────────────────────────┤
│ Footer                                      │
│ Actions • Statut • Informations             │
└─────────────────────────────────────────────┘
```

Éléments disponibles :

- Header
- Title
- Subtitle
- Badge
- Actions
- Content
- Footer

Tous les éléments sont optionnels sauf le contenu principal.

---

# 4. Variantes

## Default Card

Usage :

Affichage général.

Exemples :

- fiche client ;
- projet ;
- devis.

---

## KPI Card

Utilisée pour les indicateurs.

Exemples :

- chiffre d'affaires ;
- nombre de projets ;
- leads.

---

## Stat Card

Affiche une métrique importante.

---

## Information Card

Affiche des informations sans action.

---

## Action Card

Met en avant une action.

Exemple :

Créer un nouveau projet.

---

## Selectable Card

Peut être sélectionnée.

Utilisée notamment pour :

- choix d'une offre ;
- sélection d'un modèle ;
- galerie.

---

## Expandable Card

Permet d'afficher des informations supplémentaires.

---

## Interactive Card

Toute la carte est cliquable.

À utiliser uniquement lorsque cela améliore l'expérience utilisateur.

---

# 5. Tailles

Les tailles disponibles sont :

## Small

Utilisation :

- Dashboard
- Widgets
- KPIs

---

## Medium

Taille standard.

---

## Large

Utilisation :

- détails d'un projet ;
- fiche client ;
- contenu riche.

---

## Full Width

Occupe toute la largeur du conteneur.

Principalement utilisée pour :

- tableaux ;
- historiques ;
- activités.

---

# 6. États

Toutes les Cards doivent gérer :

## Default

Affichage normal.

---

## Hover

Indique que la carte est interactive.

---

## Focus

Visible lors de la navigation clavier.

---

## Selected

Indique une sélection.

---

## Disabled

La carte reste visible mais ne peut pas être utilisée.

---

## Loading

Affichage Skeleton.

---

## Error

Erreur de chargement.

---

## Empty

Absence de contenu.

---

# 7. Utilisation

Les Cards sont utilisées notamment pour :

- Dashboard
- CRM
- Projects
- Quotes
- CMS
- Notifications
- Analytics

Une Card ne doit pas remplacer un tableau lorsque la comparaison entre plusieurs éléments est nécessaire.

---

# 8. Accessibilité

Les Cards interactives doivent :

- être accessibles au clavier ;
- posséder un focus visible ;
- disposer d'un nom accessible si elles sont entièrement cliquables ;
- respecter les contrastes WCAG AA.

Les cartes non interactives ne doivent pas être annoncées comme des boutons.

---

# 9. Responsive

Sur mobile :

- empilement vertical ;
- largeur complète.

Sur tablette :

- grille de 2 colonnes lorsque pertinent.

Sur desktop :

- grille adaptable selon le contenu.

Les hauteurs peuvent varier, mais les largeurs doivent rester cohérentes dans une même section.

---

# 10. Bonnes pratiques

✔ Une Card = un sujet.

✔ Utiliser des titres courts.

✔ Limiter le nombre d'actions.

✔ Conserver des espacements réguliers.

✔ Afficher clairement le statut.

✔ Utiliser les variantes officielles.

---

# 11. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Trop d'informations dans une seule Card.

✘ Plusieurs actions principales.

✘ Cartes avec des hauteurs incohérentes dans une même grille.

✘ Utiliser une Card lorsqu'un tableau est plus approprié.

✘ Mélanger plusieurs domaines métier dans une même Card.

---

# 12. Références

- UI Foundation
- Layout System
- Grid System
- Components Library
- Dashboard
- Accessibility
- UX Guidelines