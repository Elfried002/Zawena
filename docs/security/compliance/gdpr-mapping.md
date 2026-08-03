# GDPR (RGPD) Compliance Mapping — Zawena Platform

> Produit : Zawena Platform
>
> Document : GDPR Compliance Mapping
>
> Référentiel : Règlement (UE) 2016/679 (RGPD)
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
3. Principes du RGPD
4. Catégories de données
5. Cartographie des exigences
6. Droits des personnes concernées
7. Mesures techniques et organisationnelles
8. Écarts identifiés
9. Plan d'amélioration
10. Révision
11. Références

---

# 1. Objectif

Ce document décrit la manière dont Zawena Platform répond aux principales exigences du Règlement Général sur la Protection des Données (RGPD).

Il permet :

- d'identifier les données personnelles ;
- de documenter les mesures de protection ;
- de préparer les audits de conformité ;
- de démonorer les bonnes pratiques de protection des données.

Il ne constitue pas une déclaration de conformité juridique.

---

# 2. Portée

Cette cartographie couvre :

- Application Web
- CRM
- CMS
- Dashboard
- Authentification
- Base de données
- APIs
- Stockage
- Support client

---

# 3. Principes du RGPD

Les traitements de données doivent respecter :

- Licéité
- Loyauté
- Transparence
- Limitation des finalités
- Minimisation des données
- Exactitude
- Limitation de la conservation
- Intégrité
- Confidentialité
- Responsabilité (Accountability)

---

# 4. Catégories de données

## Données d'identification

- Nom
- Prénom
- Adresse e-mail
- Téléphone

---

## Données professionnelles

- Société
- Fonction
- Pays
- Secteur d'activité

---

## Données techniques

- Adresse IP
- Navigateur
- Journaux
- Sessions

---

## Données métier

- Devis
- Projets
- Tickets
- Documents

---

# 5. Cartographie des exigences

| Exigence RGPD | Contrôles Zawena | Documents | Fonctionnalités | Statut |
|---------------|------------------|------------|-----------------|--------|
| Base légale | SEC-GDPR-001 | privacy-policy.md | Inscription | 🔵 |
| Information des utilisateurs | SEC-GDPR-002 | privacy-policy.md | Website | 🔵 |
| Consentement | SEC-GDPR-003 | cookies-policy.md | Cookies | 🔵 |
| Protection des données | SEC-SM-* | secrets-management.md | Database | ✅ |
| Contrôle d'accès | SEC-AC-* | access-control.md | Tous les modules | ✅ |
| Sauvegardes | SEC-BK-* | backup-policy.md | Infrastructure | ✅ |
| Journalisation | SEC-IR-* | incident-response.md | Backend | 🟡 |
| Gestion des incidents | SEC-IR-* | incident-response.md | Tous | ✅ |

---

# 6. Droits des personnes concernées

La plateforme doit permettre, selon les obligations applicables :

- droit d'accès ;
- droit de rectification ;
- droit à l'effacement ;
- droit à la limitation du traitement ;
- droit d'opposition ;
- droit à la portabilité des données.

Les modalités d'exercice de ces droits devront être documentées et implémentées.

---

# 7. Mesures techniques et organisationnelles

Mesures prévues :

- RBAC
- RLS
- Chiffrement
- Sauvegardes
- Journalisation
- Gestion des secrets
- Développement sécurisé
- Gestion des vulnérabilités

---

# 8. Écarts identifiés

Évolutions prévues :

- Export des données utilisateur.
- Suppression automatisée des comptes.
- Gestion des demandes RGPD.
- Registre des traitements.
- Politique de conservation des données.
- Gestion des violations de données personnelles.

---

# 9. Plan d'amélioration

## Court terme

- Politique de confidentialité.
- Gestion des cookies.
- Export des données.

---

## Moyen terme

- Automatisation des demandes RGPD.
- Journal des traitements.
- Rétention configurable.

---

## Long terme

- Tableau de bord conformité.
- Vérifications automatiques.
- Audit annuel.

---

# 10. Révision

Revue :

- annuelle ;
- après une évolution majeure ;
- après une évolution réglementaire.

---

# 11. Références

- Privacy Policy
- Cookies Policy
- Access Control
- Security Policy
- Security Controls
- Règlement (UE) 2016/679 (RGPD)