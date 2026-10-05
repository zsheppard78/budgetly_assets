# Sprint 2 GitHub Report — Zachary Sheppard

**Sprint:** SCRUM Sprint 2 (22 Sep – 6 Oct 2026)
**GitHub username:** zsheppard78

**Repository URLs** (the project was split into per-component repos this sprint, following the `budgetly_*` naming convention):
- Web app (customer-facing): https://github.com/zsheppard78/budgetly_web_customer
- Backend (Firebase rules + Cloud Functions): https://github.com/zsheppard78/budgetly_backend_nodejs
- Supporting repos (README-only so far this sprint): [budgetly_assets](https://github.com/zsheppard78/budgetly_assets), [budgetly_contracts](https://github.com/zsheppard78/budgetly_contracts), [budgetly_web_dash](https://github.com/zsheppard78/budgetly_web_dash)

---

## Pull Requests Authored by Me (Merged During Sprint)

Query used: `is:pr is:merged author:zsheppard78 merged:2026-09-22..2026-10-06` (run in each repo)

### budgetly_web_customer

| # | PR Title | Link | Author | Reviewers | Merge Date |
|---|---|---|---|---|---|
| 5 | Web scaffold: React + Tailwind + dashboard shell | [PR #5](https://github.com/zsheppard78/budgetly_web_customer/pull/5) | zsheppard78 | tylerpetersen1 (Approved) | Sep 23, 2026 |
| 6 | Feature/web scaffold | [PR #6](https://github.com/zsheppard78/budgetly_web_customer/pull/6) | zsheppard78 | None (self-merged) | Sep 23, 2026 |
| 8 | Split repo: move backend to separate repo, flatten web app to root | [PR #8](https://github.com/zsheppard78/budgetly_web_customer/pull/8) | zsheppard78 | None (self-merged) | Sep 25, 2026 |
| 9 | added comments to existing components to improve | [PR #9](https://github.com/zsheppard78/budgetly_web_customer/pull/9) | zsheppard78 | No formal review (merged by tylerpetersen1) | Sep 29, 2026 |
| 11 | added new files for backend and hosting | [PR #11](https://github.com/zsheppard78/budgetly_web_customer/pull/11) | zsheppard78 | No formal review (merged by tylerpetersen1) | Sep 30, 2026 |
| 12 | Add GitHub Actions auto-deploy to Firebase Hosting | [PR #12](https://github.com/zsheppard78/budgetly_web_customer/pull/12) | zsheppard78 | No formal review (merged by tylerpetersen1); CI 2/2 passing | Sep 30, 2026 |
| 13 | Feature/connect firebase | [PR #13](https://github.com/zsheppard78/budgetly_web_customer/pull/13) | zsheppard78 | No formal review (merged by tylerpetersen1); CI 2/2 passing | Sep 30, 2026 |
| 14 | Pass firebase config secrets to hosting build | [PR #14](https://github.com/zsheppard78/budgetly_web_customer/pull/14) | zsheppard78 | No formal review (merged by tylerpetersen1); CI 2/2 passing | Sep 30, 2026 |
| 15 | SCRUM-22: Upload statements to Firebase Storage with real progress | [PR #15](https://github.com/zsheppard78/budgetly_web_customer/pull/15) | zsheppard78 | No formal review (merged by tylerpetersen1); CI 2/2 passing | Oct 1, 2026 |
| 16 | Real Firebase logout + protect dashboard routes with RequireAuth | [PR #16](https://github.com/zsheppard78/budgetly_web_customer/pull/16) | zsheppard78 | No formal review (merged by tylerpetersen1); CI 2/2 passing | Oct 1, 2026 |
| 17 | Revert "t" | [PR #17](https://github.com/zsheppard78/budgetly_web_customer/pull/17) | zsheppard78 | None (self-merged); CI 2/2 passing | Oct 1, 2026 |

### budgetly_backend_nodejs

| # | PR Title | Link | Author | Reviewers | Merge Date |
|---|---|---|---|---|---|
| 1 | SCRUM-15: init Firebase config and add Firestore security rules scope | [PR #1](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/1) | zsheppard78 | No formal review (merged by tylerpetersen1) | Sep 30, 2026 |
| 2 | Scrum 15 rules tests | [PR #2](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/2) | zsheppard78 | No formal review (merged by tylerpetersen1) | Sep 30, 2026 |
| 3 | SCRUM-23: Cloud Function to create Import record on statement upload | [PR #3](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/3) | zsheppard78 | No formal review (merged by tylerpetersen1) | Oct 1, 2026 |
| 4 | SCRUM-23: document onStatementUploaded function | [PR #4](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/4) | zsheppard78 | None (self-merged) | Oct 1, 2026 |

**PRs I reviewed/merged for my teammate:** budgetly_backend_nodejs [PR #6](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/6) (SCRUM-26: write parsed transactions to Firestore, by tylerpetersen1, merged Oct 2, 2026).

**Totals:** 15 PRs authored and merged (11 web, 4 backend). 11 of 15 were merged by my teammate rather than by me, an improvement over Sprint 1 where nearly every PR was self-merged. Only PR #5 received a formal GitHub approval; for Sprint 3 we will require an approving review before merge. From PR #12 onward every web PR also ran the GitHub Actions Firebase preview deploy (2/2 checks passing) before merge.

---

## Individual Contribution Summary

| Area | What I delivered | Jira |
|---|---|---|
| Web app scaffold | React + Tailwind + Vite app, router, dashboard shell, signup/login/consent screens | Account & Onboarding epic |
| Repo restructure | Split the monorepo into `budgetly_*` repos, moved docs to assets | — |
| Firebase Auth | Signup, login, consent wired to Firebase Authentication + Firestore user profile; real logout; `RequireAuth` route protection | SCRUM-14 / Account & Onboarding |
| Security rules | Firestore rules scoped to user UID + 6 passing rules unit tests | SCRUM-15 |
| Deployment | Firebase Hosting + GitHub Actions auto-deploy on merge/PR, secrets passed to build | — |
| Statement upload | Upload to Firebase Storage with real progress bar | SCRUM-22 |
| Import function | `onStatementUploaded` Cloud Function that creates an Import record | SCRUM-23 |
| Documentation | Code comments across web components/pages and backend files, READMEs | — |

---

## Commit Activity

| Repo | My commits (non-merge) |
|---|---|
| budgetly_web_customer | 20 |
| budgetly_backend_nodejs | 9 |
| budgetly_assets / contracts / web_dash | 4 (README setup) |
| **Total** | **33** (19 through merged PRs; 14 direct to `main`, including the 4 README commits in the supporting repos, which don't count) |

- **Date range:** Sep 22, 2026 – Oct 2, 2026 (first – most recent commit this sprint)
- Commits are spread across 8 distinct days of the sprint (Sep 22, 23, 25, 27, 29, 30, Oct 1–2) rather than batched at the deadline.
- Feature commits reference Jira keys (`SCRUM-15`, `SCRUM-22`, `SCRUM-23`) and branches are named after tickets (e.g. `feature/SCRUM-22-upload-to-storage`).

**Note on workflow discipline (honest accounting):** Not every change went through a PR. In `budgetly_web_customer`, 7 of my commits landed directly on `main` (README edits, the ledger→budgetly rename, "added ui files", "added backend", the project overview presentation, and a code-comments commit on Oct 2), and in `budgetly_backend_nodejs` 3 did (two README commits and a code-comments commit on Oct 2). I also created 2 local "Merge branch 'main'" commits when syncing. Per the course rules these direct pushes don't count toward PR evidence and are listed here only for transparency. Branch protection on `main` (require PR + 1 approval) is the fix for Sprint 3.

---

## Summary

Sprint 2 was the first sprint with real feature code. I built the web app scaffold, connected it to Firebase Auth/Firestore, locked down data with UID-scoped security rules and tests, set up automatic deploys to Firebase Hosting, and built the statement upload path (Storage upload with progress + the Cloud Function that records each import). Compared with Sprint 1, PR usage went from 4 mostly-test PRs to 15 feature PRs, with most merged by my teammate. The remaining gap is the handful of direct-to-main commits for docs/comments, which we'll close by enabling branch protection.
