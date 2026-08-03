# SOC 2 Trust Services Criteria Mapping — Zawena Platform

> Produit : Zawena Platform
>
> Document : SOC 2 Controls Mapping
>
> Référentiel : AICPA SOC 2 Trust Services Criteria (TSC)
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
3. Trust Services Criteria
4. Méthodologie
5. Matrice de conformité
6. Écarts identifiés
7. Plan d'amélioration
8. Révision
9. Références

---

# 1. Objectif

Ce document établit la correspondance entre les Trust Services Criteria (TSC) de SOC 2 et les contrôles internes de Zawena Platform.

Il permet de :

- mesurer l'alignement avec SOC 2 ;
- identifier les écarts ;
- préparer une éventuelle démarche de certification ;
- centraliser les preuves de conformité.

---

# 2. Portée

Cette cartographie couvre les cinq catégories SOC 2 :

- Security
- Availability
- Processing Integrity
- Confidentiality
- Privacy

---

# 3. Trust Services Criteria

## CC — Common Criteria

Contrôles généraux applicables à l'ensemble de la plateforme.

---

## A — Availability

Disponibilité des services.

---

## PI — Processing Integrity

Exactitude et fiabilité des traitements.

---

## C — Confidentiality

Protection des informations confidentielles.

---

## P — Privacy

Protection des données personnelles.

---

# 4. Méthodologie

Chaque exigence SOC 2 est reliée à :

- un contrôle SEC-* ;
- un document interne ;
- des preuves ;
- un niveau d'implémentation.

---

# 5. Matrice de conformité

| Critère SOC 2 | Description | Contrôle Zawena | Documents | Preuves | Statut | Responsable |
|---------------|-------------|-----------------|-----------|----------|--------|-------------|
| CC1 | Gouvernance | SEC-POL-001 | security-policy.md | Politique approuvée | ✅ | Security |
| CC2 | Communication | SEC-IR-005 | incident-response.md | Rapports d'incidents | 🟡 | Security |
| CC3 | Gestion des risques | SEC-RISK-001 | risk-register.md | Registre des risques | ✅ | Compliance |
| CC4 | Surveillance | SEC-MET-001 | security-metrics.md | Tableau de bord sécurité | 🟡 | Security |
| CC5 | Contrôle des accès | SEC-AC-001 | access-control.md | RBAC + RLS | ✅ | Engineering |
| CC6 | Sécurité logique | SEC-AC-002 | access-control.md | Configuration Auth | ✅ | Engineering |
| CC7 | Détection des incidents | SEC-IR-001 | incident-response.md | Procédure IR | ✅ | Security |
| CC8 | Gestion des changements | SEC-SD-001 | secure-development.md | Git + CI/CD | 🟡 | Engineering |
| CC9 | Gestion des fournisseurs | SEC-SM-001 | secrets-management.md | Configuration Cloud | 🟡 | DevSecOps |
| A1 | Disponibilité | SEC-DR-001 | disaster-recovery.md | PRA | ✅ | Infrastructure |
| PI1 | Intégrité des traitements | SEC-SD-002 | secure-development.md | Tests automatisés | 🟡 | Engineering |
| C1 | Confidentialité | SEC-SM-002 | secrets-management.md | Rotation des secrets | ✅ | DevSecOps |
| P1 | Données personnelles | SEC-GDPR-001 | gdpr-mapping.md | Registre RGPD | 🔵 | Compliance |

---

# 6. Écarts identifiés

Axes d'amélioration :

- MFA
- SSO
- Journalisation centralisée
- SIEM
- Gestion avancée des fournisseurs
- Classification automatique des données

---

# 7. Plan d'amélioration

## Court terme

- MFA
- Logs centralisés
- Monitoring avancé

---

## Moyen terme

- SIEM
- SSO
- Classification des données

---

## Long terme

- Pré-audit SOC 2
- Audit Type I
- Audit Type II

---

# 8. Révision

La cartographie est revue :

- tous les 6 mois ;
- après chaque audit ;
- après un changement majeur.

---

# 9. Références

- Security Policy
- Security Controls
- Risk Register
- Security Metrics
- SOC 2 Trust Services Criteria