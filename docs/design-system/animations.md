# Animations & Motion — Zawena Platform

> Produit : Zawena Platform
>
> Document : Animations & Motion
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
3. Philosophie du mouvement
4. Types d'animations
5. Durées
6. Courbes d'animation
7. Animations des composants
8. États de chargement
9. Accessibilité
10. Performance
11. Bonnes pratiques
12. Anti-patterns
13. Références

---

# 1. Objectif

Ce document définit les règles d'animation de Zawena Platform.

Les animations doivent :

- améliorer la compréhension ;
- guider l'utilisateur ;
- fournir un feedback immédiat ;
- renforcer la cohérence de l'interface.

Les animations ne sont jamais utilisées uniquement à des fins décoratives.

---

# 2. Principes

Toutes les animations doivent être :

- discrètes ;
- cohérentes ;
- rapides ;
- fluides ;
- utiles.

Chaque animation doit répondre à un besoin fonctionnel.

---

# 3. Philosophie du mouvement

Les animations servent principalement à :

## Guider

Montrer où l'attention doit se porter.

---

## Confirmer

Indiquer qu'une action a été exécutée.

---

## Relier

Montrer la relation entre deux états.

---

## Informer

Illustrer un chargement ou une transition.

---

## Prévenir

Attirer l'attention sur une erreur ou une information importante.

---

# 4. Types d'animations

## Fade

Utilisation :

- apparition ;
- disparition.

---

## Slide

Utilisation :

- Sidebar ;
- Drawer ;
- Menu mobile.

---

## Scale

Utilisation :

- Modales ;
- Dialogues ;
- Popovers.

---

## Collapse

Utilisation :

- Accordéons ;
- Sections repliables.

---

## Skeleton

Utilisation :

Chargement des contenus.

---

## Spinner

Utilisation :

Chargements courts.

---

## Toast

Utilisation :

Notifications temporaires.

---

## Progress

Utilisation :

Téléversements ;
traitements longs.

---

# 5. Durées

Les animations doivent rester courtes.

| Type | Durée recommandée |
|-------|------------------:|
| Hover | 100–150 ms |
| Focus | 100–150 ms |
| Bouton | 150–200 ms |
| Menu | 200–250 ms |
| Drawer | 250–300 ms |
| Modale | 250–300 ms |
| Toast | 200–300 ms |

Les animations supérieures à 500 ms doivent être exceptionnelles.

---

# 6. Courbes d'animation

Les transitions doivent privilégier des courbes naturelles.

Utilisation recommandée :

- Ease Out → apparition
- Ease In → disparition
- Ease In Out → transition générale

Les animations doivent éviter les accélérations brusques.

---

# 7. Animations des composants

## Boutons

- Hover discret.
- Focus visible.
- Loading fluide.

---

## Cards

- Légère élévation au survol si elles sont interactives.
- Transition douce.

---

## Sidebar

- Ouverture progressive.
- Fermeture rapide.

---

## Modales

- Apparition avec un léger effet d'échelle.
- Disparition fluide.

---

## Toasts

- Apparition discrète.
- Disparition automatique.

---

## Tableaux

Les nouvelles lignes peuvent être mises en évidence brièvement.

Les suppressions doivent être confirmées avant toute animation.

---

## Formulaires

Les erreurs peuvent être mises en évidence de manière discrète.

Les validations réussies doivent fournir un retour visuel sans distraire.

---

# 8. États de chargement

Pendant un chargement :

- privilégier les Skeletons pour les contenus structurés ;
- utiliser un Spinner pour les actions courtes ;
- afficher une barre de progression pour les opérations longues.

Les interfaces ne doivent jamais sembler figées.

---

# 9. Accessibilité

Les animations doivent respecter les préférences système.

Si l'utilisateur active "Reduce Motion" :

- réduire ou supprimer les animations non essentielles ;
- conserver uniquement les transitions nécessaires à la compréhension.

Les animations ne doivent jamais provoquer :

- clignotements rapides ;
- mouvements excessifs ;
- distraction permanente.

---

# 10. Performance

Les animations doivent :

- privilégier `transform` et `opacity` ;
- éviter les recalculs de layout inutiles ;
- rester fluides sur les appareils modestes.

Les animations ne doivent pas dégrader les performances de l'application.

---

# 11. Bonnes pratiques

✔ Utiliser les animations avec parcimonie.

✔ Fournir un retour immédiat après une action.

✔ Garder des durées cohérentes.

✔ Tester les animations sur mobile et desktop.

✔ Respecter les préférences d'accessibilité.

---

# 12. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Animations uniquement décoratives.

✘ Animations trop longues.

✘ Plusieurs animations simultanées sans justification.

✘ Effets visuels excessifs.

✘ Animations bloquant l'interaction.

✘ Clignotements rapides.

---

# 13. Références

- UI Foundation
- Components Library
- Accessibility
- Responsive Design
- UX Guidelines