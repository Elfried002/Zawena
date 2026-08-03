# Access Control Policy — Zawena Platform

> Produit : Zawena Platform
>
> Document : Access Control Policy
>
> Version : 1.0
>
> Statut : Draft
>
> Dernière mise à jour : 03 Août 2026
>
> Propriétaire : Security Team

---

# Table des matières

1. Objectif
2. Principes
3. Modèle de contrôle d'accès
4. Authentification
5. Autorisation
6. Rôles
7. Permissions
8. Row Level Security (RLS)
9. Sessions
10. Journalisation
11. Security Controls
12. Bonnes pratiques
13. Anti-patterns
14. Références

---

# 1. Objectif

Ce document définit les règles de contrôle d'accès de Zawena Platform.

Les objectifs sont :

- protéger les données ;
- limiter les privilèges ;
- empêcher les accès non autorisés ;
- assurer la traçabilité des actions.

Toutes les fonctionnalités doivent appliquer ces règles.

---

# 2. Principes

Le contrôle d'accès repose sur :

- Least Privilege
- Need-to-Know
- Zero Trust
- Defense in Depth
- Separation of Duties

Aucun utilisateur ne possède plus de droits que nécessaire.

---

# 3. Modèle de contrôle d'accès

Zawena utilise un modèle **RBAC (Role-Based Access Control)**.

Le rôle attribué à un utilisateur détermine :

- les modules accessibles ;
- les actions autorisées ;
- les données consultables ;
- les opérations possibles.

Les permissions sont évaluées à chaque requête.

---

# 4. Authentification

L'authentification est assurée par **Supabase Auth**.

Méthodes prévues :

- Email / Mot de passe
- Vérification Email
- Réinitialisation du mot de passe

Évolutions futures :

- OAuth
- MFA
- SSO

Toutes les connexions doivent être sécurisées via HTTPS.

---

# 5. Autorisation

Après authentification, chaque requête est soumise à une vérification d'autorisation.

Les décisions sont basées sur :

- le rôle ;
- les permissions ;
- les politiques RLS ;
- le contexte de la requête.

Une authentification valide ne garantit jamais l'autorisation d'accéder à une ressource.

---

# 6. Rôles

Les principaux rôles sont :

## Super Administrator

Accès complet à la plateforme.

---

## Administrator

Gestion de son organisation.

---

## Sales

Gestion commerciale.

---

## Project Manager

Gestion des projets.

---

## Developer

Accès aux projets et tâches techniques.

---

## Support

Gestion des demandes d'assistance.

---

## Client

Accès limité à ses propres données.

---

## Visitor

Accès uniquement au site public.

---

# 7. Permissions

Les permissions suivent une logique CRUD.

Exemples :

```text
projects.read

projects.create

projects.update

projects.delete

quotes.read

crm.manage

cms.publish

users.invite

settings.update
```

Les permissions sont regroupées par domaine métier.

---

# 8. Row Level Security (RLS)

Toutes les tables sensibles utilisent les politiques RLS de PostgreSQL.

Les politiques doivent garantir qu'un utilisateur ne peut accéder qu'aux données auxquelles il est autorisé.

Aucune requête ne doit contourner les politiques RLS.

Les politiques sont versionnées avec les migrations.

---

# 9. Sessions

Les sessions doivent :

- être invalidées lors de la déconnexion ;
- expirer après une période d'inactivité selon la configuration de sécurité ;
- être renouvelées de manière sécurisée.

Les jetons d'authentification doivent être protégés contre les usages non autorisés.

---

# 10. Journalisation

Les événements suivants doivent être journalisés :

- connexion ;
- déconnexion ;
- échec d'authentification ;
- changement de rôle ;
- modification des permissions ;
- accès aux ressources sensibles.

Les journaux doivent être protégés contre les modifications non autorisées.

---

# 11. Security Controls

## SEC-AC-001

Contrôle :

Authentification obligatoire pour toutes les ressources privées.

Priorité :

Critique

Implémentation :

Supabase Auth

---

## SEC-AC-002

Contrôle :

Autorisation basée sur les rôles.

Priorité :

Critique

Implémentation :

RBAC

---

## SEC-AC-003

Contrôle :

Application systématique des politiques RLS.

Priorité :

Critique

Implémentation :

PostgreSQL Row Level Security

---

## SEC-AC-004

Contrôle :

Journalisation des événements sensibles.

Priorité :

Élevée

Implémentation :

Audit Logs

---

## SEC-AC-005

Contrôle :

Révision périodique des droits d'accès.

Priorité :

Élevée

Implémentation :

Audit de sécurité

---

# 12. Bonnes pratiques

✔ Appliquer le principe du moindre privilège.

✔ Vérifier les permissions côté serveur.

✔ Utiliser RLS sur toutes les données métier.

✔ Révoquer rapidement les accès inutiles.

✔ Journaliser les opérations sensibles.

✔ Réaliser des revues régulières des droits.

---

# 13. Anti-patterns

Les pratiques suivantes sont interdites :

✘ Vérifier les permissions uniquement côté client.

✘ Accorder des droits d'administrateur par défaut.

✘ Désactiver RLS.

✘ Partager des comptes utilisateurs.

✘ Utiliser des permissions codées en dur dans plusieurs endroits.

✘ Contourner les contrôles d'accès via une Edge Function ou une API.

---

# 14. Références

- Security Policy
- Permissions Architecture
- Authentication Architecture
- Database Architecture
- Secure Development
- Secrets Management