# Support Process — Zawena Platform

> Produit : Zawena Platform
>
> Document : Support Process
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Customer Support Team

---

# Table des matières

1. Objectif
2. Portée
3. Principes
4. Types de demandes
5. Workflow de traitement
6. Priorisation
7. Gestion des escalades
8. Clôture des tickets
9. KPI du support
10. Bonnes pratiques
11. Anti-patterns
12. Révision
13. Références

---

# 1. Objectif

Ce document décrit le processus officiel de gestion du support client de Zawena Platform.

Les objectifs sont :

- assurer une prise en charge rapide des demandes ;
- standardiser le traitement des tickets ;
- respecter les engagements de niveau de service (SLA) ;
- améliorer la satisfaction client ;
- capitaliser sur les retours d'expérience.

---

# 2. Portée

Cette procédure s'applique à toutes les demandes adressées au support concernant :

- l'utilisation de la plateforme ;
- les incidents techniques ;
- les bugs ;
- les demandes d'assistance ;
- les demandes d'évolution ;
- les questions administratives.

---

# 3. Principes

Chaque demande doit être :

- enregistrée ;
- qualifiée ;
- priorisée ;
- traitée ;
- documentée ;
- clôturée.

Toutes les communications avec le client doivent être conservées dans l'historique du ticket.

---

# 4. Types de demandes

## Incident

Exemple :

- plateforme indisponible ;
- erreur bloquante ;
- problème d'authentification.

---

## Bug

Exemple :

- anomalie fonctionnelle ;
- erreur d'affichage ;
- comportement inattendu.

---

## Assistance

Exemple :

- aide à l'utilisation ;
- configuration ;
- accompagnement.

---

## Demande d'évolution

Exemple :

- nouvelle fonctionnalité ;
- amélioration d'une fonctionnalité existante ;
- optimisation du produit.

Ces demandes sont transmises à l'équipe Produit pour évaluation.

---

## Demande administrative

Exemple :

- facturation ;
- abonnement ;
- informations contractuelles.

---

# 5. Workflow de traitement

```text
Réception

↓

Création du ticket

↓

Qualification

↓

Priorisation

↓

Affectation

↓

Traitement

↓

Validation

↓

Clôture

↓

Enquête de satisfaction
```

---

# 6. Priorisation

Les tickets sont classés selon leur impact et leur urgence.

| Priorité | Description | Exemple |
|-----------|-------------|----------|
| P1 | Critique | Plateforme indisponible |
| P2 | Élevée | Fonction bloquante |
| P3 | Moyenne | Bug mineur |
| P4 | Faible | Question ou demande d'information |

Les délais de prise en charge sont définis dans :

`docs/operations/sla-policy.md`

---

# 7. Gestion des escalades

Un ticket peut être escaladé lorsque :

- il dépasse le délai prévu ;
- une expertise spécifique est requise ;
- plusieurs clients sont impactés ;
- un incident de sécurité est suspecté.

### Niveaux d'escalade

Niveau 1 :

Support Client

↓

Niveau 2 :

Équipe Technique

↓

Niveau 3 :

Engineering

↓

Niveau 4 :

Security / Direction (si nécessaire)

Toutes les escalades sont enregistrées dans le ticket.

---

# 8. Clôture des tickets

Un ticket peut être clôturé lorsque :

- la demande est résolue ;
- le client confirme la résolution, lorsque cela est applicable ;
- la documentation est complétée ;
- les actions réalisées sont enregistrées.

Les tickets clôturés restent consultables à des fins d'historique et d'analyse.

---

# 9. KPI du support

| KPI | Objectif |
|------|----------|
| Temps moyen de première réponse (MTTA) | < 1 heure |
| Temps moyen de résolution (MTTR) | < 4 heures |
| Tickets résolus dans le SLA | ≥ 95 % |
| Taux de satisfaction client (CSAT) | ≥ 90 % |
| Tickets réouverts | < 5 % |
| Temps moyen d'escalade | < 30 minutes |

Les indicateurs sont suivis dans :

`docs/operations/operational-kpis.md`

---

# 10. Bonnes pratiques

✔ Accuser réception rapidement.

✔ Documenter toutes les actions réalisées.

✔ Informer régulièrement le client de l'avancement.

✔ Respecter les priorités définies.

✔ Identifier les causes racines des incidents récurrents.

✔ Alimenter la base de connaissances avec les solutions réutilisables.

---

# 11. Anti-patterns

✘ Laisser un ticket sans réponse.

✘ Clôturer un ticket sans vérification.

✘ Modifier la priorité sans justification.

✘ Ignorer les escalades nécessaires.

✘ Ne pas documenter la résolution.

---

# 12. Révision

Cette procédure est revue :

- après une évolution importante du support ;
- après une modification des SLA ;
- après un incident majeur ;
- au minimum une fois par an.

---

# 13. Références

- SLA Policy
- Operational KPIs
- Incident Runbooks
- Client Onboarding
- Service Catalog
- Business Continuity