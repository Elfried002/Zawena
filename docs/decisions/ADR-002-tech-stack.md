# ADR-002 — Technology Stack Selection

> ADR ID : ADR-002
>
> Titre : Technology Stack Selection
>
> Statut : Accepted
>
> Date : 03 Août 2026
>
> Décideurs : Founder, Engineering Team
>
> Type : Architecture Decision

---

# Table des matières

1. Statut
2. Contexte
3. Problématique
4. Facteurs de décision
5. Options étudiées
6. Décision
7. Justification des choix
8. Conséquences
9. Compromis (Trade-offs)
10. Évolutions futures
11. Révision
12. Documents associés

---

# 1. Statut

**Accepted**

Cette décision constitue la stack technique officielle de Zawena Platform.

---

# 2. Contexte

Zawena est une plateforme SaaS moderne destinée aux entreprises.

Le projet nécessite une architecture capable de répondre aux contraintes suivantes :

- développement rapide du MVP ;
- forte évolutivité ;
- sécurité intégrée ;
- faible coût d'exploitation au démarrage ;
- maintenance simplifiée ;
- expérience développeur moderne ;
- intégration native avec les services cloud.

L'objectif est de privilégier une stack mature, documentée et largement adoptée.

---

# 3. Problématique

Quelle stack technologique permet de développer Zawena rapidement tout en garantissant une architecture évolutive, maintenable et sécurisée ?

---

# 4. Facteurs de décision

Les critères retenus sont :

- maturité de la technologie ;
- communauté active ;
- documentation ;
- performances ;
- sécurité ;
- productivité des développeurs ;
- évolutivité ;
- coût d'exploitation ;
- facilité de recrutement de développeurs ;
- intégration avec l'écosystème moderne.

---

# 5. Options étudiées

## Front-end

### React

✔ Grande communauté

✔ Écosystème mature

✔ Excellente intégration TypeScript

✔ Compatible avec Vite

---

### Vue

Très bonne expérience développeur.

Communauté plus réduite.

---

### Angular

Très complet.

Mais plus complexe pour un MVP.

---

### Svelte

Très performant.

Écosystème encore moins mature.

---

## Backend

### Supabase

Backend-as-a-Service basé sur PostgreSQL.

---

### Firebase

Très mature.

Mais fortement orienté NoSQL.

---

### Appwrite

Open Source.

Écosystème moins mature.

---

### Backend Node.js personnalisé

Très flexible.

Temps de développement plus important.

---

# 6. Décision

La stack officielle de Zawena est la suivante.

| Domaine | Technologie retenue |
|----------|---------------------|
| Front-end | React |
| Langage | TypeScript |
| Build Tool | Vite |
| UI | Tailwind CSS |
| Components | shadcn/ui |
| Backend | Supabase |
| Base de données | PostgreSQL |
| Authentification | Supabase Auth |
| Stockage | Supabase Storage |
| API | REST + Edge Functions |
| Déploiement | Vercel |
| Versioning | Git + GitHub |

Cette stack constitue la référence officielle du projet.

---

# 7. Justification des choix

## React

Choisi pour :

- sa maturité ;
- son immense communauté ;
- sa flexibilité ;
- son excellente intégration avec TypeScript.

---

## TypeScript

Choisi afin de :

- réduire les erreurs ;
- améliorer la maintenabilité ;
- faciliter la collaboration ;
- améliorer l'expérience développeur.

---

## Vite

Choisi pour :

- son démarrage extrêmement rapide ;
- ses temps de compilation réduits ;
- sa simplicité de configuration.

---

## Tailwind CSS

Choisi afin de :

- construire rapidement des interfaces modernes ;
- réduire le CSS personnalisé ;
- améliorer la cohérence visuelle.

---

## shadcn/ui

Choisi pour :

- ses composants accessibles ;
- sa personnalisation complète ;
- l'absence de dépendance à une bibliothèque de composants propriétaire.

---

## Supabase

Choisi pour :

- PostgreSQL natif ;
- Auth intégrée ;
- Storage intégré ;
- Row Level Security ;
- Edge Functions ;
- API générées automatiquement.

---

## PostgreSQL

Choisi pour :

- sa robustesse ;
- sa conformité SQL ;
- ses performances ;
- son évolutivité ;
- son excellente compatibilité avec Supabase.

---

## Vercel

Choisi pour :

- son intégration native avec Vite ;
- son déploiement continu ;
- sa simplicité d'utilisation.

---

# 8. Conséquences

## Positives

- développement rapide ;

- faible coût initial ;

- architecture moderne ;

- maintenance simplifiée ;

- sécurité native ;

- stack largement documentée.

---

## Négatives

- dépendance partielle à Supabase ;

- nécessité de suivre les évolutions de certains services cloud ;

- certaines personnalisations avancées peuvent nécessiter du développement spécifique.

---

# 9. Compromis (Trade-offs)

Les principaux compromis sont :

- privilégier la rapidité de développement plutôt qu'une architecture entièrement personnalisée ;

- accepter une dépendance modérée à Supabase afin d'accélérer le lancement ;

- utiliser des services managés pour réduire la charge opérationnelle.

Ces compromis sont considérés comme acceptables au regard des objectifs actuels du projet.

---

# 10. Évolutions futures

La stack pourra évoluer si :

- les besoins de montée en charge le justifient ;

- certaines limitations techniques apparaissent ;

- des contraintes réglementaires imposent des changements ;

- une technologie apporte un avantage démontré.

Toute évolution majeure devra faire l'objet d'un nouvel ADR.

---

# 11. Révision

Cette décision est revue :

- lors d'une évolution majeure de la plateforme ;

- avant toute migration importante ;

- au minimum une fois par an.

---

# 12. Documents associés

- Architecture Overview
- Development Guidelines
- Database Design
- Authentication Architecture
- Technology Watch
- ADR-003 Database
- ADR-004 Authentication
- ADR-005 Design System