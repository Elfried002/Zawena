# Sitemap — Zawena Platform

> Produit : Zawena Platform
>
> Document : Sitemap
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
2. Architecture globale
3. Site public
4. Authentification
5. Application
6. Portail Client
7. Administration
8. APIs
9. Évolution future
10. Références

---

# 1. Objectif

Ce document présente l'organisation complète des pages, modules et espaces fonctionnels de Zawena Platform.

Le Sitemap sert de référence pour :

- les développeurs ;
- les designers UX/UI ;
- les testeurs ;
- la documentation ;
- l'architecture du produit.

---

# 2. Architecture globale

```
Zawena Platform
│
├── Website (Public)
├── Authentication
├── Dashboard
├── CRM
├── Quotes
├── Projects
├── Client Portal
├── CMS
├── Notifications
└── Settings
```

---

# 3. Site public

```
/
│
├── Accueil
├── Services
│   ├── Développement Web
│   ├── Applications
│   ├── Cybersécurité
│   ├── IA & Automatisation
│   └── Consulting
│
├── Réalisations
│
├── Blog
│   ├── Liste des articles
│   └── Article
│
├── FAQ
│
├── Contact
│
├── Demande de devis
│
├── Mentions légales
│
├── Politique de confidentialité
│
└── Connexion
```

---

# 4. Authentification

```
/auth

├── Connexion
├── Inscription (optionnelle selon le modèle retenu)
├── Mot de passe oublié
├── Réinitialisation
├── Vérification Email
└── Déconnexion
```

---

# 5. Application

```
/dashboard
│
├── Tableau de bord
│
├── CRM
│   ├── Leads
│   ├── Prospects
│   ├── Entreprises
│   ├── Contacts
│   ├── Opportunités
│   ├── Activités
│   └── Notes
│
├── Quotes
│   ├── Tous les devis
│   ├── Nouveau devis
│   ├── Détail
│   └── Historique
│
├── Projects
│   ├── Tous les projets
│   ├── Tableau Kanban
│   ├── Calendrier
│   ├── Phases
│   ├── Jalons
│   ├── Livrables
│   ├── Documents
│   └── Discussions
│
├── CMS
│   ├── Pages
│   ├── Blog
│   ├── Services
│   ├── FAQ
│   ├── Études de cas
│   ├── Médias
│   └── SEO
│
├── Notifications
│
└── Paramètres
```

---

# 6. Portail Client

```
/client

├── Dashboard
├── Mes projets
├── Livrables
├── Documents
├── Devis
├── Contrats
├── Notifications
└── Mon profil
```

---

# 7. Administration

```
/settings

├── Organisation
├── Utilisateurs
├── Rôles
├── Permissions
├── Sécurité
├── Branding
├── SMTP
├── Fournisseur IA
├── Intégrations
├── Journal d'audit
└── Préférences
```

---

# 8. APIs

```
/api

├── Authentication
├── CRM
├── Quotes
├── Projects
├── CMS
├── Notifications
├── Client Portal
└── Settings
```

---

# 9. Évolution future

Les futures versions de Zawena pourront ajouter :

```
Marketplace

Application Mobile

Chat Temps Réel

Facturation

Paiement en ligne

Workflows IA

Automatisations

Analytics avancées

Multi-tenant avancé
```

---

# 10. Références

- PRD
- MVP Definition
- Feature Specifications
- User Stories
- User Flows
- Roadmap