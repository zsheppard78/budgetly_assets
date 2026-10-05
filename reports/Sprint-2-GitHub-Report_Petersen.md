# Sprint 2 GitHub Report — Tyler Petersen

**Sprint:** SCRUM Sprint 2 (22 Sep – 6 Oct 2026)
**GitHub username:** tylerpetersen1

**Repository URLs:**
- Backend (Firebase rules + Cloud Functions): https://github.com/zsheppard78/budgetly_backend_nodejs
- Web app (customer-facing): https://github.com/zsheppard78/budgetly_web_customer

---

## Pull Requests Authored by Me (Merged During Sprint)

Query used: `is:pr is:merged author:tylerpetersen1 merged:2026-09-22..2026-10-06` (run in each repo)

| # | Repo | PR Title | Link | Author | Reviewers | Merge Date |
|---|---|---|---|---|---|---|
| 5 | budgetly_backend_nodejs | SCRUM-24: Implement CSV parser and add test fixtures | [PR #5](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/5) | tylerpetersen1 | None (self-merged) | Oct 2, 2026 |
| 6 | budgetly_backend_nodejs | SCRUM-26: write parsed transactions to Firestore. | [PR #6](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/6) | tylerpetersen1 | No formal review (merged by zsheppard78) | Oct 2, 2026 |
| 7 | budgetly_backend_nodejs | SCRUM-28: mark imports failed instead of hanging when processing runs out of time | [PR #7](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/7) | tylerpetersen1 | No formal review | Oct 4, 2026 |
| 8 | budgetly_backend_nodejs | SCRUM-25: parse text based PDF statements | [PR #8](https://github.com/zsheppard78/budgetly_backend_nodejs/pull/8) | tylerpetersen1 | No formal review | Oct 4, 2026 |
| 18 | budgetly_web_customer | SCRUM-29: live import history, failed/partial/no-data states | [PR #18](https://github.com/zsheppard78/budgetly_web_customer/pull/18) | tylerpetersen1 | No formal review; CI 2/2 passing | Oct 3, 2026 |
| 19 | budgetly_web_customer | Use crypto.randomUUID for temporary import row ids (SonarQube) | [PR #19](https://github.com/zsheppard78/budgetly_web_customer/pull/19) | tylerpetersen1 | No formal review; CI 2/2 passing | Oct 5, 2026 |

**Totals:** 6 PRs authored and merged (4 backend, 2 web).

**PRs I reviewed/merged for my teammate (11):** budgetly_web_customer #5, #9, #11, #12, #13, #14, #15, #16 and budgetly_backend_nodejs #1, #2, #3.

---

## Individual Contribution Summary

| Area | What I delivered | Jira |
|---|---|---|
| CSV parsing | `csvParser.js` that normalizes bank CSV exports into transactions, with test fixtures and unit tests | SCRUM-24 |
| Firestore writes | Import pipeline that writes parsed transactions to Firestore (`importPipeline.js`, `firestoreStore.js`) with tests | SCRUM-26 |
| PDF parsing | Parsing of text-based PDF bank statements | SCRUM-25 |
| Failure handling | Imports are marked failed instead of hanging when processing times out | SCRUM-28 |
| Import states UI | Live import history plus failed / partial / no-data states in the web app | SCRUM-29 |
| Code quality | Fixed a SonarQube finding (crypto.randomUUID for temporary row ids) | — |
| Code review | Reviewed and merged 11 of my teammate's PRs across both repos | — |
| Docs | Enhanced system architecture documentation (Sep 22) | — |

---

## Commit Activity

| Repo | My commits (non-merge) |
|---|---|
| budgetly_backend_nodejs | 2 |
| budgetly_web_customer | 3 |
| **Total** | **5** (2 through merged PRs; 3 reached `main` without a PR, which don't count) |

- **Date range:** Sep 22, 2026 – Oct 2, 2026

**Note on workflow discipline:** Two of my web commits on Oct 1 ("t" and "Deleted accidental copies") went directly to `main` instead of through a PR; the accidental "t" commit was reverted through PR #17. My Sep 22 architecture-doc commit reached `main` through a manual merge rather than a PR. These don't count as PR evidence and are listed for transparency.

---

## Summary

My main Sprint 2 work was the data side of statement import: parsing CSV and PDF statements, writing transactions to Firestore, handling failed/timed-out imports, and showing import status in the UI. I also acted as the reviewer/merger for most of my teammate's PRs, which fixed the Sprint 1 gap where PRs were self-merged.
