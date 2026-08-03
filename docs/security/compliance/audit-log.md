# Security & Compliance Audit Register — Zawena Platform

> Produit : Zawena Platform
>
> Document : Security & Compliance Audit Register
>
> Version : 1.0
>
> Statut : Living Document
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Security & Compliance Team

---

# Table des matières

1. Objectif
2. Portée
3. Types d'audit
4. Cycle d'audit
5. Registre des audits
6. Gestion des constats
7. Actions correctives (CAPA)
8. Preuves d'audit
9. KPI d'audit
10. Calendrier
11. Révision
12. Références

---

# 1. Objectif

Ce document centralise l'ensemble des audits réalisés sur Zawena Platform.

Il permet de :

- suivre les audits réalisés ;
- documenter les constats ;
- suivre les non-conformités ;
- piloter les actions correctives ;
- conserver les preuves d'audit.

---

# 2. Portée

Les audits peuvent concerner :

- Gouvernance
- Développement
- DevSecOps
- Infrastructure
- Cloud
- Base de données
- Authentification
- Gestion des accès
- Sauvegardes
- Continuité d'activité
- Protection des données
- Conformité réglementaire

---

# 3. Types d'audit

## Audit interne

Réalisé par l'équipe interne.

Objectifs :

- vérifier la conformité ;
- identifier les améliorations ;
- préparer un audit externe.

---

## Audit externe

Réalisé par un prestataire ou un organisme indépendant.

Objectifs :

- évaluation indépendante ;
- préparation à une certification ;
- validation des contrôles.

---

## Audit technique

Exemples :

- revue d'architecture ;
- revue de code ;
- revue DevSecOps ;
- revue Cloud.

---

## Audit de conformité

Référentiels :

- ISO 27001
- SOC 2
- NIST CSF
- OWASP ASVS
- RGPD

---

# 4. Cycle d'audit

Chaque audit suit le processus suivant :

```text
Planification

↓

Préparation

↓

Exécution

↓

Collecte des preuves

↓

Analyse

↓

Rapport

↓

Plan d'actions

↓

Suivi

↓

Clôture
```

---

# 5. Registre des audits

| ID | Date | Type | Domaine | Responsable | Résultat | Statut |
|----|------|------|----------|-------------|----------|--------|
| AUD-001 | AAAA-MM-JJ | Interne | Sécurité | Security Team | Conforme | Planifié |
| AUD-002 | AAAA-MM-JJ | Technique | DevSecOps | Engineering | Conforme avec réserves | Planifié |
| AUD-003 | AAAA-MM-JJ | Conformité | ISO 27001 | Compliance | À compléter | Planifié |

---

# 6. Gestion des constats

Chaque constat possède :

- un identifiant ;
- une criticité ;
- une description ;
- un responsable ;
- une échéance ;
- un statut.

## Niveaux de criticité

| Niveau | Description |
|----------|-------------|
| Critique | Risque immédiat |
| Élevé | Correction prioritaire |
| Moyen | Correction planifiée |
| Faible | Amélioration |

---

## Exemple

| ID | Audit | Criticité | Description | Responsable | Échéance | Statut |
|----|-------|-----------|-------------|-------------|-----------|--------|
| FIND-001 | AUD-001 | Élevée | MFA non implémenté | Engineering | AAAA-MM-JJ | Ouvert |

---

# 7. Actions Correctives et Préventives (CAPA)

Chaque non-conformité génère une CAPA.

| CAPA | Constat | Action | Responsable | Échéance | Statut |
|-------|----------|---------|-------------|-----------|--------|
| CAPA-001 | FIND-001 | Déployer MFA | Engineering | AAAA-MM-JJ | En cours |

Le suivi des CAPA est obligatoire jusqu'à leur clôture.

---

# 8. Preuves d'audit

Chaque audit doit être accompagné de preuves.

Exemples :

- rapports CodeQL ;
- résultats Dependabot ;
- captures de configuration ;
- journaux d'audit ;
- résultats des tests ;
- exports GitHub Actions ;
- rapports de pentest ;
- preuves de restauration ;
- rapports de conformité.

Toutes les preuves doivent être archivées de manière sécurisée.

---

# 9. KPI d'audit

| KPI | Objectif |
|------|----------|
| Audits réalisés | 100 % |
| CAPA clôturées | >95 % |
| Non-conformités critiques ouvertes | 0 |
| Audits réalisés dans les délais | 100 % |
| Rapports publiés | 100 % |

---

# 10. Calendrier recommandé

| Audit | Fréquence |
|---------|-----------|
| Audit interne sécurité | Trimestriel |
| Revue des accès | Trimestrielle |
| Audit DevSecOps | Semestriel |
| Audit de conformité | Annuel |
| Pentest externe | Annuel |
| Test PRA | Semestriel |

---

# 11. Révision

Ce registre est mis à jour :

- après chaque audit ;
- après chaque pentest ;
- après chaque incident majeur ;
- après chaque revue de conformité.

---

# 12. Références

- Security Policy
- Security Controls
- Risk Register
- Security Metrics
- Incident Response
- ISO 19011
- ISO 27001
- SOC 2
- NIST CSF
- OWASP ASVS