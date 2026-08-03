# Accessibility Guidelines — Zawena Platform

> Produit : Zawena Platform
>
> Document : Accessibility Guidelines
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
3. Normes de référence
4. Navigation au clavier
5. Gestion du focus
6. Couleurs et contrastes
7. Typographie
8. Images et médias
9. Formulaires
10. Composants interactifs
11. Messages et notifications
12. Responsive et zoom
13. Bonnes pratiques
14. Anti-patterns
15. Références

---

# 1. Objectif

Ce document définit les exigences d'accessibilité de Zawena Platform.

L'objectif est de garantir une plateforme :

- inclusive ;
- utilisable ;
- cohérente ;
- conforme aux bonnes pratiques internationales.

L'accessibilité est intégrée dès la conception ("Accessibility by Design").

---

# 2. Principes

Le Design System suit les quatre principes fondamentaux des WCAG.

## Perceptible

Les informations doivent pouvoir être perçues.

---

## Utilisable

Toutes les fonctionnalités doivent être accessibles.

---

## Compréhensible

L'interface doit être simple et prévisible.

---

## Robuste

Les composants doivent fonctionner avec les technologies d'assistance.

---

# 3. Normes de référence

Le Design System vise une conformité avec :

- WCAG 2.2 Niveau AA
- WAI-ARIA
- HTML sémantique
- Bonnes pratiques React

Toute exception doit être documentée.

---

# 4. Navigation au clavier

Toutes les fonctionnalités doivent être utilisables sans souris.

Les utilisateurs doivent pouvoir :

- naviguer avec Tab ;
- revenir avec Shift + Tab ;
- activer avec Entrée ou Espace ;
- fermer les dialogues avec Échap lorsque pertinent.

L'ordre de navigation doit être logique.

---

# 5. Gestion du focus

Les composants interactifs doivent toujours afficher un focus visible.

Le focus :

- ne doit jamais être supprimé sans remplacement équivalent ;
- doit rester clairement identifiable ;
- doit suivre un ordre cohérent.

Les modales et dialogues doivent piéger temporairement le focus jusqu'à leur fermeture.

---

# 6. Couleurs et contrastes

La couleur ne doit jamais être le seul moyen de transmettre une information.

Les contrastes doivent respecter les exigences WCAG AA.

Les états suivants doivent rester distinguables :

- normal ;
- focus ;
- erreur ;
- succès ;
- désactivé.

---

# 7. Typographie

Les textes doivent :

- rester lisibles ;
- utiliser une taille adaptée ;
- conserver un espacement suffisant ;
- éviter les blocs trop longs.

Les utilisateurs doivent pouvoir agrandir le texte sans perte de contenu ou de fonctionnalité.

---

# 8. Images et médias

Les images informatives doivent posséder un texte alternatif (`alt`).

Les images purement décoratives doivent être ignorées par les technologies d'assistance.

Les icônes utilisées seules doivent disposer d'un nom accessible.

Les vidéos et contenus audio devront proposer des alternatives adaptées lorsque cela est applicable.

---

# 9. Formulaires

Chaque champ doit posséder :

- un label explicite ;
- un identifiant unique ;
- un message d'aide si nécessaire.

Les erreurs doivent :

- être clairement expliquées ;
- être associées au champ concerné ;
- rester compréhensibles.

Les champs obligatoires doivent être identifiés autrement que par une couleur.

---

# 10. Composants interactifs

Tous les composants doivent :

- être accessibles au clavier ;
- posséder un nom accessible ;
- respecter les rôles ARIA lorsque nécessaire ;
- annoncer correctement leur état.

Exemples :

- boutons ;
- menus ;
- accordéons ;
- onglets ;
- modales ;
- listes déroulantes.

---

# 11. Messages et notifications

Les notifications importantes doivent pouvoir être annoncées aux technologies d'assistance.

Les messages de succès, d'erreur ou d'avertissement doivent :

- être compréhensibles ;
- rester visibles suffisamment longtemps ou être consultables ;
- ne pas interrompre inutilement la navigation.

---

# 12. Responsive et zoom

L'application doit rester utilisable :

- sur mobile ;
- sur tablette ;
- sur desktop ;
- avec un zoom du navigateur.

Le contenu ne doit pas nécessiter de défilement horizontal dans les cas d'usage courants.

---

# 13. Bonnes pratiques

✔ Utiliser des éléments HTML sémantiques.

✔ Prévoir un focus visible.

✔ Tester la navigation au clavier.

✔ Utiliser des libellés explicites.

✔ Fournir des messages d'erreur clairs.

✔ Vérifier les contrastes avant toute mise en production.

✔ Prévoir des alternatives textuelles lorsque nécessaire.

---

# 14. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Utiliser uniquement une couleur pour transmettre une information.

✘ Supprimer le focus clavier.

✘ Utiliser des placeholders comme seuls labels.

✘ Créer des composants impossibles à utiliser au clavier.

✘ Générer des messages d'erreur incompréhensibles.

✘ Utiliser des animations impossibles à interrompre lorsqu'elles peuvent gêner l'utilisateur.

---

# 15. Références

- UI Foundation
- Components Library
- Forms
- Navigation System
- Responsive Design
- UX Guidelines
- WCAG 2.2 AA
- WAI-ARIA Authoring Practices