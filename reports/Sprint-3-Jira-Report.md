# Sprint 3 Jira Report

**Jira Project:** Software Engineering (Financial Planner)
**Jira Link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1
**Sprint:** SCRUM Sprint 3 (8 Oct – 20 Oct 2026)
**Sprint Goal:** Imported transactions are categorized automatically, and the app runs on each user's real data (budgets, settings, manual transactions) instead of sample data.

---

## Sprint Commitment vs Delivery

| Metric | Count |
|---|---|
| Issues committed at sprint start | 19 (SCRUM-68 – 77, SCRUM-80 – 88) |
| Issues completed | 31 |
| Issues not completed | 2 (SCRUM-89, SCRUM-90) |
| Issues added mid-sprint | 14 (SCRUM-89 – 93, SCRUM-97 – 105) |

---

## Issue Breakdown by Type

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 0 |
| Task | 2 | 0 | 31 |
| Bug | 0 | 0 | 0 |

| Epic | Issues | Points | Done |
|---|---|---|---|
| Auto Categorization | 10 (SCRUM-68 – 77) | 26 | 10 |
| Real User Data | 12 (SCRUM-80 – 88, 91 – 93) | 32 | 12 |
| Dashboard | 4 (SCRUM-97 – 100) | 7 | 4 |
| Smart Budgeting | 5 (SCRUM-101 – 105) | 12 | 5 |
| No epic (process) | 2 (SCRUM-89, 90) | 2 | 0 |

---

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| ZS (Zachary Sheppard) | 24 | 22 | 52 |
| TP (Tyler Petersen) | 9 | 9 | 25 |

- **ZS:**
  - Category list and AI categorization contract (SCRUM-68, 69).
  - AI client with fallback, plus the free merchant keyword rules that categorize imports at no cost (SCRUM-70 – 72).
  - Inline category edit (SCRUM-77).
  - Firestore schema, Settings income and the security rules for settings (SCRUM-80, 84, 88).
  - Raw file storage and statement delete, plus credit/debit card statement handling (SCRUM-91, 92).
  - Dashboard readability (SCRUM-93, 97 – 100).
  - Auto budget, custom categories and income-based budgets (SCRUM-101 – 105).
- **TP:**
  - Categorization inside the import pipeline, with chunking, the merchant cache and tests with CI (SCRUM-73 – 76).
  - Live budgets from Firestore and the Transactions table (SCRUM-81, 82, 85).
  - Manual transactions (SCRUM-86) and empty states (SCRUM-87).
- SCRUM-83 (save budget limits to Firestore) is assigned to ZS but was delivered inside TP's SCRUM-81 work (web PR #30, backend PR #15). It's counted under ZS above because that's the Jira assignee.

---

## Estimation & Accuracy

| Metric | Value |
|---|---|
| Story points committed at sprint start | 49 |
| Story points added mid-sprint | 30 |
| Total story points completed | 77 |
| Completion % (of committed) | 100% (49 / 49) |
| Completion % (of final scope) | 97% (77 / 79) |

All issues were estimated at 1–3 points, and all of the planned work (49 points) was completed.

---

## Workflow Discipline

- [x] Issues moved through workflow states (To Do → In Progress → Done). This applies to the planned issues (SCRUM-68 – 88). SCRUM-97 – 105 were logged after the work was finished, so they went straight to Done.
- [x] Issues closed only after acceptance criteria met: each issue was closed after its PR was merged (and, for user-facing work, tried on the deployed site).
- [x] Branches and commits reference Jira keys (e.g. `feature/scrum-84-settings-income`, `SCRUM-88: Firestore rules and tests for profile settings`).
- [ ] Sprint completed/closed in Jira (to be closed after the 10/20 demo)

---

## Blockers & Scope Changes

- **Major blockers:**
  - **AI cost:** AI categorization needed a paid Claude API key. We built and tested the AI path (SCRUM-70 – 72), then switched it off and shipped free merchant keyword rules instead. They categorize about 97% of our test statements at no cost.
  - **Secret check on deploy:** keeping the AI function in the code made Firebase ask for a Secret Manager key on every deploy, so we moved it out of the deployed functions.
  - **Credit card statements:** card payments ("AUTOMATIC PAYMENT - THANK YOU") were being counted as income, which inflated every budget. This was fixed with the Transfer category and account types (SCRUM-92).
- **Scope changes:** 14 issues (30 points) were added mid-sprint after testing with real statements:
  - dashboard readability (SCRUM-93, 97 – 100)
  - Auto budget and custom categories (SCRUM-101 – 105)
  - credit/debit card statements (SCRUM-92)
  - raw file storage (SCRUM-91)
  - process tasks (SCRUM-89, 90)

  Nothing was removed.
- **Why work spilled over:**
  - **SCRUM-89 (branch protection on all repos):** a GitHub settings change that wasn't done before sprint end. It moves to Sprint 4.
  - **SCRUM-90 (commit documented page):** not started. It moves to Sprint 4.

---

## Jira Evidence Links

- **Sprint report link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1/reports/sprint-retrospective
- **Backlog link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog
- **Board link (filtered to sprint):** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1
