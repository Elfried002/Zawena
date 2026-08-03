# Security Review Checklist — Zawena Platform

> Version : 1.0

---

# Objectif

Checklist utilisée :

- avant un Merge
- avant un Déploiement
- avant une Release

---

# Développement

□ TypeScript compile

□ ESLint OK

□ Tests OK

□ Code Review effectuée

□ Documentation mise à jour

---

# Authentification

□ Auth vérifiée

□ Permissions serveur

□ RBAC

□ RLS

□ Sessions

---

# Secrets

□ Aucun secret Git

□ Variables Vercel

□ Variables GitHub

□ Rotation si nécessaire

---

# Base de données

□ Migration validée

□ Sauvegarde réalisée

□ Rollback documenté

□ RLS testée

---

# API

□ Validation Zod

□ Gestion erreurs

□ Rate Limiting

□ Logs

---

# Frontend

□ Responsive

□ Accessibilité

□ Design System

□ Permissions UI

---

# Infrastructure

□ CI/CD

□ Monitoring

□ Backup

□ Disaster Recovery

---

# Incident Response

□ Logs actifs

□ Alertes

□ Documentation

□ Contacts

---

# Validation finale

□ Security Team

□ Engineering

□ Product Owner

□ Release Manager

---

# Résultat

□ Validation

□ Validation avec réserves

□ Refus de mise en production