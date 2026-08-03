# NIST Cybersecurity Framework (CSF) 2.0 Mapping — Zawena Platform

> Produit : Zawena Platform
>
> Document : NIST CSF 2.0 Mapping
>
> Référentiel : NIST Cybersecurity Framework 2.0
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Security & Compliance Team

---

# Table des matières

1. Objectif
2. Portée
3. Vue d'ensemble du NIST CSF 2.0
4. Méthodologie
5. Cartographie des fonctions
6. Évaluation de maturité
7. Écarts identifiés
8. Plan d'amélioration
9. Références

---

# 1. Objectif

Ce document établit la correspondance entre le NIST Cybersecurity Framework 2.0 et les contrôles de sécurité internes de Zawena Platform.

Il permet de :

- mesurer la maturité cybersécurité ;
- suivre les progrès ;
- identifier les écarts ;
- faciliter les audits internes.

---

# 2. Portée

Cette cartographie couvre :

- Gouvernance
- Développement
- Infrastructure
- Cloud
- DevSecOps
- Continuité d'activité
- Gestion des incidents
- Gestion des risques

---

# 3. Vue d'ensemble du NIST CSF 2.0

Le NIST CSF repose sur six fonctions.

```text
GOVERN
        ↓
IDENTIFY
        ↓
PROTECT
        ↓
DETECT
        ↓
RESPOND
        ↓
RECOVER
```

Chaque fonction est représentée dans la documentation de Zawena.

---

# 4. Méthodologie

Chaque fonction est reliée :

- aux contrôles SEC-* ;
- aux documents de sécurité ;
- aux preuves disponibles ;
- au niveau de mise en œuvre.

---

# 5. Cartographie des fonctions

## GOVERN (GV)

Objectif :

Piloter la cybersécurité.

| Catégorie | Contrôles Zawena | Documents | Statut |
|------------|-----------------|-----------|--------|
| Gouvernance | SEC-POL-001 | security-policy.md | ✅ |
| Gestion des risques | SEC-RISK-001 | risk-register.md | ✅ |
| Roadmap sécurité | SEC-CMP-001 | security-roadmap.md | ✅ |
| KPI sécurité | SEC-MET-001 | security-metrics.md | ✅ |

---

## IDENTIFY (ID)

Objectif :

Comprendre les actifs, risques et dépendances.

| Catégorie | Contrôles | Documents | Statut |
|------------|-----------|-----------|--------|
| Inventaire | SEC-CMP-001 | security-roadmap.md | 🟡 |
| Gestion des risques | SEC-RISK-001 | risk-register.md | ✅ |
| Classification des données | SEC-GDPR-001 | gdpr-mapping.md | 🔵 |

---

## PROTECT (PR)

Objectif :

Empêcher les incidents.

| Domaine | Contrôles | Documents | Statut |
|----------|-----------|-----------|--------|
| RBAC | SEC-AC-001 | access-control.md | ✅ |
| RLS | SEC-AC-003 | access-control.md | ✅ |
| Développement sécurisé | SEC-SD-* | secure-development.md | ✅ |
| Secrets | SEC-SM-* | secrets-management.md | ✅ |
| Sauvegardes | SEC-BK-* | backup-policy.md | ✅ |

---

## DETECT (DE)

Objectif :

Détecter rapidement les incidents.

| Domaine | Contrôles | Documents | Statut |
|----------|-----------|-----------|--------|
| Logs | SEC-IR-003 | incident-response.md | 🟡 |
| CodeQL | SEC-VM-002 | vulnerability-management.md | 🟡 |
| Monitoring | SEC-MET-001 | security-metrics.md | 🟡 |

---

## RESPOND (RS)

Objectif :

Réagir efficacement.

| Domaine | Contrôles | Documents | Statut |
|----------|-----------|-----------|--------|
| Incident Response | SEC-IR-* | incident-response.md | ✅ |
| Gestion de crise | SEC-DR-004 | disaster-recovery.md | ✅ |
| Communication | SEC-IR-005 | incident-response.md | ✅ |

---

## RECOVER (RC)

Objectif :

Restaurer les services.

| Domaine | Contrôles | Documents | Statut |
|----------|-----------|-----------|--------|
| Sauvegardes | SEC-BK-* | backup-policy.md | ✅ |
| PRA | SEC-DR-* | disaster-recovery.md | ✅ |
| Tests de restauration | SEC-BK-003 | backup-policy.md | ✅ |

---

# 6. Évaluation de maturité

| Fonction | Niveau actuel | Objectif |
|-----------|---------------|-----------|
| Govern | 4/5 | 5/5 |
| Identify | 3/5 | 5/5 |
| Protect | 4/5 | 5/5 |
| Detect | 3/5 | 5/5 |
| Respond | 4/5 | 5/5 |
| Recover | 4/5 | 5/5 |

---

# 7. Écarts identifiés

Les principaux écarts concernent :

- Inventaire automatisé des actifs.
- SIEM.
- Détection temps réel.
- CSPM.
- Threat Intelligence.
- Threat Modeling.
- MFA.
- SSO.

Ces actions sont intégrées à la Security Roadmap.

---

# 8. Plan d'amélioration

## Court terme

- MFA
- Secret Scanning
- CodeQL
- Centralisation des logs

---

## Moyen terme

- SIEM
- Monitoring temps réel
- CSPM

---

## Long terme

- Détection comportementale
- Threat Hunting
- Conformité continue

---

# 9. Références

- Security Policy
- Security Controls
- Security Metrics
- Risk Register
- Incident Response
- Disaster Recovery
- NIST Cybersecurity Framework 2.0