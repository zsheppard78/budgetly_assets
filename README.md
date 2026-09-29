# Budgetly — Assets

Non-code files for Budgetly: documentation, images, and sprint reports.

## Budgetly Repositories

| Repo | Contents |
|---|---|
| [budgetly_web_customer](https://github.com/zsheppard78/budgetly_web_customer) | Customer-facing React web app |
| [budgetly_web_dash](https://github.com/zsheppard78/budgetly_web_dash) | Dashboard web app |
| [budgetly_backend_nodejs](https://github.com/zsheppard78/budgetly_backend_nodejs) | Firebase Cloud Functions (Node.js), Firestore rules |
| [budgetly_contracts](https://github.com/zsheppard78/budgetly_contracts) | Interfaces: data schemas, API definitions, AI interface |
| **budgetly_assets** (this repo) | Docs, images, reports |

## Structure

```
docs/
  system-architecture.md          Overall system design
  ui-constraints.md               UI/UX rules for web and mobile
  projectOverviewPresentation.md  Project scope and overview
images/                           Logos, screenshots, wireframes (planned)
reports/                          Sprint Jira and Git reports, Sprint 2 onward (planned)
```

Data schemas and the AI interface are **not** here. They're interfaces the code must follow, so they live in **budgetly_contracts**.

Images and icons that an app loads at runtime belong in that app's repo. This repo is for source files, design exports, and reference material.

## Workflow

All changes go through a branch and pull request with at least one reviewer approval. No direct pushes to `main`.

## Team

- Zach Sheppard
- Tyler Petersen

CSCI 475 / CIS 675: Software Engineering, UW-Parkside, Fall 2026