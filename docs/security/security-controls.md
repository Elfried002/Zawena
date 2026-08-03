# Security Controls Catalog — Zawena Platform

> Version : 1.0

---

# Objectif

Ce document centralise tous les contrôles de sécurité utilisés dans Zawena.

Chaque contrôle possède :

- un identifiant ;
- une priorité ;
- un propriétaire ;
- une méthode de vérification.

---

# Classification

| Priorité | Description |
|-----------|-------------|
| Critique | Contrôle indispensable |
| Élevée | Contrôle fortement recommandé |
| Moyenne | Contrôle complémentaire |
| Faible | Amélioration continue |

---

# Catalogue

| ID | Contrôle | Domaine | Priorité | Vérification | Responsable |
|----|----------|----------|-----------|---------------|-------------|
| SEC-AC-001 | Authentification obligatoire | Access Control | Critique | Audit | Security |
| SEC-AC-002 | RBAC | Access Control | Critique | Tests | Engineering |
| SEC-AC-003 | RLS PostgreSQL | Database | Critique | Audit SQL | Engineering |
| SEC-SD-001 | Validation Zod | Secure Development | Critique | Code Review | Engineering |
| SEC-SD-002 | Permissions serveur | Secure Development | Critique | Tests | Engineering |
| SEC-SM-001 | Aucun secret dans Git | Secrets | Critique | Secret Scanning | DevSecOps |
| SEC-SM-002 | Rotation des secrets | Secrets | Élevée | Audit | DevSecOps |
| SEC-VM-001 | Analyse Dependabot | Vulnerability | Critique | GitHub | Engineering |
| SEC-VM-002 | Analyse CodeQL | Vulnerability | Élevée | CI/CD | Engineering |
| SEC-BK-001 | Sauvegarde automatique | Backup | Critique | Logs | Infrastructure |
| SEC-BK-002 | Sauvegardes chiffrées | Backup | Critique | Audit | Infrastructure |
| SEC-DR-001 | Plan de reprise | Disaster Recovery | Critique | Test PRA | Infrastructure |
| SEC-IR-001 | Plan réponse incident | Incident Response | Critique | Audit | Security |

---

# Cycle de vie

Chaque contrôle suit :

Planification

↓

Implémentation

↓

Validation

↓

Surveillance

↓

Amélioration

---

# Révision

Revue semestrielle.

---

# Références

Tous les documents du dossier Security.