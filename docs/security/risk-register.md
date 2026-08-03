# Security Risk Register — Zawena Platform

> Produit : Zawena Platform
>
> Document : Security Risk Register
>
> Version : 1.0
>
> Statut : Living Document
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Security Team

---

# Table des matières

1. Objectif
2. Gestion du registre
3. Méthode d'évaluation
4. Niveaux de risque
5. Registre des risques
6. Traitement des risques
7. Révision
8. Références

---

# 1. Objectif

Le registre des risques centralise l'ensemble des risques de sécurité identifiés sur Zawena Platform.

Il permet :

- d'identifier les menaces ;
- d'évaluer leur impact ;
- de prioriser les actions ;
- de suivre les plans de traitement.

Ce document est vivant.

---

# 2. Gestion du registre

Chaque risque possède :

- un identifiant unique ;
- un propriétaire ;
- un niveau de risque ;
- un plan de traitement ;
- un statut.

---

# 3. Méthode d'évaluation

Le niveau de risque est calculé selon :

```text
Probabilité × Impact
```

Échelle :

| Valeur | Signification |
|---------|---------------|
| 1 | Très faible |
| 2 | Faible |
| 3 | Moyen |
| 4 | Élevé |
| 5 | Critique |

---

# 4. Niveaux de risque

| Score | Niveau |
|--------|---------|
| 1–4 | Faible |
| 5–9 | Moyen |
| 10–16 | Élevé |
| 17–25 | Critique |

---

# 5. Registre des risques

| ID | Risque | Actif | Probabilité | Impact | Niveau | Contrôle associé | Responsable | Statut |
|----|---------|--------|-------------|--------|---------|------------------|-------------|--------|
| RISK-001 | Compromission compte administrateur | Auth | 3 | 5 | Élevé | SEC-AC-001 | Security | Ouvert |
| RISK-002 | Fuite clé API | Secrets | 2 | 5 | Élevé | SEC-SM-001 | Engineering | Mitigé |
| RISK-003 | Dépendance vulnérable | Frontend | 4 | 3 | Élevé | SEC-VM-001 | Engineering | En cours |
| RISK-004 | Perte de données | Database | 2 | 5 | Élevé | SEC-BK-001 | Infrastructure | Mitigé |
| RISK-005 | Indisponibilité Supabase | Backend | 2 | 5 | Élevé | SEC-DR-001 | Infrastructure | Mitigé |
| RISK-006 | Déploiement défectueux | Production | 3 | 4 | Élevé | SEC-DR-002 | Engineering | Mitigé |
| RISK-007 | Réponse tardive incident | Security | 2 | 5 | Élevé | SEC-IR-001 | Security | Mitigé |
| RISK-008 | Erreur de configuration | Infrastructure | 3 | 4 | Élevé | SEC-SD-004 | Engineering | En cours |

---

# 6. Traitement des risques

Chaque risque suit le processus :

Identification

↓

Évaluation

↓

Traitement

↓

Validation

↓

Suivi

↓

Clôture

---

# 7. Révision

Le registre est révisé :

- chaque trimestre ;
- après un incident majeur ;
- après un audit ;
- avant chaque version majeure.

---

# 8. Références

- Security Policy
- Security Controls
- Vulnerability Management
- Incident Response