# Forms — Zawena Platform

> Produit : Zawena Platform
>
> Document : Forms
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
3. Anatomie d'un formulaire
4. Types de champs
5. Validation
6. États des formulaires
7. Messages
8. Actions
9. Accessibilité
10. Responsive
11. Bonnes pratiques
12. Anti-patterns
13. Références

---

# 1. Objectif

Les formulaires permettent aux utilisateurs de créer, consulter, modifier ou supprimer des données dans Zawena Platform.

Tous les formulaires doivent offrir une expérience cohérente, rapide, accessible et sécurisée.

---

# 2. Principes

Chaque formulaire doit être :

- simple ;
- clair ;
- prévisible ;
- accessible ;
- réutilisable ;
- responsive.

Les utilisateurs doivent toujours comprendre :

- quelles informations sont attendues ;
- quels champs sont obligatoires ;
- pourquoi une erreur est affichée ;
- quelle action sera exécutée.

---

# 3. Anatomie d'un formulaire

Structure recommandée :

```text
Titre

↓

Description (optionnelle)

↓

Sections

↓

Champs

↓

Messages d'aide

↓

Résumé des erreurs (si nécessaire)

↓

Boutons d'action
```

Exemple :

```text
Créer un projet

Nom du projet

Description

Client

Chef de projet

Date de début

Date de fin

[ Annuler ]     [ Créer le projet ]
```

---

# 4. Types de champs

## Text Input

Utilisation :

- Nom
- Société
- Ville
- Titre

---

## Email Input

Validation automatique du format.

---

## Password Input

Utilisé uniquement pour l'authentification.

Le champ doit permettre :

- masquer / afficher le mot de passe.

---

## Number Input

Utilisé pour :

- montants ;
- quantités ;
- durées.

---

## Textarea

Pour les contenus longs :

- description ;
- commentaires ;
- notes.

---

## Select

Utilisé lorsqu'une seule option est possible.

Exemples :

- statut ;
- pays ;
- rôle.

---

## Multi Select

Permet plusieurs sélections.

---

## Checkbox

Utilisée pour :

- accepter des conditions ;
- sélectionner plusieurs éléments.

---

## Radio Group

Permet un choix unique parmi plusieurs options visibles.

---

## Switch

Utilisé pour activer ou désactiver une option.

---

## Date Picker

Sélection de date.

---

## Date Range Picker

Sélection d'une période.

---

## Time Picker

Sélection d'une heure.

---

## File Upload

Utilisé pour :

- documents ;
- images ;
- livrables.

Le composant doit afficher :

- nom ;
- taille ;
- progression ;
- état du téléchargement.

---

## Rich Text Editor

Utilisé dans :

- Blog
- CMS
- Descriptions riches

---

## Search Input

Champ avec recherche instantanée.

---

# 5. Validation

La validation est réalisée :

- côté client ;
- côté serveur.

Les règles doivent être identiques.

Chaque champ peut être :

- requis ;
- optionnel ;
- conditionnel.

Les erreurs sont affichées immédiatement après la validation.

Les validations métier restent effectuées côté serveur.

---

# 6. États des formulaires

Tous les formulaires doivent gérer les états suivants.

## Default

Formulaire prêt.

---

## Editing

Modification en cours.

---

## Loading

Soumission en cours.

Les actions doivent être temporairement désactivées.

---

## Success

Confirmation de l'enregistrement.

---

## Error

Affichage des erreurs.

---

## Read Only

Consultation sans modification.

---

## Disabled

Le formulaire est visible mais non modifiable.

---

# 7. Messages

## Message d'aide

Explique ce qui est attendu.

Exemple :

```text
Le nom du projet sera visible par les membres de l'équipe.
```

---

## Message d'erreur

Décrit clairement le problème.

Exemple :

```text
Veuillez saisir une adresse email valide.
```

Éviter :

```text
Erreur 502
```

---

## Message de confirmation

Informe l'utilisateur de la réussite d'une action.

Exemple :

```text
Projet créé avec succès.
```

---

# 8. Actions

Les formulaires utilisent généralement :

- Enregistrer
- Créer
- Modifier
- Publier
- Envoyer
- Annuler
- Réinitialiser

Une seule action primaire est recommandée.

Les actions destructives doivent demander une confirmation.

---

# 9. Accessibilité

Tous les formulaires doivent :

- être entièrement navigables au clavier ;
- posséder des labels explicites ;
- associer chaque erreur au champ concerné ;
- annoncer les erreurs aux lecteurs d'écran ;
- respecter les contrastes WCAG AA.

Les champs obligatoires doivent être identifiés sans utiliser uniquement la couleur.

---

# 10. Responsive

Sur mobile :

- une seule colonne ;
- boutons empilés si nécessaire ;
- champs pleine largeur.

Sur tablette :

- deux colonnes lorsque cela améliore la lisibilité.

Sur desktop :

- plusieurs colonnes selon le contexte.

Les formulaires ne doivent jamais provoquer un défilement horizontal.

---

# 11. Bonnes pratiques

✔ Grouper les champs par thème.

✔ Utiliser des labels explicites.

✔ Afficher les erreurs près du champ concerné.

✔ Limiter le nombre de champs visibles.

✔ Pré-remplir les informations connues lorsque cela est pertinent.

✔ Utiliser une validation progressive.

✔ Conserver les données saisies en cas d'erreur.

---

# 12. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Labels remplacés uniquement par des placeholders.

✘ Messages d'erreur techniques.

✘ Formulaires trop longs sans sections.

✘ Champs obligatoires non identifiés.

✘ Réinitialisation automatique des champs après une erreur.

✘ Validation uniquement côté client.

---

# 13. Références

- UI Foundation
- Components Library
- Buttons
- Accessibility
- Responsive Design
- UX Guidelines
- Functional Requirements