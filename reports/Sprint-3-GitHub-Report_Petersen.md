# Sprint 3 GitHub Report — Tyler Petersen

**Sprint:** SCRUM Sprint 3 (8 Oct – 20 Oct 2026)
**GitHub username:** tylerpetersen1

**Repository URLs:**
- Backend (Firebase rules + Cloud Functions): https://github.com/zsheppard78/budgetly_backend_nodejs
- Web app (customer-facing): https://github.com/zsheppard78/budgetly_web_customer

---

## Pull Requests Authored by Me (Merged During Sprint)

Query used: `is:pr is:merged author:tylerpetersen1 merged:2026-10-08..2026-10-20` (run in each repo)

| # | Repo | PR Title | Link | Author | Merged by | Merge Date |
|---|---|---|---|---|---|---|
| 15 | budgetly_backend_nodejs | SCRUM-81: Firestore rules and tests for per-user budgets | [PR #15](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/15) | tylerpetersen1 | zsheppard78 | Oct 16, 2026 |
| 16 | budgetly_backend_nodejs | SCRUM-86: Firestore rules and tests for manual transactions | [PR #16](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/16) | tylerpetersen1 | zsheppard78 | Oct 16, 2026 |
| 17 | budgetly_backend_nodejs | SCRUM-73 to 76: categorize imports (rules, merchant cache, AI chunks) with tests and CI | [PR #17](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/17) | tylerpetersen1 | zsheppard78 | Oct 16, 2026 |
| 29 | budgetly_web_customer | SCRUM-87: empty states when a user has no budgets yet (dashboard and budget page) | [PR #29](https://github.com/zsheppard78/budgetly_web_customer/pull/29) | tylerpetersen1 | zsheppard78 | Oct 16, 2026 |
| 30 | budgetly_web_customer | SCRUM-81, SCRUM-85: budgets come from Firestore instead of sample data | [PR #30](https://github.com/zsheppard78/budgetly_web_customer/pull/30) | tylerpetersen1 | zsheppard78 | Oct 16, 2026 |
| 31 | budgetly_web_customer | SCRUM-86: add, edit and delete manual transactions | [PR #31](https://github.com/zsheppard78/budgetly_web_customer/pull/31) | tylerpetersen1 | tylerpetersen1 (self-merged) | Oct 16, 2026 |
| 32 | budgetly_web_customer | SCRUM-86: edit a manual transaction in place on its row | [PR #32](https://github.com/zsheppard78/budgetly_web_customer/pull/32) | tylerpetersen1 | tylerpetersen1 (self-merged) | Oct 16, 2026 |

"Merged by" comes from the merge commit. Formal approvals are recorded on GitHub, not in git.

**Totals:** 7 PRs authored and merged (3 backend, 4 web). 5 of 7 were merged by my teammate.

**PRs I reviewed/merged for my teammate (9):**
- budgetly_backend_nodejs #11 (SCRUM-68), #12 (SCRUM-70–72), #13 (free merchant keyword rules), #14 (keep deploys free) and #18 (SCRUM-88)
- budgetly_web_customer #33 (SCRUM-77) and #34 (SCRUM-84)
- budgetly_contracts #1 (SCRUM-68, 69) and #3 (SCRUM-80)

---

## Individual Contribution Summary

| Area | What I delivered | Jira |
|---|---|---|
| Real budgets | Budgets load live from `users/{uid}/budgets` (onSnapshot) and save with setDoc/deleteDoc, replacing the sample data; dashboard summary uses real numbers | SCRUM-81, SCRUM-85 |
| Budget security rules | Firestore rules for per-user budgets (owner only, exact fields, non-negative limit) + 6 emulator tests | SCRUM-81 |
| Empty states | Dashboard and Budget page explain what to do when a new user has no budgets yet | SCRUM-87 |
| Manual transactions | Add, edit and delete a transaction by hand (`ManualTransactionForm.jsx`), including editing in place on its row | SCRUM-86 |
| Manual transaction rules | Firestore rules that allow only the exact shape of a manual transaction, and keep imported ones read-only except the category + 7 emulator tests | SCRUM-86 |
| Import categorization | Categorization runs inside the import before the Firestore write: free rules first, then a per-user merchant cache of categories the user picked (saved by the new `onTransactionCategoryChanged` function), then optional AI in chunks of 50 with a time budget so the import always finishes inside the function timeout | SCRUM-73, 74, 75 |
| Tests and CI | 35 unit tests for import categorization with a mocked AI client; GitHub Actions workflow that runs the backend unit tests on every PR and push to main | SCRUM-76 |
| Code review | Reviewed and merged 9 of my teammate's PRs across all three repos | — |

---

## Commit Activity

| Repo | My commits (non-merge) |
|---|---|
| budgetly_backend_nodejs | 3 |
| budgetly_web_customer | 4 |
| **Total** | **7** (all through merged PRs) |

- **Date:** Oct 16, 2026
- **No direct pushes to `main` this sprint**, compared with 3 commits that reached `main` without a PR in Sprint 2.
- Every commit references its Jira key (`SCRUM-73` to `SCRUM-87`), and branches are named after tickets (e.g. `feature/scrum-81-85-real-budgets`).
- About 1,500 lines added in total. The biggest change is PR #17: 845 lines across 9 files, including `merchantCache.js`, `importCategorization.js` and the CI workflow.

---

## Summary

My Sprint 3 work made the app run on real user data. Budgets now live in Firestore instead of sample data, new users see helpful empty states, and users can add, edit and delete transactions by hand. Each of these has matching security rules and emulator tests. On the backend I wired categorization into the import pipeline with a merchant cache, so once a user picks a category for a merchant, future imports reuse it with no AI call, and added CI so the backend tests run on every pull request. I also reviewed and merged 9 of my teammate's PRs, and every one of my commits went through a PR.
