# ISO/IEC 27001:2022 Controls Mapping — Zawena Platform

> Produit : Zawena Platform
>
> Document : ISO/IEC 27001 Controls Mapping
>
> Référentiel : ISO/IEC 27001:2022 (Annexe A)
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
3. Méthodologie
4. Niveaux de conformité
5. Matrice des contrôles
6. Écarts identifiés
7. Plan d'amélioration
8. Révision
9. Références

---

# 1. Objectif

Ce document établit la correspondance entre les contrôles de l'ISO/IEC 27001:2022 et les contrôles de sécurité internes de Zawena Platform.

Il permet :

- d'évaluer le niveau d'alignement ;
- d'identifier les écarts ;
- de planifier les améliorations ;
- de préparer d'éventuels audits internes.

Ce document ne constitue pas une preuve de certification.

---

# 2. Portée

Cette cartographie couvre :

- Gouvernance
- Contrôle d'accès
- Développement sécurisé
- Gestion des secrets
- Gestion des vulnérabilités
- Sauvegardes
- Reprise après sinistre
- Réponse aux incidents
- DevSecOps

---

# 3. Méthodologie

Chaque contrôle ISO est associé à :

- un ou plusieurs contrôles internes (`SEC-*`) ;
- les documents de référence ;
- des preuves attendues ;
- un niveau de mise en œuvre.

---

# 4. Niveaux de conformité

| Statut | Description |
|---------|-------------|
| ✅ Implémenté | Contrôle mis en œuvre et documenté |
| 🟡 Partiellement implémenté | Contrôle en cours de déploiement |
| 🔵 Planifié | Contrôle prévu dans la roadmap |
| ❌ Non implémenté | Aucun contrôle actuellement |

---

# 5. Matrice des contrôles

| Contrôle ISO 27001 | Description | Contrôle Zawena | Documents | Preuves attendues | Statut | Responsable |
|--------------------|-------------|-----------------|-----------|-------------------|--------|-------------|
| A.5.1 | Politiques de sécurité | SEC-POL-001 | security-policy.md | Politique approuvée | ✅ | Security |
| A.5.15 | Contrôle des accès | SEC-AC-001 à SEC-AC-005 | access-control.md | Configuration RBAC + RLS | ✅ | Engineering |
| A.5.17 | Authentification | SEC-AC-001 | access-control.md | Configuration Supabase Auth | ✅ | Engineering |
| A.5.23 | Sécurité des services Cloud | SEC-SM-001 | secrets-management.md | Configuration Vercel / Supabase | 🟡 | DevSecOps |
| A.5.30 | Préparation TIC à la continuité | SEC-DR-001 | disaster-recovery.md | Plan PRA | ✅ | Infrastructure |
| A.8.8 | Gestion des vulnérabilités | SEC-VM-001 à SEC-VM-005 | vulnerability-management.md | Rapports Dependabot / CodeQL | ✅ | Engineering |
| A.8.9 | Gestion de configuration | SEC-SD-001 | secure-development.md | Git + CI/CD | 🟡 | Engineering |
| A.8.13 | Sauvegardes | SEC-BK-001 à SEC-BK-005 | backup-policy.md | Journaux de sauvegarde | ✅ | Infrastructure |
| A.8.15 | Journalisation | SEC-IR-003 | incident-response.md | Audit Logs | 🟡 | Security |
| A.8.16 | Surveillance des activités | SEC-VM-002 | vulnerability-management.md | Rapports de surveillance | 🟡 | Security |

---

# 6. Écarts identifiés

Les principaux axes d'amélioration sont :

- Déploiement du MFA.
- Mise en place d'un SSO.
- Centralisation des journaux de sécurité.
- SIEM.
- Exercices réguliers de gestion de crise.
- Pentests externes annuels.
- Programme de sensibilisation sécurité.

Chaque écart est intégré à la Security Roadmap.

---

# 7. Plan d'amélioration

## Court terme (0–6 mois)

- MFA
- GitHub CodeQL
- Secret Scanning
- Tests du PRA

---

## Moyen terme (6–12 mois)

- SIEM
- SSO
- CSPM
- Pentests

---

## Long terme (12–24 mois)

- Pré-audit ISO 27001
- Revues de conformité automatisées
- Tableaux de bord de conformité
- Amélioration continue des contrôles

---

# 8. Révision

Cette matrice est revue :

- tous les 6 mois ;
- après une évolution majeure de l'architecture ;
- après un audit interne ;
- avant tout audit externe.

---

# 9. Références

- Security Policy
- Security Controls
- Risk Register
- Security Roadmap
- ISO/IEC 27001:2022