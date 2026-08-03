# Architecture Decision Records (ADR)

> Dossier : `docs/decisions/`
>
> Version : 1.0
>
> Dernière mise à jour : 03 Août 2026

---

# Table des matières

1. Objectif
2. Qu'est-ce qu'un ADR ?
3. Pourquoi utiliser des ADR ?
4. Quand créer un ADR ?
5. Cycle de vie d'un ADR
6. Structure standard
7. Conventions de nommage
8. ADR existants
9. Créer un nouvel ADR
10. Bonnes pratiques
11. Anti-patterns
12. Références

---

# 1. Objectif

Ce dossier centralise toutes les **Architecture Decision Records (ADR)** de Zawena Platform.

Les ADR permettent de documenter les décisions importantes prises pendant la conception et l'évolution de la plateforme.

Chaque ADR répond à une question simple :

> **Pourquoi cette décision a-t-elle été prise ?**

L'objectif est de conserver le contexte, les alternatives étudiées et les conséquences de chaque choix afin de faciliter la maintenance, l'évolution du produit et l'intégration de nouveaux collaborateurs.

---

# 2. Qu'est-ce qu'un ADR ?

Un ADR (Architecture Decision Record) est un document court qui décrit une décision significative concernant l'architecture, la technologie, la sécurité, le design ou toute autre orientation structurante du projet.

Un ADR ne décrit pas seulement la décision finale.

Il explique également :

- le contexte ;
- le problème à résoudre ;
- les options envisagées ;
- les critères de décision ;
- les conséquences du choix effectué.

---

# 3. Pourquoi utiliser des ADR ?

Les ADR permettent notamment de :

- conserver l'historique des décisions ;
- éviter les débats déjà tranchés ;
- faciliter l'intégration de nouveaux membres ;
- documenter les compromis techniques ;
- améliorer la traçabilité des choix d'architecture ;
- justifier les évolutions futures.

---

# 4. Quand créer un ADR ?

Un ADR doit être créé lorsqu'une décision est susceptible d'avoir un impact durable sur le projet.

Exemples :

- choix d'une technologie ;
- changement d'architecture ;
- adoption d'un framework ;
- modification importante du modèle de données ;
- changement du système d'authentification ;
- adoption d'un nouveau Design System ;
- évolution majeure des politiques de sécurité.

Les décisions mineures ou temporaires ne nécessitent généralement pas d'ADR.

---

# 5. Cycle de vie d'un ADR

Chaque ADR possède un statut.

| Statut | Description |
|---------|-------------|
| Proposed | Proposition en cours d'évaluation |
| Accepted | Décision approuvée et appliquée |
| Deprecated | Décision devenue obsolète mais conservée pour l'historique |
| Superseded | Décision remplacée par un nouvel ADR |

Lorsqu'une décision est remplacée, l'ancien ADR n'est jamais supprimé. Il est marqué comme **Superseded** et référence le nouvel ADR.

---

# 6. Structure standard

Tous les ADR suivent la même structure.

1. Statut
2. Contexte
3. Problématique
4. Facteurs de décision
5. Options étudiées
6. Décision
7. Justification
8. Conséquences
9. Compromis (Trade-offs)
10. Évolutions futures
11. Révision
12. Documents associés

Cette structure garantit une documentation homogène et facilite la lecture.

---

# 7. Conventions de nommage

Les ADR sont numérotés de manière séquentielle.

Format :

```text
ADR-001-title.md
ADR-002-title.md
ADR-003-title.md
```

Le numéro d'un ADR ne change jamais, même si son contenu évolue.

Les nouveaux ADR reçoivent toujours le numéro suivant disponible.

---

# 8. ADR existants

| ADR | Titre | Statut |
|------|-------|--------|
| ADR-001 | Brand Identity and Product Naming | Accepted |
| ADR-002 | Technology Stack Selection | Accepted |
| ADR-003 | Database Architecture | Accepted |
| ADR-004 | Authentication Architecture | Accepted |
| ADR-005 | Design System Adoption | Accepted |

Cette liste est mise à jour à chaque création d'un nouvel ADR.

---

# 9. Créer un nouvel ADR

Avant de créer un ADR :

1. Vérifier qu'aucun ADR existant ne traite déjà du sujet.
2. Définir clairement le problème à résoudre.
3. Identifier les options possibles.
4. Documenter les critères de décision.
5. Justifier le choix retenu.
6. Décrire les conséquences attendues.

Chaque ADR doit être relu avant d'être marqué comme **Accepted**.

---

# 10. Bonnes pratiques

✔ Documenter uniquement les décisions importantes.

✔ Expliquer le contexte avant la décision.

✔ Décrire les alternatives étudiées.

✔ Être transparent sur les compromis.

✔ Mettre à jour les statuts lorsque les décisions évoluent.

✔ Référencer les documents liés.

---

# 11. Anti-patterns

✘ Créer un ADR pour chaque petite décision.

✘ Modifier l'historique d'un ADR sans conserver la trace des changements.

✘ Supprimer un ADR devenu obsolète.

✘ Oublier de documenter les conséquences.

✘ Utiliser un ADR pour documenter une simple tâche technique.

---

# 12. Références

- Architecture Documentation
- Technology Decision Records
- Product Architecture
- Engineering Guidelines
- Project Governance