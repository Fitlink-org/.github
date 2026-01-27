# Contributing Guidelines

This document outlines the coding standards, workflows, and security protocols for our team. Please review these guidelines before contributing to the codebase.

## 1. Git Workflow & Branching Strategy

We follow a **Gitflow** (or adapted Trunk-based) workflow.

* **`main` (Production):** Always stable and deployable. **Direct commits are strictly prohibited.**
* **`develop` (Staging):** The default branch for development. All PRs should target this branch.
* **Branch Naming Convention:**
    * New Features: `feat/short-description` (e.g., `feat/user-login`)
    * Bug Fixes: `fix/short-description` (e.g., `fix/api-timeout`)
    * Hotfixes: `hotfix/short-description` (e.g., `hotfix/payment-error`)

## 2. Commits & Pull Requests (PR)

### Commit Messages
We adhere to the **Conventional Commits** specification:
* `feat: ...` -> New feature
* `fix: ...` -> Bug fix
* `docs: ...` -> Documentation changes
* `chore: ...` -> Maintenance (e.g., dependency updates)

**Example:** `feat: integrate google auth provider`

### Pull Request Process
1.  Provide a concise description of the changes.
2.  Requires approval from at least **1 team member**.
3.  CI/CD checks must pass.
4.  Merge conflicts must be resolved locally before merging.

## 3. Documentation

* **README.md:** Must be updated if there are changes to the setup or installation process.
* **CHANGELOG.md:** Major changes must be logged for every release.
* **Comments:** Complex logic should be accompanied by clear code comments.

## 4. AI Usage Policy

* **Privacy & Security:** Do not paste Customer PII, API Keys, or proprietary business logic into public AI models (ChatGPT, Gemini, etc.).
* **Code Review:** AI-generated code must be reviewed line-by-line. Blindly copying and pasting AI code is not accepted; you must understand what you commit.

## 5. Security & Tooling

* **Accounts:** All third-party tools (Figma, GitHub, Jira, etc.) must be accessed using **company email addresses**.
* **Secrets Management:** Never push `.env` files to the repository. Use Environment Variables for API keys and secrets.
* **Testing:** Unit tests are required for critical functionality.

## 6. Environments

* **Local:** Your local development setup.
* **Staging:** Testing environment deployed from the `develop` branch.
* **Production:** Live environment used by customers.

---
*Last updated: [Date]*
