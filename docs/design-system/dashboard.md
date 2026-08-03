# Dashboard Design — Zawena Platform

> Produit : Zawena Platform
>
> Document : Dashboard Design
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
3. Structure du Dashboard
4. Widgets
5. Cartes KPI
6. Graphiques
7. Tableaux
8. Filtres
9. Personnalisation
10. États
11. Responsive
12. Accessibilité
13. Bonnes pratiques
14. Anti-patterns
15. Références

---

# 1. Objectif

Le Dashboard constitue le point d'entrée principal des utilisateurs authentifiés.

Il permet de :

- visualiser les indicateurs clés (KPI) ;
- accéder rapidement aux modules ;
- suivre les activités récentes ;
- identifier les éléments nécessitant une action.

Chaque rôle dispose d'un Dashboard adapté à ses responsabilités.

---

# 2. Principes

Le Dashboard doit être :

- pertinent ;
- personnalisable ;
- rapide à consulter ;
- orienté vers l'action ;
- cohérent avec le reste de l'application.

Les informations les plus importantes doivent apparaître sans défilement lorsque cela est possible.

---

# 3. Structure du Dashboard

Organisation recommandée :

```text
Titre de la page

↓

Actions rapides

↓

Cartes KPI

↓

Graphiques

↓

Tableaux

↓

Activités récentes

↓

Widgets secondaires
```

Toutes les sections ne sont pas obligatoires.

---

# 4. Widgets

Le Dashboard est composé de widgets indépendants.

Chaque widget possède :

- un titre ;
- un contenu ;
- des actions éventuelles ;
- un état de chargement ;
- un état vide.

Exemples de widgets :

- KPI
- Calendrier
- Tâches
- Notifications
- Activités
- Projets récents
- Derniers devis
- Leads récents

---

# 5. Cartes KPI

Les KPI affichent les indicateurs les plus importants.

Exemples :

- Nombre de Leads
- Opportunités ouvertes
- Devis envoyés
- Projets actifs
- Taux de conversion
- Chiffre d'affaires
- Tâches en retard

Chaque carte KPI comprend :

- un titre ;
- une valeur principale ;
- une évolution (si disponible) ;
- une icône (optionnelle).

Les KPI doivent être faciles à comparer.

---

# 6. Graphiques

Les graphiques permettent de visualiser les tendances.

Types recommandés :

- Courbe (Line Chart)
- Barres (Bar Chart)
- Secteurs (Pie Chart)
- Aires (Area Chart)

Chaque graphique doit :

- posséder un titre ;
- afficher une légende si nécessaire ;
- permettre une lecture rapide ;
- utiliser les couleurs officielles du Design System.

Les graphiques ne doivent jamais être utilisés lorsqu'un tableau est plus pertinent.

---

# 7. Tableaux

Les tableaux présentent des listes d'informations.

Exemples :

- Derniers projets
- Derniers devis
- Leads récents
- Activités
- Notifications

Les tableaux doivent permettre :

- tri ;
- filtrage ;
- pagination ;
- accès rapide aux détails.

---

# 8. Filtres

Le Dashboard peut proposer des filtres globaux.

Exemples :

- période ;
- équipe ;
- client ;
- projet ;
- statut.

Les filtres doivent être facilement réinitialisables.

---

# 9. Personnalisation

Selon les droits de l'utilisateur, le Dashboard peut permettre :

- réorganiser les widgets ;
- masquer des widgets ;
- enregistrer une disposition ;
- personnaliser les filtres par défaut.

Les personnalisations sont enregistrées par utilisateur.

---

# 10. États

Chaque widget doit gérer les états suivants :

## Loading

Affichage Skeleton.

---

## Empty

Aucune donnée disponible.

---

## Error

Erreur de chargement.

---

## Success

Affichage normal des données.

---

## Refresh

Mise à jour des informations.

Les changements d'état doivent être fluides et ne pas perturber la navigation.

---

# 11. Responsive

## Mobile

- widgets empilés ;
- graphiques simplifiés ;
- tableaux adaptés ou remplacés par des listes.

---

## Tablette

- grille sur deux colonnes lorsque pertinent.

---

## Desktop

- grille sur plusieurs colonnes ;
- exploitation complète de l'espace disponible.

Les informations critiques doivent rester visibles sur toutes les tailles d'écran.

---

# 12. Accessibilité

Le Dashboard doit :

- être entièrement navigable au clavier ;
- respecter les contrastes WCAG AA ;
- fournir des alternatives textuelles aux graphiques lorsque nécessaire ;
- annoncer les mises à jour importantes aux technologies d'assistance.

---

# 13. Bonnes pratiques

✔ Afficher les KPI les plus importants en premier.

✔ Limiter le nombre de widgets visibles simultanément.

✔ Utiliser des titres explicites.

✔ Mettre en avant les actions prioritaires.

✔ Garder une structure stable entre les rôles.

✔ Rafraîchir les données de manière contrôlée.

---

# 14. Anti-patterns

Les pratiques suivantes sont à éviter :

✘ Surcharger le Dashboard avec trop de widgets.

✘ Utiliser plusieurs graphiques représentant la même information.

✘ Afficher des données non pertinentes pour le rôle de l'utilisateur.

✘ Mélanger des actions critiques et secondaires dans un même widget.

✘ Modifier fréquemment la disposition des éléments.

---

# 15. Références

- UI Foundation
- Layout System
- Grid System
- Components Library
- Cards
- Responsive Design
- Accessibility
- UX Guidelines