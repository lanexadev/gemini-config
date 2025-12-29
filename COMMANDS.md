# 🛠️ Gemini CLI - Command Definitions

Ce document définit l'ensemble des commandes disponibles dans `gemini-cli`, leurs alias et leurs objectifs fonctionnels.

## 🚀 Core Development

Commandes essentielles pour le cycle de développement quotidien.

- **`oneshot`** : Implémentation "One-Shot". Génère le code complet pour une fonctionnalité simple ou un script autonome en une seule passe, sans itérations complexes. Idéal pour les scripts utilitaires ou les composants UI isolés.
- **`debug`** : Analyse un extrait de code, un message d'erreur ou une stack trace. Identifie la cause racine (Root Cause Analysis) et propose un correctif précis avec le code corrigé.
- **`explain`** : Pédagogue technique. Explique le fonctionnement d'un bloc de code complexe, une regex obscure ou une architecture logicielle en langage naturel clair.
- **`review`** : Agit comme un "Senior Developer". Effectue une revue de code stricte axée sur la lisibilité, la performance, la sécurité et les principes SOLID/DRY.
- **`refactor`** : Réécrit le code fourni pour l'améliorer (nettoyage, modernisation de syntaxe, simplification de la complexité cyclomatique) **sans** modifier son comportement fonctionnel.
- **`security-audit`** : Expert Cybersécurité. Scanne le code pour détecter les vulnérabilités courantes (OWASP Top 10 : XSS, Injections SQL, secrets exposés, dépendances non sécurisées).

## 🧠 APEX Methodology (Complex Features)

_Systematic implementation using Analyse-Plan-Execute-eXamine._

### Standard APEX (Projets Complets)

- **`apex 1-analyse`** : **Analyse Phase**. Ingère tout le contexte du projet (fichiers, README, user story). Produit un rapport technique détaillé identifiant les contraintes et les requis.
- **`apex 2-plan`** : **Planning Phase**. Crée une stratégie d'implémentation étape par étape ("Step-by-step Implementation Plan") basée sur l'analyse précédente.
- **`apex 3-execute`** : **Execute Phase**. Mode "Ultra Thinking". Écrit le code complet en suivant le plan validé.
- **`apex 4-examine`** : **Examine Phase**. Vérifie le code produit par rapport au plan initial, suggère des améliorations et valide la logique avant toute intégration.
- **`apex 5-tasks`** : **Task Creation**. Découpe le plan global en fichiers de tâches atomiques Markdown (ex: `task-01.md`, `task-02.md`) pour une exécution séquentielle par un agent ou un dev.

### APEX Quick (Itérations Rapides)

- **`apex-quick analyse`** : Analyse rapide du contexte courant en mémoire tampon pour donner une direction immédiate ou clarifier une ambiguïté.
- **`apex-quick plan`** : Propose une stratégie d'implémentation flash (liste à puces) directement dans la conversation.
- **`apex-quick execute`** : Génère directement le code pour une modification ciblée ou un hotfix, sans générer de fichiers de tâches.
- **`apex-quick examine`** : Relit rapidement un bout de code généré pour détecter les hallucinations ou erreurs de syntaxe évidentes.

## 🧪 Testing & Documentation

- **`test-gen`** : Génère une suite de tests unitaires (Jest, Pytest, Vitest, etc.) pour le code fourni, en insistant sur la couverture des cas limites (edge cases).
- **`doc-gen`** : Génère automatiquement la documentation technique. Peut produire de la JSDoc/Docstrings pour le code, ou un fichier `README.md` complet pour un projet.

## 📦 Git & CI/CD workflow

- **`git commit`** : Génère un message de commit suivant la convention "Conventional Commits" (ex: `feat:`, `fix:`, `chore:`) en analysant le diff stagé (`git diff --staged`).
- **`git create-pr`** : Rédige une description de Pull Request professionnelle (Titre, Résumé, Changements clés, Impact, Instructions de test) basée sur la différence entre la branche actuelle et `main/develop`.
- **`git fix-pr-comments`** : Prend en entrée les commentaires d'une PR et le code concerné, puis génère les modifications de code pour résoudre les retours.
- **`git merge-conflict`** : Assistant de résolution de conflits. Analyse les balises de conflit (`<<<<<<<`, `=======`, `>>>>>>>`) et propose une version fusionnée cohérente.
- **`watch-ci`** : Analyse les logs bruts d'échec de CI/CD (GitHub Actions, GitLab CI) pour expliquer pourquoi le pipeline a échoué et comment le réparer (ex: erreur de linter cachée, timeout).

## 🚀 SaaS Builder (Product & Launch)

Commandes spécifiques pour lancer des produits (SaaS, Micro-SaaS).

- **`saas challenge-idea`** : "Roast my idea". Agit comme un VC ou un critique produit pour trouver les failles de marché, les problèmes de faisabilité et les concurrents d'une idée de SaaS.
- **`saas create-architecture`** : Propose une stack technique et une architecture système (Frontend, Backend, DB, Infra) adaptées aux besoins du projet (Scalabilité vs Rapidité).
- **`saas create-prd`** : Rédige un **Product Requirement Document** (PRD) complet : User Stories, Critères d'acceptation, Flux utilisateurs.
- **`saas create-tasks`** : Transforme un PRD ou une liste de fonctionnalités en un backlog de tâches techniques (Jira/Linear style).
- **`saas define-pricing`** : Analyse le marché pour proposer une stratégie de pricing (Freemium, Tiered, Usage-based) et des tableaux de prix psychologiques.
- **`saas find-domain-name`** : Brainstorming créatif de noms de domaine disponibles, courts et "catchy", basés sur la proposition de valeur.
- **`saas create-landing`** : Génère la structure et le contenu (Copywriting) d'une Landing Page à haute conversion (Hero, Features, Social Proof, CTA).
- **`saas implement-landing`** : Génère le code (React/Tailwind/HTML) pour la Landing Page définie précédemment.
- **`saas create-legals`** : Génère des modèles de base pour les documents légaux (Privacy Policy, Terms of Service) adaptés au type de service (⚠️ À vérifier par un juriste).

## 📣 Marketing & Copywriting

- **`marketing copywriting`** : Expert en écriture persuasive. Réécrit ou génère du texte pour : emails de vente, posts LinkedIn/Twitter, ou descriptions produits, en utilisant des frameworks comme AIDA ou PAS.

## 🔧 Utils & Helpers

- **`utils quick-search`** : Moteur de recherche sémantique. Recherche dans la documentation fournie ou le code pour trouver la réponse précise à une question technique (au lieu de lire toute la doc).
- **`utils shell-assist`** : _[Nouveau]_ Convertit une demande en langage naturel (ex: "Trouve tous les fichiers > 10mo et supprime les") en commande terminal (Bash/Zsh) optimisée.
- **`utils sql-helper`** : _[Nouveau]_ Génère des requêtes SQL complexes ou optimise une requête existante à partir d'une description du besoin et du schéma de la base.
- **`utils auto-fix`** : Tente de corriger automatiquement une erreur de linter ou de compilation fournie en entrée (JSON output, logs).
- **`utils fix-grammar`** : Correcteur avancé. Corrige l'orthographe, la grammaire et améliore le style/ton d'un texte (français ou anglais).
- **`utils translate`** : Traducteur technique. Traduit du code (fichiers i18n/json) ou de la documentation tout en préservant scrupuleusement le contexte technique et les variables.
- **`utils regex`** : Générateur/Explicateur de Regex. Crée une expression régulière robuste à partir d'une description, ou décortique une regex existante.
- **`utils tools`** : Conseiller technique. Recommande la meilleure bibliothèque, outil ou service SaaS pour résoudre un problème spécifique (ex: "Quelle lib pour gérer les dates en JS en 2025 ?").
