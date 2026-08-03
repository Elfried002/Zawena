# Buttons — Zawena Platform

> Produit : Zawena Platform
>
> Document : Buttons
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
3. Anatomie d'un bouton
4. Variantes
5. Tailles
6. États
7. Icônes
8. Utilisation
9. Accessibilité
10. Responsive
11. Bonnes pratiques
12. Anti-patterns
13. Références

---

# 1. Objectif

Les boutons permettent aux utilisateurs de déclencher une action.

Ils constituent le principal composant d'interaction de Zawena Platform.

Tous les boutons de l'application doivent respecter les règles définies dans ce document.

---

# 2. Principes

Un bouton doit toujours :

- être facilement identifiable ;
- indiquer clairement son action ;
- fournir un retour visuel ;
- rester cohérent avec le Design System ;
- être accessible.

Chaque écran doit posséder une hiérarchie claire entre les boutons principaux et secondaires.

---

# 3. Anatomie d'un bouton

Un bouton peut être composé des éléments suivants :

```text
┌──────────────────────────────┐
│  Icône   Libellé    Badge    │
└──────────────────────────────┘
```

Éléments possibles :

- Icône (optionnelle)
- Texte (obligatoire sauf cas particuliers)
- Badge (optionnel)
- Indicateur de chargement

---

# 4. Variantes

## Primary Button

Utilisation :

- Action principale d'une page

Exemples :

- Enregistrer
- Créer
- Publier
- Continuer

Une seule action primaire est recommandée par écran.

---

## Secondary Button

Utilisation :

Actions secondaires.

Exemples :

- Modifier
- Retour
- Prévisualiser

---

## Outline Button

Utilisation :

Actions importantes mais non prioritaires.

---

## Ghost Button

Utilisation :

Actions discrètes.

Exemples :

- Voir plus
- Annuler
- Fermer

---

## Destructive Button

Utilisation :

Actions irréversibles.

Exemples :

- Supprimer
- Désactiver
- Archiver définitivement

Une confirmation doit être demandée avant l'exécution de l'action.

---

## Link Button

Utilisation :

Navigation interne ou externe.

---

# 5. Tailles

Les tailles officielles sont :

## Small (SM)

Utilisation :

- tableaux ;
- listes ;
- actions secondaires.

---

## Medium (MD)

Taille par défaut.

---

## Large (LG)

Utilisation :

- Hero
- Landing Page
- CTA

---

## Icon Button

Bouton composé uniquement d'une icône.

Il doit toujours posséder un libellé accessible (`aria-label`).

---

# 6. États

Tous les boutons doivent gérer les états suivants.

## Default

État normal.

---

## Hover

Le bouton indique qu'il est interactif.

---

## Focus

Visible lors de la navigation clavier.

---

## Active

Retour visuel après un clic.

---

## Disabled

Le bouton est visible mais inactif.

Il ne doit jamais être utilisé pour masquer une permission.

---

## Loading

Le bouton affiche un indicateur de chargement.

Pendant cet état :

- clic désactivé ;
- texte conservé si possible ;
- spinner affiché.

---

## Success

Utilisé uniquement après certaines actions importantes.

---

## Error

Affiché lorsqu'une action a échoué.

---

# 7. Icônes

Les icônes sont autorisées :

Avant le texte :

```text
➕ Nouveau projet
```

Après le texte :

```text
Continuer →
```

Les icônes seules sont réservées :

- Toolbar
- Header
- Sidebar
- Actions rapides

---

# 8. Utilisation

Les boutons sont utilisés notamment pour :

- créer ;
- modifier ;
- supprimer ;
- enregistrer ;
- exporter ;
- envoyer ;
- publier ;
- confirmer.

Le texte du bouton doit toujours commencer par un verbe d'action lorsque cela est pertinent.

Exemples :

- Créer un projet
- Enregistrer
- Envoyer le devis
- Publier
- Télécharger

---

# 9. Accessibilité

Tous les boutons doivent :

- être accessibles au clavier ;
- posséder un focus visible ;
- respecter les contrastes WCAG AA ;
- disposer d'un nom accessible.

Les boutons composés uniquement d'une icône doivent toujours utiliser un `aria-label`.

---

# 10. Responsive

Sur mobile :

- les boutons principaux peuvent occuper toute la largeur ;
- les groupes de boutons peuvent être empilés.

Sur desktop :

- largeur adaptée au contenu ;
- alignement cohérent avec les actions de la page.

---

# 11. Bonnes pratiques

✔ Utiliser une seule action primaire par écran.

✔ Utiliser des verbes explicites.

✔ Conserver une taille cohérente.

✔ Utiliser les variantes officielles.

✔ Désactiver les doubles clics pendant le chargement.

✔ Conserver des espacements réguliers entre les boutons.

---

# 12. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Plusieurs boutons Primary côte à côte.

✘ Texte ambigu.

Exemple :

```text
OK
```

Préférer :

```text
Enregistrer les modifications
```

---

✘ Utiliser la couleur seule pour transmettre une information.

---

✘ Changer la taille d'un bouton de manière arbitraire.

---

✘ Utiliser un bouton lorsqu'un lien est plus approprié.

---

# 13. Références

- UI Foundation
- Components Library
- Accessibility
- UX Guidelines
- Forms