# 🧠 Gemini CLI Configuration: The "Second Brain" OS

![Gemini Config](https://img.shields.io/badge/Gemini-CLI%20Config-8A2BE2?style=for-the-badge&logo=google-gemini)
![Status](https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge)
![Methodology](https://img.shields.io/badge/Methodology-APEX-blue?style=for-the-badge)

> **"Ne codez pas plus dur, codez plus intelligemment."**
> Cette configuration transforme votre CLI Gemini standard en un partenaire d'ingénierie senior, un stratège produit et un expert marketing.

---

## 📑 Table des Matières

- [💎 Philosophie & Vision](#-philosophie--vision)
- [⚡ Installation Rapide](#-installation-rapide)
- [🔥 L'Arsenal (Fonctionnalités Clés & Exemples)](#-larsenal-fonctionnalités-clés--exemples)
    - [Core Engineering](#core-engineering-le-développeur-senior)
    - [Méthodologie APEX](#méthodologie-apex-architecture-first)
    - [SaaS Builder](#saas-builder-idea-to-market)
    - [Testing & Git](#testing--git-workflows)
    - [Utils & Marketing](#utils--marketing)
- [🛡️ Architecture & Sécurité](#-architecture--sécurité)
- [🛠️ Guide de Développement (Extension)](#-guide-de-développement-extension)
- [🤝 Contribuer](#-contribuer)

---

## 💎 Philosophie & Vision

La plupart des développeurs utilisent l'IA comme un outil de complétion ("Génère-moi une fonction").
Cette configuration est conçue pour l'utiliser comme un **Système Cognitif**.

Elle repose sur trois piliers :
1.  **Context-Awareness** : Chaque commande charge un contexte spécifique (Expert Sécu, Tech Lead, Copywriter).
2.  **Chain of Thought Forcée** : Des prompts structurés (XML tags, Steps) qui obligent le modèle à réfléchir avant de coder.
3.  **Standardisation** : Que vous soyez Junior ou Senior, la qualité du code produit reste constante et conforme aux standards (SOLID, DRY, OWASP).

---

## ⚡ Installation Rapide

### Prérequis
- **Gemini CLI** installé et authentifié.
- **Git** pour le versioning.

### Setup en 3 étapes

1.  **Cloner le dépôt** (dans votre dossier de configs global) :
    ```bash
    git clone https://github.com/votre-org/gemini-config.git ~/gemini-config
    ```

2.  **Configuration du Workspace** :
    Si vous utilisez VSCode ou un IDE, assurez-vous que `settings.json` est bien pris en compte.

3.  **Vérification** :
    ```bash
    gemini /oneshot "Crée une fonction Hello World en Python"
    ```

---

## 🔥 L'Arsenal (Fonctionnalités Clés & Exemples)

### Core Engineering (Le Développeur Senior)
*Pour le développement quotidien, rapide et qualitatif.*

<details>
<summary><code>/oneshot</code> - Génération de Code Rapide</summary>

**Scénario :** Créer un script simple.
*   **Input :** `gemini /oneshot "Script Python qui scrape les titres de HackerNews avec BeautifulSoup"`
*   **Output :**
    ```python
    import requests
    from bs4 import BeautifulSoup
    # ... Code complet avec gestion d'erreurs ...
    ```
</details>

<details>
<summary><code>/debug</code> - Root Cause Analysis</summary>

**Scénario :** Une erreur obscure dans vos logs.
*   **Input :** `gemini /debug "TypeError: Cannot read properties of undefined (reading 'map') dans UserList.js"`
*   **Output :**
    > **Root Cause :** La prop `users` arrive `undefined` avant le fetch initial.
    > **Fix :** Ajout d'un Optional Chaining (`users?.map`) ou valeur par défaut.
    > ```javascript
    > // Code corrigé ...
    > ```
</details>

<details>
<summary><code>/refactor</code> - Clean Code</summary>

**Scénario :** Nettoyer une fonction legacy illisible.
*   **Input :** `gemini /refactor (avec le fichier ouvert ou le code copié)`
*   **Output :** Code réécrit avec des noms de variables explicites, extraction de sous-fonctions, et typage ajouté.
</details>

<details>
<summary><code>/review</code> - Senior Code Review</summary>

**Scénario :** Vérifier la qualité avant de push.
*   **Input :** `gemini /review (sur un diff ou un fichier)`
*   **Output :**
    > 🔴 **Security :** Injection SQL possible ligne 42.
    > 🟡 **Performance :** N+1 query détectée dans la boucle.
    > 🟢 **Style :** Conforme, mais la fonction fait 50 lignes (trop long).
</details>

<details>
<summary><code>/security-audit</code> - OWASP Scan</summary>

**Scénario :** Audit de sécurité flash.
*   **Input :** `gemini /security-audit`
*   **Output :** Rapport listant les vulnérabilités (XSS, Secrets hardcodés) avec score de criticité (High/Medium/Low).
</details>

<details>
<summary><code>/explain</code> - Pédagogie</summary>

**Scénario :** Comprendre une Regex complexe.
*   **Input :** `gemini /explain "^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{8,}$"`
*   **Output :** "Cette regex valide un mot de passe : au moins 8 caractères, 1 lettre, 1 chiffre."
</details>

---

### Méthodologie APEX (Architecture First)
*Pour les fonctionnalités complexes nécessitant réflexion.*

<details>
<summary><code>/apex 1-analyse</code> - Phase d'Analyse</summary>

**Scénario :** Démarrer un gros module (ex: Système d'Auth).
*   **Input :** `gemini /apex 1-analyse "Je veux ajouter l'auth JWT avec Refresh Token"`
*   **Output :** Rapport technique listant les impacts, les dépendances nécessaires (jsonwebtoken, redis), et les risques de sécurité.
</details>

<details>
<summary><code>/apex 2-plan</code> - Phase de Planification</summary>

**Scénario :** Définir la roadmap technique.
*   **Input :** `gemini /apex 2-plan (après l'analyse)`
*   **Output :**
    1.  Setup DB Schema (User table).
    2.  Implement `generateToken` helper.
    3.  Create Middleware `verifyToken`.
    4.  Create Login/Register Routes.
</details>

<details>
<summary><code>/apex 3-execute</code> - Phase d'Exécution</summary>

**Scénario :** Coder le plan validé.
*   **Input :** `gemini /apex 3-execute "Implémente l'étape 2 du plan"`
*   **Output :** Code complet du helper `generateToken` et configuration des variables d'environnement.
</details>

<details>
<summary><code>/apex 4-examine</code> - Phase de Vérification</summary>

**Scénario :** Détecter les bugs logiques.
*   **Input :** `gemini /apex 4-examine`
*   **Output :** "Attention, le token n'est pas invalidé à la déconnexion. Suggère d'ajouter une blacklist Redis."
</details>

---

### SaaS Builder (Idea to Market)
*De l'idée au lancement produit.*

<details>
<summary><code>/saas challenge-idea</code> - Crash Test</summary>

**Scénario :** Tester une idée de startup.
*   **Input :** `gemini /saas challenge-idea "Tinder pour adopter des chats"`
*   **Output :**
    > **Marché :** Niche, monétisation difficile (les refuges ont peu de budget).
    > **Concurrents :** Petfinder, AdopteUnChat.
    > **Pivot :** Modèle Freemium pour les futurs propriétaires (kits de démarrage).
</details>

<details>
<summary><code>/saas create-landing</code> - Copywriting Page de Vente</summary>

**Scénario :** Rédiger le contenu du site.
*   **Input :** `gemini /saas create-landing "SaaS de comptabilité pour freelances"`
*   **Output :** Structure complète (H1: "Fini le cauchemar des factures", CTA: "Essai gratuit sans CB", Preuves sociales...).
</details>

<details>
<summary><code>/saas implement-landing</code> - Code Frontend</summary>

**Scénario :** Coder la page précédente.
*   **Input :** `gemini /saas implement-landing`
*   **Output :** Fichier React/Tailwind complet avec composants responsive.
</details>

---

### Testing & Git Workflows
*Qualité et CI/CD.*

<details>
<summary><code>/test-gen</code> - Génération de Tests</summary>

**Scénario :** Sécuriser une fonction critique.
*   **Input :** `gemini /test-gen (sur une fonction de calcul de TVA)`
*   **Output :** Fichier `tva.test.js` (Jest) couvrant les cas nominaux, les taux nuls, et les inputs invalides.
</details>

<details>
<summary><code>/git commit</code> - Message Conventionnel</summary>

**Scénario :** Commit propre.
*   **Input :** `gemini /git commit (avec des fichiers stagés)`
*   **Output :** `feat(auth): implement jwt refresh token rotation`
</details>

<details>
<summary><code>/git create-pr</code> - Description de PR</summary>

**Scénario :** Ouvrir une Pull Request.
*   **Input :** `gemini /git create-pr`
*   **Output :** Titre, Résumé des changements, Instructions de test, Checklist de validation.
</details>

---

### Utils & Marketing
*Les outils du quotidien.*

<details>
<summary><code>/marketing copywriting</code> - Posts Engageants</summary>

**Scénario :** Annoncer une feature sur LinkedIn.
*   **Input :** `gemini /marketing copywriting "Lancement de la v2 de notre API"`
*   **Output :** Post structuré (Hook -> Problème -> Solution -> CTA) avec emojis et formatage aéré.
</details>

<details>
<summary><code>/utils shell-assist</code> - Traducteur Bash</summary>

**Scénario :** Oubli d'une commande complexe.
*   **Input :** `gemini /utils shell-assist "Trouve tous les fichiers > 100Mo et zip-les"`
*   **Output :** `find . -type f -size +100M -exec zip archive.zip {} +`
</details>

<details>
<summary><code>/utils regex</code> - Générateur Regex</summary>

**Scénario :** Valider un email.
*   **Input :** `gemini /utils regex "Valide un email standard"`
*   **Output :** `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$` avec explication.
</details>

---

## 🛡️ Architecture & Sécurité

### Structure des Fichiers
Le dossier `commands/` est le cerveau du système. Chaque fichier `.toml` définit un agent spécialisé.

```text
commands/
├── core/           # oneshot, debug, refactor...
├── marketing/      # copywriting
├── saas/           # challenge-idea, landing...
└── utils/          # regex, sql, shell...
```

### Intégration MCP
Configuré pour `context7` via `settings.json` pour un accès contextuel étendu.

---

## 🛠️ Guide de Développement (Extension)

### Créer une commande personnalisée
Exemple : `commands/testing/cypress-gen.toml`

```toml
description = "Génère des tests E2E Cypress."
prompt = """
Tu es un Expert QA. Crée des tests Cypress robustes.
<input>Composant ou User Story</input>
"""
```

---

## 🤝 Contribuer

*   **Bug Report** : Ouvrez une issue.
*   **PRs** : Améliorez les prompts existants !

---

<p align="center">
  <em>Propulsé par Gemini CLI. Conçu pour les bâtisseurs.</em>
</p>
