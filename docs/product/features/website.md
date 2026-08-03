# Feature Specification — Site Web Public

> Produit : Zawena Platform
>
> Module : Website
>
> Identifiant : FEAT-WEB
>
> Version : 1.0
>
> Statut : MVP
>
> Priorité : Critique
>
> Dernière mise à jour : 02 Août 2026
>
> Propriétaire : Product Management – Zawena

---

# Table des matières

1. Objectif
2. Vue d'ensemble
3. Pourquoi ce module existe
4. Valeur métier
5. Personas concernés
6. Cas d'utilisation
7. Fonctionnalités
8. Architecture fonctionnelle
9. Pages et écrans
10. Composants UI
11. États
12. Règles métier
13. Permissions
14. Notifications
15. Journalisation
16. Modèle de données
17. APIs et intégrations
18. SEO
19. Analytics
20. Sécurité
21. Performance
22. Accessibilité
23. Responsive Design
24. Gestion des erreurs
25. KPIs
26. Limites du MVP
27. Évolutions V2+
28. Critères d'acceptation
29. Dépendances
30. Références

---

# 1. Objectif

Le module Website constitue la vitrine publique de Zawena.

Il doit permettre à un visiteur de :

- comprendre rapidement ce qu'est Zawena ;
- découvrir ses services ;
- comprendre les problèmes que Zawena peut résoudre ;
- évaluer la crédibilité de l'entreprise ;
- consulter ses réalisations ;
- entrer en contact ;
- demander un devis ;
- être transformé progressivement en prospect qualifié.

Le site doit également constituer le principal canal numérique d'acquisition organique de Zawena.

---

# 2. Vue d'ensemble

Le site web représente la couche publique de Zawena Platform.

Il est accessible sans authentification et communique avec plusieurs modules internes.

Architecture fonctionnelle simplifiée :

```text
Visiteur
   │
   ▼
Site Zawena
   │
   ├── Présentation
   ├── Services
   ├── Réalisations
   ├── Contenus
   ├── Contact
   └── Demande de devis
          │
          ▼
       Backend
          │
          ├── CRM
          ├── CMS
          ├── Notifications
          ├── Analytics
          └── Dashboard Admin
```

Le site ne doit donc pas être considéré comme une application indépendante.

Il constitue une interface publique directement connectée au système d'information de Zawena.

---

# 3. Pourquoi ce module existe

Zawena commence son développement par une activité de services autour de :

1. AI Agents
2. AI Automation
3. AI Integration
4. AI Applications
5. Software Engineering
6. Cybersecurity
7. AI Consulting

L'entreprise doit pouvoir présenter ces compétences et transformer l'intérêt généré en opportunités commerciales.

Le site doit résoudre quatre problématiques principales :

### Visibilité

Permettre à Zawena d'être trouvée et comprise.

### Crédibilité

Présenter une image professionnelle et cohérente.

### Acquisition

Transformer les visiteurs en prospects.

### Qualification

Collecter suffisamment d'informations pour comprendre les besoins des prospects avant un premier échange.

---

# 4. Valeur métier

Le Website contribue directement aux objectifs suivants :

- acquisition de prospects ;
- génération de demandes de devis ;
- développement de la notoriété ;
- amélioration de la crédibilité ;
- référencement naturel ;
- collecte de données commerciales ;
- présentation des réalisations ;
- distribution des contenus marketing.

Il constitue le début du funnel commercial :

```text
Visiteur
   ↓
Visiteur engagé
   ↓
Lead
   ↓
Prospect
   ↓
Prospect qualifié
   ↓
Opportunité
   ↓
Client
```

---

# 5. Personas concernés

## Persona principal

### Visitor

Consulte le site sans authentification.

Référence :

`../personas/visitor.md`

---

## Persona secondaire

### Prospect

A manifesté un intérêt pour Zawena.

Référence :

`../personas/prospect.md`

---

## Personas internes indirectement concernés

### Sales

Reçoit et qualifie les opportunités commerciales.

### Administrator

Gère le contenu et les demandes entrantes.

### Super Administrator

Administre la configuration globale.

---

# 6. Cas d'utilisation

## UC-WEB-001 — Découvrir Zawena

Le visiteur arrive sur la page d'accueil et souhaite comprendre l'activité de l'entreprise.

Résultat attendu :

Il comprend en quelques secondes :

- ce que fait Zawena ;
- pour qui ;
- quelle valeur elle apporte ;
- quelle action effectuer ensuite.

---

## UC-WEB-002 — Consulter un service

Le visiteur souhaite comprendre une offre particulière.

Exemple :

AI Automation.

Le site présente :

- le problème ;
- la solution ;
- les bénéfices ;
- les cas d'utilisation ;
- le processus ;
- un CTA.

---

## UC-WEB-003 — Demander un devis

Le visiteur possède un besoin concret.

Il complète le formulaire de demande de devis.

Le système :

1. valide les données ;
2. enregistre la demande ;
3. crée ou met à jour le contact ;
4. crée une opportunité dans le CRM ;
5. notifie l'équipe concernée ;
6. confirme la réception au prospect.

---

## UC-WEB-004 — Contacter Zawena

Le visiteur souhaite poser une question.

Il utilise le formulaire de contact.

La demande est enregistrée et transmise à l'équipe.

---

## UC-WEB-005 — Vérifier la crédibilité

Le visiteur consulte :

- À propos ;
- Réalisations ;
- Études de cas ;
- partenaires ;
- méthodologie ;
- contenus.

---

## UC-WEB-006 — Consulter du contenu

Le visiteur consulte un article ou une ressource publiée par Zawena.

Objectifs :

- apporter de la valeur ;
- démontrer l'expertise ;
- améliorer le SEO ;
- générer une conversion future.

---

# 7. Fonctionnalités

## FEAT-WEB-001 — Navigation principale

La navigation doit permettre d'accéder rapidement aux sections principales.

Éléments minimum :

- Accueil
- Services
- Réalisations
- À propos
- Blog
- Contact
- CTA « Demander un devis »

---

## FEAT-WEB-002 — Page d'accueil

La page d'accueil doit présenter :

- proposition de valeur ;
- services ;
- bénéfices ;
- méthodologie ;
- éléments de confiance ;
- réalisations sélectionnées ;
- CTA ;
- FAQ ou objections principales.

---

## FEAT-WEB-003 — Catalogue des services

Une page doit permettre de consulter l'ensemble des services proposés.

Services initiaux :

- AI Agents
- AI Automation
- AI Integration
- AI Applications
- Software Engineering
- Cybersecurity
- AI Consulting

---

## FEAT-WEB-004 — Pages Service

Chaque service dispose d'une présentation détaillée.

Structure recommandée :

```text
Hero
↓
Problème
↓
Solution Zawena
↓
Cas d'utilisation
↓
Bénéfices
↓
Méthodologie
↓
Technologies / Expertise
↓
FAQ
↓
CTA
```

---

## FEAT-WEB-005 — Réalisations

Le site permet de présenter les projets réalisés par Zawena.

Une réalisation peut contenir :

- nom ;
- client si publiable ;
- secteur ;
- problème ;
- solution ;
- technologies ;
- résultats ;
- illustrations ;
- témoignage éventuel.

---

## FEAT-WEB-006 — Études de cas

Certaines réalisations peuvent disposer d'une étude de cas détaillée.

---

## FEAT-WEB-007 — À propos

La page présente notamment :

- Zawena ;
- vision ;
- mission ;
- valeurs ;
- histoire ;
- expertise ;
- approche.

---

## FEAT-WEB-008 — Blog / Insights

Le site permet de publier des contenus sur :

- Intelligence Artificielle ;
- automatisation ;
- développement logiciel ;
- cybersécurité ;
- transformation numérique ;
- produits Zawena.

---

## FEAT-WEB-009 — Contact

Un formulaire permet de contacter Zawena.

Champs minimum :

- nom ;
- email ;
- entreprise ;
- sujet ;
- message ;
- consentement requis le cas échéant.

---

## FEAT-WEB-010 — Demande de devis

Le formulaire de devis doit permettre de qualifier le besoin.

Informations possibles :

- identité ;
- entreprise ;
- coordonnées ;
- service recherché ;
- description du besoin ;
- budget indicatif ;
- échéance souhaitée ;
- pièces jointes si activées ;
- consentement.

Le formulaire doit rester suffisamment simple pour ne pas réduire excessivement le taux de conversion.

---

## FEAT-WEB-011 — FAQ

Le site permet d'afficher des questions fréquentes.

Les FAQ peuvent être :

- générales ;
- spécifiques à un service ;
- administrables via le CMS.

---

## FEAT-WEB-012 — Appels à l'action

Les CTA principaux sont :

- Demander un devis
- Nous contacter
- Découvrir nos services
- Parler de votre projet

Les formulations doivent respecter la charte rédactionnelle.

---

## FEAT-WEB-013 — Mentions légales

Le site doit permettre l'accès aux documents juridiques applicables.

Exemples :

- Politique de confidentialité
- Politique relative aux cookies
- Conditions applicables
- Mentions légales

---

## FEAT-WEB-014 — Consentement cookies

Lorsque requis par la configuration juridique ou les technologies utilisées, le visiteur doit pouvoir :

- accepter ;
- refuser ;
- personnaliser ses choix ;
- modifier ultérieurement son consentement.

---

## FEAT-WEB-015 — Recherche

La recherche globale n'est pas obligatoire pour le MVP.

Une architecture compatible avec son ajout futur doit néanmoins être conservée.

---

# 8. Architecture fonctionnelle

Le module Website est organisé en plusieurs domaines.

```text
Website
│
├── Navigation
│
├── Pages institutionnelles
│
├── Services
│
├── Portfolio
│
├── Blog
│
├── FAQ
│
├── Contact
│
├── Devis
│
├── SEO
│
├── Analytics
│
└── Legal
```

Le contenu éditorial administrable provient du CMS.

---

# 9. Pages et écrans

Le périmètre initial prévoit notamment :

```text
/
├── /
├── /services
├── /services/[slug]
├── /realisations
├── /realisations/[slug]
├── /a-propos
├── /blog
├── /blog/[slug]
├── /contact
├── /devis
├── /confidentialite
├── /cookies
└── /conditions
```

Le sitemap définitif est documenté dans :

`../15-sitemap.md`

---

# 10. Composants UI

Les composants principaux comprennent :

## Navigation

- Header
- Desktop Navigation
- Mobile Navigation
- CTA principal

## Contenu

- Hero
- Section
- Service Card
- Case Study Card
- Article Card
- Testimonial
- Logo Cloud
- FAQ Accordion
- Stats
- Process Steps

## Conversion

- CTA Banner
- Contact Form
- Quote Form

## Navigation secondaire

- Breadcrumb
- Pagination

## Pied de page

- Footer
- Social Links
- Legal Links

Les composants doivent provenir du Design System lorsque celui-ci définit un équivalent.

---

# 11. États

Les composants interactifs doivent prévoir au minimum :

- default ;
- hover ;
- focus ;
- active ;
- loading ;
- success ;
- error ;
- disabled.

Les formulaires doivent également gérer :

```text
Initial
↓
Editing
↓
Validating
↓
Submitting
↓
Success
```

ou :

```text
Submitting
↓
Error
↓
Correction
↓
Submitting
```

---

# 12. Règles métier

## BR-WEB-001

Une demande de devis valide doit créer une entrée exploitable par le CRM.

## BR-WEB-002

Une demande ne doit pas être perdue si l'envoi de la notification interne échoue après son enregistrement.

## BR-WEB-003

Les champs obligatoires doivent être validés côté client et côté serveur.

## BR-WEB-004

Les contenus non publiés ne doivent jamais être accessibles publiquement.

## BR-WEB-005

Une réalisation confidentielle ne peut pas être publiée.

## BR-WEB-006

Un article doit posséder un statut avant publication.

Exemples :

```text
draft
review
scheduled
published
archived
```

## BR-WEB-007

Un slug public doit être unique dans son type de contenu.

## BR-WEB-008

La suppression d'un contenu publié doit privilégier l'archivage lorsque la conservation est nécessaire.

---

# 13. Permissions

## Visiteur

Peut :

- consulter les contenus publics ;
- envoyer un formulaire ;
- gérer son consentement.

Ne peut pas :

- modifier le contenu ;
- consulter le back-office ;
- accéder aux données privées.

---

## Administrateur

Selon ses permissions :

- crée ;
- modifie ;
- publie ;
- archive les contenus.

---

## Super Administrateur

Dispose des capacités administratives globales conformément au système RBAC.

Les règles détaillées sont définies dans :

`docs/architecture/permissions.md`

---

# 14. Notifications

## Demande de devis

Après réception :

### Prospect

Reçoit une confirmation.

### Équipe Zawena

Reçoit une notification indiquant qu'une nouvelle demande est disponible.

---

## Contact

Même logique :

```text
Formulaire
↓
Enregistrement
↓
Notification interne
↓
Confirmation utilisateur
```

Une panne du système de notification ne doit pas supprimer la donnée déjà enregistrée.

---

# 15. Journalisation

Les événements pertinents peuvent inclure :

- formulaire envoyé ;
- erreur de soumission ;
- contenu publié ;
- contenu modifié ;
- contenu archivé ;
- consentement enregistré ;
- événement de conversion.

Les données sensibles ne doivent pas être copiées inutilement dans les logs.

---

# 16. Modèle de données

Entités principales potentielles :

```text
services
case_studies
articles
categories
faqs
contact_requests
quote_requests
testimonials
site_settings
seo_metadata
```

Exemple conceptuel :

```text
quote_requests

id
full_name
email
phone
company_name
service_id
project_description
budget_range
desired_timeline
status
source
created_at
updated_at
```

Le schéma définitif appartient à :

`docs/architecture/database.md`

Ce document ne constitue pas la source de vérité du schéma physique.

---

# 17. APIs et intégrations

Le Website peut communiquer avec :

- CRM ;
- CMS ;
- service email ;
- analytics ;
- stockage ;
- calendrier / prise de rendez-vous ;
- anti-spam.

Les contrats définitifs seront documentés dans :

`docs/architecture/api.md`

et :

`docs/architecture/integrations.md`

---

# 18. SEO

Le site doit être conçu pour permettre une stratégie SEO solide.

Chaque page indexable doit pouvoir définir :

- title ;
- meta description ;
- canonical URL ;
- Open Graph ;
- image sociale ;
- données structurées lorsque pertinentes.

Le système doit également prévoir :

- sitemap XML ;
- robots.txt ;
- redirections ;
- gestion des erreurs 404 ;
- URLs lisibles.

Les contenus privés, brouillons et pages techniques ne doivent pas être indexés.

---

# 19. Analytics

Le système doit permettre de mesurer au minimum :

- pages vues ;
- sessions ;
- sources d'acquisition ;
- clics sur CTA ;
- formulaires commencés ;
- formulaires envoyés ;
- demandes de devis ;
- conversions.

Événements conceptuels :

```text
page_view
service_view
cta_click
contact_started
contact_submitted
quote_started
quote_submitted
```

La solution analytics exacte est définie dans la documentation technique.

---

# 20. Sécurité

Le Website doit respecter les principes de sécurité définis par Zawena.

Mesures minimum :

- validation serveur ;
- sanitisation appropriée ;
- protection contre les injections ;
- protection XSS ;
- protection CSRF lorsque pertinente ;
- limitation des abus ;
- contrôle des fichiers téléversés ;
- gestion sécurisée des secrets ;
- HTTPS ;
- dépendances maintenues.

Les formulaires publics doivent disposer de mécanismes anti-spam adaptés.

Aucun secret applicatif ne doit être exposé côté client.

---

# 21. Performance

Le site doit privilégier :

- chargement rapide ;
- optimisation des images ;
- lazy loading lorsque pertinent ;
- réduction du JavaScript inutile ;
- cache approprié ;
- chargement optimisé des polices ;
- limitation des scripts tiers.

Les Core Web Vitals doivent être surveillés.

Les objectifs quantitatifs définitifs sont définis dans :

`09-non-functional-requirements.md`

---

# 22. Accessibilité

Objectif :

**WCAG 2.2 niveau AA** lorsque applicable.

Le site doit notamment prévoir :

- navigation clavier ;
- focus visible ;
- HTML sémantique ;
- labels explicites ;
- textes alternatifs ;
- contraste suffisant ;
- messages d'erreur compréhensibles ;
- respect de `prefers-reduced-motion` lorsque pertinent.

---

# 23. Responsive Design

Le site est conçu selon une approche responsive.

Il doit fonctionner sur :

- smartphone ;
- tablette ;
- ordinateur portable ;
- desktop.

Les fonctionnalités essentielles ne doivent pas disparaître sur mobile.

La navigation doit être adaptée à la taille de l'écran.

---

# 24. Gestion des erreurs

## 404

Une page dédiée doit :

- expliquer que la ressource n'existe pas ;
- proposer un retour vers le site ;
- fournir éventuellement des liens utiles.

## 500

Les erreurs serveur ne doivent jamais exposer :

- stack traces ;
- secrets ;
- détails techniques sensibles.

## Formulaires

Les erreurs doivent :

- identifier clairement le champ concerné ;
- expliquer la correction attendue ;
- conserver les données déjà saisies lorsque possible.

---

# 25. KPIs

## Acquisition

- visiteurs uniques ;
- sessions ;
- trafic organique ;
- sources d'acquisition.

## Engagement

- consultation des services ;
- engagement sur les contenus ;
- interactions avec les CTA.

## Conversion

- demandes de contact ;
- demandes de devis ;
- taux de conversion visiteur → lead ;
- taux de conversion lead → prospect.

## Performance

- Core Web Vitals ;
- erreurs frontend ;
- disponibilité.

## Business

- prospects générés ;
- opportunités générées ;
- valeur du pipeline attribuable au site ;
- clients issus du site.

---

# 26. Limites du MVP

Le MVP n'a pas vocation à intégrer immédiatement :

- personnalisation dynamique avancée ;
- moteur de recommandation IA ;
- chatbot IA complet ;
- recherche sémantique ;
- portail multilingue avancé ;
- A/B testing intégré ;
- marketing automation complet ;
- marketplace.

Ces éléments peuvent être ajoutés après validation du besoin.

---

# 27. Évolutions V2+

## V2

Possibilités :

- prise de rendez-vous intégrée ;
- newsletter ;
- téléchargement de ressources ;
- témoignages avancés ;
- études de cas enrichies ;
- lead scoring ;
- automatisation CRM.

## V3

Possibilités :

- assistant IA public ;
- recommandations personnalisées ;
- contenu dynamique ;
- personnalisation par secteur ;
- recherche intelligente.

## Long terme

Le site devient la porte d'entrée publique de l'ensemble de l'écosystème SaaS Zawena.

---

# 28. Critères d'acceptation

Le module Website est considéré comme fonctionnel lorsque :

- les pages publiques essentielles sont disponibles ;
- la navigation fonctionne sur les tailles d'écran supportées ;
- les services sont consultables ;
- le formulaire de contact fonctionne ;
- le formulaire de devis fonctionne ;
- les demandes sont enregistrées avant notification ;
- les demandes de devis sont exploitables par le CRM ;
- les contenus publiés peuvent être administrés ;
- les brouillons restent privés ;
- les métadonnées SEO essentielles sont configurables ;
- les pages légales sont accessibles ;
- les erreurs principales sont correctement gérées ;
- les contrôles de sécurité essentiels sont opérationnels ;
- les exigences d'accessibilité du MVP sont respectées ;
- aucun secret applicatif n'est exposé côté client.

---

# 29. Dépendances

Le module dépend notamment de :

```text
Website
│
├── CMS
├── CRM
├── Quotes
├── Notifications
├── Analytics
├── Database
└── Security
```

Une évolution de ces modules peut avoir un impact direct sur le Website.

---

# 30. Références

## Produit

- `../01-prd.md`
- `../02-product-vision.md`
- `../03-product-goals.md`
- `../04-personas.md`
- `../15-sitemap.md`

## Personas

- `../personas/visitor.md`
- `../personas/prospect.md`
- `../personas/sales.md`
- `../personas/administrator.md`

## Entreprise

- `../../company/services.md`
- `../../company/positioning.md`
- `../../company/pricing-strategy.md`

## Marque

- `../../brand/brand-guidelines.md`
- `../../brand/voice-tone.md`
- `../../brand/writing-guidelines.md`

## Design

- `../../design-system/ui.md`
- `../../design-system/ux.md`
- `../../design-system/responsive.md`
- `../../design-system/accessibility.md`

## Architecture

- `../../architecture/api.md`
- `../../architecture/database.md`
- `../../architecture/integrations.md`
- `../../architecture/security.md`

## Sécurité

- `../../security/secure-development.md`
- `../../security/access-control.md`

---

# Statut du module

| Élément | Statut |
|---|---|
| Spécification fonctionnelle | Définie |
| Personas | Définis |
| User Stories | À documenter |
| User Flows | À documenter |
| Architecture technique | À finaliser |
| Design UI | À finaliser |
| Tests | À définir |
| Développement | Non démarré |

---

> **Principe directeur :**
>
> Le site de Zawena ne doit pas simplement présenter l'entreprise.
> Il doit transformer la confiance en conversation, puis la conversation en opportunité commerciale.