# Sprint 3 GitHub Report — Zachary Sheppard

**Sprint:** SCRUM Sprint 3 (8 Oct – 20 Oct 2026)
**GitHub username:** zsheppard78

**Repository URLs:**
- Web app (customer-facing): https://github.com/zsheppard78/budgetly_web_customer
- Backend (Firebase rules + Cloud Functions): https://github.com/zsheppard78/budgetly_backend_nodejs
- Contracts (shared schemas and AI interface): https://github.com/zsheppard78/budgetly_contracts
- Supporting repo: [budgetly_assets](https://github.com/zsheppard78/budgetly_assets) (this report)

---

## Pull Requests Authored by Me (Merged During Sprint)

Query used: `is:pr is:merged author:zsheppard78 merged:2026-10-08..2026-10-20` (run in each repo).
Titles are the PR titles; where a title was the default or cut off, the commit subject is used. Reviewers: the teammate who reviewed and merged the PR (from the merge record); "None (self-merged)" where I merged my own.

### budgetly_web_customer

| # | PR Title | Link | Author | Reviewers | Merge Date |
|---|---|---|---|---|---|
| 20 | Dashboard: real current month with month switcher, signed-in user's name, plain tile labels (SCRUM-97, 98) | [PR #20](https://github.com/zsheppard78/budgetly_web_customer/pull/20) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 21 | Dashboard: clearer budget summary with labeled spent, left to spend and total budget (SCRUM-99) | [PR #21](https://github.com/zsheppard78/budgetly_web_customer/pull/21) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 22 | Dashboard: monthly budget is based on the month's money in (SCRUM-100) | [PR #22](https://github.com/zsheppard78/budgetly_web_customer/pull/22) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 23 | Budget page: Auto budget with preview, and custom categories (SCRUM-101, 102) | [PR #23](https://github.com/zsheppard78/budgetly_web_customer/pull/23) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 24 | Import page: delete a statement with its transactions and file | [PR #24](https://github.com/zsheppard78/budgetly_web_customer/pull/24) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 25 | Budget page: total budget is the month's money in (SCRUM-103) | [PR #25](https://github.com/zsheppard78/budgetly_web_customer/pull/25) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 26 | Auto budget: allocate all money in, with optional savings taken evenly from categories (SCRUM-104) | [PR #26](https://github.com/zsheppard78/budgetly_web_customer/pull/26) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 27 | Budget page shows one month at a time; Auto budget explains uncategorized spending (SCRUM-105) | [PR #27](https://github.com/zsheppard78/budgetly_web_customer/pull/27) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 28 | Credit card statements: Transfer category left out of money in/out, send account type on upload (SCRUM-92) | [PR #28](https://github.com/zsheppard78/budgetly_web_customer/pull/28) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 33 | SCRUM-77: inline category edit shows saving and errors, and can apply to the same merchant | [PR #33](https://github.com/zsheppard78/budgetly_web_customer/pull/33) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 19, 2026 |
| 34 | SCRUM-84: Settings saves your name and monthly income | [PR #34](https://github.com/zsheppard78/budgetly_web_customer/pull/34) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 19, 2026 |
| 35 | Dashboard: no fake "0% vs last month" without data; Transactions net leaves out transfers | [PR #35](https://github.com/zsheppard78/budgetly_web_customer/pull/35) | zsheppard78 | None (self-merged) | Oct 19, 2026 |

### budgetly_backend_nodejs

| # | PR Title | Link | Author | Reviewers | Merge Date |
|---|---|---|---|---|---|
| 9 | Add deleteImport callable: removes an import's transactions, file and record | [PR #9](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/9) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 10 | fixed credit card statement upload (SCRUM-92) | [PR #10](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/10) | zsheppard78 | None (self-merged) | Oct 8, 2026 |
| 11 | SCRUM-68: backend copy of the category list and category fields | [PR #11](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/11) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 9, 2026 |
| 12 | SCRUM-70, SCRUM-71, SCRUM-72: categorize transactions with Claude Haiku 5.5, fall back to Uncategorized | [PR #12](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/12) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 9, 2026 |
| 13 | Free merchant keyword rules: categorize common merchants on import with no AI cost | [PR #13](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/13) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 9, 2026 |
| 14 | fixed ai categorization (keep deploys free: move the paid Claude function out of index.js) | [PR #14](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/14) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 9, 2026 |
| 18 | SCRUM-88: Firestore rules and tests for profile settings | [PR #18](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/18) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 19, 2026 |

### budgetly_contracts

| # | PR Title | Link | Author | Reviewers | Merge Date |
|---|---|---|---|---|---|
| 1 | SCRUM-68, SCRUM-69: category list, category fields and AI categorization interface | [PR #1](https://github.com/zsheppard78/budgetly_contracts/pull/1) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 9, 2026 |
| 2 | removed need for api key (rule source also covers the free merchant keyword list) | [PR #2](https://github.com/zsheppard78/budgetly_contracts/pull/2) | zsheppard78 | None (self-merged) | Oct 9, 2026 |
| 3 | SCRUM-80: Firestore schema for budgets and user settings (monthly income) | [PR #3](https://github.com/zsheppard78/budgetly_contracts/pull/3) | zsheppard78 | tylerpetersen1 (reviewed and merged) | Oct 19, 2026 |

**PRs I reviewed/merged for my teammate:**
- budgetly_web_customer [PR #29](https://github.com/zsheppard78/budgetly_web_customer/pull/29) (SCRUM-87: empty states) and [PR #30](https://github.com/zsheppard78/budgetly_web_customer/pull/30) (SCRUM-81, 85: budgets from Firestore), by tylerpetersen1, merged Oct 16, 2026.
- budgetly_backend_nodejs [PR #15](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/15) (SCRUM-81: budget rules), [PR #16](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/16) (SCRUM-86: manual transaction rules) and [PR #17](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/17) (SCRUM-73–76: import categorization), by tylerpetersen1, merged Oct 16, 2026.

**Totals:** 22 PRs authored and merged (12 web, 7 backend, 3 contracts). 9 of 22 were merged by my teammate, and I merged 5 of his. That's more cross-merging than Sprint 2, but the Oct 8 batch (web #20–28, backend #9–10) was still self-merged. Branch protection (SCRUM-89, PR + 1 approval) is the planned fix. Every web PR triggers the GitHub Actions Firebase preview deploy, and since Tyler's PR #17 added a backend-tests workflow, backend PRs run the unit tests in CI as well.

---

## Individual Contribution Summary

| Area | What I delivered | Jira |
|---|---|---|
| Dashboard readability | Real current month with month arrows, greeting by name, plain-language tiles, clearer budget card, budget based on money in | SCRUM-93, 97–100 |
| Budget page | Budget = month's money in; one month at a time; "Auto budget" that splits all income across categories with optional savings taken evenly; custom categories | SCRUM-101–105 |
| Settings | Monthly income and name saved to Firestore; budgets use the income in months with no deposits | SCRUM-84 |
| Statement management | `deleteImport` Cloud Function (transactions in batches of ≤400, Storage file, import record) + Delete button with confirm dialog | — (follow-up to SCRUM-91 raw file storage) |
| Credit card statements | Account type sent on upload; card payments marked as transfers; positive card purchases flipped; transfers left out of all totals | SCRUM-92 |
| Auto categorization | Category list and AI request/response contract; Claude Haiku categorizer with validation and fallback (kept off to avoid API cost); free merchant keyword rules that are live | SCRUM-68–72 |
| Inline category edit | Save feedback, error message, "Also set N more from this merchant" | SCRUM-77 |
| Security and schema | Firestore rules + 7 emulator tests for profile settings; data model doc for budgets and settings | SCRUM-88, SCRUM-80 |
| Tests | 66 new tests: 59 backend unit tests (delete import 12, credit cards 14, categories 6, AI categorization 18, merchant rules 9) and 7 Firestore rules tests on the emulator | — |

---

## Commit Activity

| Repo | My commits (non-merge) |
|---|---|
| budgetly_web_customer | 13 |
| budgetly_backend_nodejs | 7 |
| budgetly_contracts | 3 |
| **Total** | **23** |

- **Date range:** Oct 8, 2026 (first commit) – Oct 19, 2026 (last commit), with commits on Oct 8, 9 and 19.
- **No direct pushes to `main` in the code repos this sprint.** Every code commit went through a feature branch and a PR, compared with 10 direct-to-main commits in Sprint 2. The only exceptions are two small edits to this report file on Oct 19 in `budgetly_assets`, made in the GitHub web editor (docs only, not counted).
- Commits and branches reference Jira keys (`SCRUM-68` to `SCRUM-88`) and are named after tickets (e.g. `feature/scrum-84-settings-income`).

---

## Summary

Sprint 3 turned the app from "imports transactions" into "helps you budget". On the web side I made the dashboard readable, based every budget on real income, added Auto budget with a savings option, and added a Settings income for card-only months. On the backend I added full statement deletion and correct handling of credit card statements, and I led auto categorization. That meant designing the contract, building an AI categorizer with Claude, and then, when we decided not to pay for an AI API, shipping free keyword rules that categorize about 97% of our test statements. Process improved too: every change went through a PR, cross-merging with my teammate increased, and branch protection (SCRUM-89) will require an approval on every PR from Sprint 4 onward.
