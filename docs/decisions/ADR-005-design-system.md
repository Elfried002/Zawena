# ADR-005 — Design System Adoption

> ADR ID : ADR-005
>
> Titre : Design System Adoption
>
> Statut : Accepted
>
> Date : 03 Août 2026
>
> Décideurs : Founder, Product Team, Design Team, Engineering Team
>
> Type : UI/UX & Architecture Decision

---

# Table des matières

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

---

# 1. Statut

**Accepted**

Cette décision définit l'approche officielle de conception des interfaces utilisateur de Zawena Platform.

---

# 2. Contexte

Zawena est une plateforme SaaS amenée à évoluer avec de nombreux modules, écrans et composants.

Sans Design System, plusieurs risques apparaissent rapidement :

- incohérence visuelle ;
- duplication des composants ;
- dette technique front-end ;
- difficultés de maintenance ;
- expérience utilisateur inégale.

Le projet nécessite une base commune pour garantir une interface cohérente et évolutive.

---

# 3. Problématique

Comment assurer une cohérence visuelle, une excellente expérience utilisateur et une forte productivité de développement tout au long de la vie du produit ?

---

# 4. Facteurs de décision

Les critères retenus sont :

- cohérence graphique ;
- réutilisabilité des composants ;
- accessibilité ;
- maintenabilité ;
- personnalisation ;
- performances ;
- compatibilité avec React ;
- compatibilité avec Tailwind CSS ;
- faible dette technique.

---

# 5. Options étudiées

## Composants développés sans Design System

### Avantages

- liberté totale ;
- aucun cadre imposé.

### Inconvénients

- duplication rapide ;
- incohérences visuelles ;
- maintenance difficile.

---

## Bibliothèque UI complète (Material UI, Ant Design...)

### Avantages

- nombreux composants prêts à l'emploi ;
- développement rapide.

### Inconvénients

- personnalisation plus limitée ;
- identité visuelle moins distinctive ;
- dépendance forte à une bibliothèque externe.

---

## Tailwind CSS + shadcn/ui (Option retenue)

### Avantages

- composants réutilisables ;
- personnalisation complète ;
- excellente intégration React ;
- accessibilité native ;
- faible dette technique ;
- contrôle total du code.

### Inconvénients

- nécessite la mise en place et la maintenance du Design System.

---

# 6. Décision

Zawena adopte un Design System basé sur :

- Tailwind CSS ;
- shadcn/ui ;
- Design Tokens ;
- composants réutilisables ;
- principes d'accessibilité ;
- documentation centralisée.

Tous les nouveaux composants doivent respecter ce Design System.

---

# 7. Justification

## Cohérence

Tous les écrans utilisent les mêmes composants, couleurs, espacements, typographies et comportements.

---

## Productivité

Les composants existants sont réutilisés plutôt que recréés.

Cela réduit le temps de développement et facilite les évolutions.

---

## Accessibilité

Les composants suivent les bonnes pratiques en matière :

- d'accessibilité clavier ;
- de contraste ;
- de navigation ;
- de lecteurs d'écran.

---

## Maintenabilité

Une modification apportée à un composant partagé bénéficie automatiquement à toutes les interfaces qui l'utilisent.

---

## Évolutivité

Le Design System permet d'ajouter facilement :

- nouveaux thèmes ;
- nouveaux composants ;
- nouvelles variantes ;
- nouvelles interfaces.

---

# 8. Conséquences

## Positives

- expérience utilisateur cohérente ;

- développement plus rapide ;

- maintenance simplifiée ;

- meilleure accessibilité ;

- réduction des composants dupliqués ;

- identité visuelle forte.

---

## Négatives

- investissement initial plus important ;

- nécessité de documenter les composants ;

- gouvernance nécessaire pour éviter les écarts.

---

# 9. Compromis (Trade-offs)

Les principaux compromis sont :

- consacrer du temps à construire un Design System afin de réduire les coûts de maintenance futurs ;

- imposer des standards communs plutôt que laisser chaque développeur créer ses propres composants.

Ce compromis est considéré comme essentiel pour un produit destiné à évoluer sur le long terme.

---

# 10. Évolutions futures

Le Design System pourra évoluer avec :

- de nouveaux composants ;
- de nouveaux thèmes ;
- le mode sombre ;
- des variantes spécifiques aux clients Enterprise ;
- des améliorations d'accessibilité ;
- des optimisations des performances.

Toute évolution importante du Design System devra être documentée.

---

# 11. Révision

Cette décision est revue :

- après une évolution majeure du Design System ;

- avant une refonte graphique ;

- au minimum une fois par an.

---

# 12. Documents associés

- Design System
- UI Components
- Brand Guidelines
- Accessibility Guidelines
- Frontend Guidelines
- ADR-002 Technology Stack