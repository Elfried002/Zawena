# Non-Functional Requirements — Zawena Platform

> Produit : Zawena Platform
>
> Document : Non-Functional Requirements
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Objectif
2. Portée
3. Classification des exigences
4. Exigences non fonctionnelles
5. Critères de validation
6. Références

---

# 1. Objectif

Ce document définit les exigences non fonctionnelles (Non-Functional Requirements - NFR) de Zawena Platform.

Contrairement aux exigences fonctionnelles, ces exigences décrivent les qualités attendues du système : performance, sécurité, disponibilité, accessibilité, maintenabilité, évolutivité, observabilité, compatibilité et conformité.

Ces exigences servent de référence pour :

- l'architecture technique ;
- le développement ;
- les tests de performance ;
- les audits de sécurité ;
- les déploiements ;
- la maintenance.

---

# 2. Portée

Ces exigences s'appliquent à l'ensemble des modules :

- Website
- Authentication
- Dashboard
- CRM
- Quotes
- Projects
- Client Portal
- CMS
- Notifications
- Settings

---

# 3. Classification des exigences

Les exigences sont regroupées par domaine :

- Performance
- Disponibilité
- Sécurité
- Fiabilité
- Scalabilité
- Maintenabilité
- Observabilité
- Accessibilité
- Compatibilité
- UX
- Confidentialité
- Sauvegarde
- Journalisation
- Conformité

Chaque exigence est identifiée par :

NFR-XXX

---

# 4. Exigences non fonctionnelles

# Performance

## NFR-PERF-001

Le temps de chargement d'une page ne doit pas dépasser 2 secondes dans des conditions normales d'utilisation.

Priorité : Critique

---

## NFR-PERF-002

Les appels API doivent répondre en moins de 500 ms pour 95 % des requêtes.

---

## NFR-PERF-003

Le Dashboard doit être entièrement chargé en moins de 3 secondes.

---

## NFR-PERF-004

Les recherches globales doivent retourner un résultat en moins de 1 seconde.

---

## NFR-PERF-005

La génération d'un PDF doit être réalisée en moins de 5 secondes.

---

# Disponibilité

## NFR-AVAIL-001

La plateforme doit viser une disponibilité annuelle minimale de 99,9 %.

---

## NFR-AVAIL-002

Les opérations de maintenance doivent être planifiées et annoncées.

---

## NFR-AVAIL-003

Les interruptions non planifiées doivent être journalisées.

---

# Sécurité

## NFR-SEC-001

Toutes les communications doivent utiliser HTTPS/TLS.

---

## NFR-SEC-002

Les mots de passe doivent être stockés sous forme de hash sécurisé.

---

## NFR-SEC-003

Les permissions doivent être contrôlées côté serveur.

---

## NFR-SEC-004

Chaque requête authentifiée doit être vérifiée avant traitement.

---

## NFR-SEC-005

Les journaux d'audit doivent être protégés contre les modifications.

---

## NFR-SEC-006

Les données sensibles ne doivent jamais être exposées dans les journaux.

---

# Fiabilité

## NFR-REL-001

Les transactions critiques doivent être atomiques.

---

## NFR-REL-002

Le système doit éviter la création de doublons.

---

## NFR-REL-003

Les erreurs doivent être détectées et journalisées.

---

# Scalabilité

## NFR-SCALE-001

L'architecture doit permettre l'ajout de nouveaux modules sans refonte majeure.

---

## NFR-SCALE-002

La plateforme doit supporter plusieurs organisations (architecture multi-tenant).

---

## NFR-SCALE-003

Les services doivent pouvoir évoluer horizontalement.

---

# Maintenabilité

## NFR-MAIN-001

Le code doit respecter les standards définis dans la documentation de développement.

---

## NFR-MAIN-002

Les composants doivent être réutilisables.

---

## NFR-MAIN-003

Les modules doivent être faiblement couplés.

---

## NFR-MAIN-004

Toute fonctionnalité doit être documentée.

---

# Observabilité

## NFR-OBS-001

Toutes les erreurs critiques doivent être journalisées.

---

## NFR-OBS-002

Les métriques principales doivent être collectées.

---

## NFR-OBS-003

Les événements métier doivent être tracés.

---

# Accessibilité

## NFR-ACC-001

L'interface doit être navigable au clavier.

---

## NFR-ACC-002

Les contrastes doivent respecter les recommandations WCAG 2.1 niveau AA.

---

## NFR-ACC-003

Les images doivent disposer d'un texte alternatif lorsque nécessaire.

---

# Compatibilité

## NFR-COMP-001

La plateforme doit fonctionner sur les principaux navigateurs modernes.

---

## NFR-COMP-002

L'application doit être responsive.

---

## NFR-COMP-003

Les fonctionnalités principales doivent être utilisables sur mobile, tablette et ordinateur.

---

# Expérience utilisateur

## NFR-UX-001

Les interfaces doivent rester cohérentes sur tous les modules.

---

## NFR-UX-002

Les messages d'erreur doivent être compréhensibles.

---

## NFR-UX-003

Chaque action importante doit fournir un retour visuel.

---

# Confidentialité

## NFR-PRIV-001

Chaque utilisateur ne doit accéder qu'aux données autorisées.

---

## NFR-PRIV-002

Les informations personnelles doivent être protégées conformément à la politique de confidentialité.

---

# Sauvegarde

## NFR-BACKUP-001

Les sauvegardes de la base de données doivent être automatisées.

---

## NFR-BACKUP-002

Les sauvegardes doivent être vérifiées régulièrement.

---

## NFR-BACKUP-003

Une procédure de restauration doit être documentée et testée.

---

# Journalisation

## NFR-LOG-001

Toutes les actions sensibles doivent être journalisées.

---

## NFR-LOG-002

Les journaux doivent inclure :

- utilisateur ;
- date ;
- heure ;
- action ;
- résultat.

---

## NFR-LOG-003

Les journaux doivent être consultables par les administrateurs autorisés.

---

# Conformité

## NFR-COMP-001

La plateforme doit respecter les obligations légales applicables dans les pays où elle est déployée.

---

## NFR-COMP-002

Les utilisateurs doivent pouvoir consulter les documents légaux.

---

## NFR-COMP-003

Le consentement relatif aux cookies doit être géré lorsque requis.

---

# 5. Critères de validation

Les exigences non fonctionnelles seront validées à l'aide de :

- tests de performance ;
- tests de charge ;
- tests de sécurité ;
- audits de code ;
- audits d'accessibilité ;
- tests de compatibilité ;
- tests de restauration ;
- monitoring de production.

Chaque NFR devra être associée à un ou plusieurs cas de test.

---

# 6. Références

- PRD
- MVP Definition
- Functional Requirements
- Security Policy
- Architecture
- Development Standards
- OWASP ASVS
- ISO/IEC 25010
- WCAG 2.1