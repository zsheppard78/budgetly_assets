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
| Issues completed | 36 (all) |
| Issues not completed | 0 |
| Issues added mid-sprint | 17 (SCRUM-89 – 93, SCRUM-97 – 108) |

---

## Issue Breakdown by Type

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 0 |
| Task | 0 | 0 | 36 |
| Bug | 0 | 0 | 0 |

| Epic | Issues | Points | Done |
|---|---|---|---|
| Auto Categorization | 10 (SCRUM-68 – 77) | 26 | 10 |
| Real User Data | 12 (SCRUM-80 – 88, 91 – 93) | 32 | 12 |
| Dashboard | 4 (SCRUM-97 – 100) | 7 | 4 |
| Smart Budgeting | 5 (SCRUM-101 – 105) | 12 | 5 |
| Statements | 3 (SCRUM-106 – 108) | 9 | 3 |
| No epic (process) | 2 (SCRUM-89, 90) | 2 | 2 |

---

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| ZS (Zachary Sheppard) | 27 | 27 | 63 |
| TP (Tyler Petersen) | 9 | 9 | 25 |

- **ZS:**
  - Category list and AI categorization contract (SCRUM-68, 69).
  - AI client with fallback, plus the free merchant keyword rules that categorize imports at no cost (SCRUM-70 – 72).
  - Inline category edit (SCRUM-77).
  - Firestore schema, Settings income and the security rules for settings (SCRUM-80, 84, 88).
  - Raw file storage and statement delete, plus credit/debit card statement handling (SCRUM-91, 92).
  - Dashboard readability (SCRUM-93, 97 – 100).
  - Auto budget, custom categories and income-based budgets (SCRUM-101 – 105).
  - Delete an imported statement, choosing Checking or Credit Card on import, and card payments tagged as Transfer (SCRUM-106 – 108).
  - Branch protection on the repos and the documented page (SCRUM-89, 90).
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
| Story points added mid-sprint | 39 |
| Total story points completed | 88 |
| Completion % (of committed) | 100% (49 / 49) |
| Completion % (of final scope) | 100% (88 / 88) |

All issues were estimated at 1–3 points, and all of the planned work (49 points) was completed.

---

## Workflow Discipline

- [x] Issues moved through workflow states (To Do → In Progress → Done). This applies to the planned issues (SCRUM-68 – 88). SCRUM-97 – 108 were logged after the work was finished, so they went straight to Done.
- [x] Issues closed only after acceptance criteria met: each issue was closed after its PR was merged (and, for user-facing work, tried on the deployed site).
- [x] Branches and commits reference Jira keys (e.g. `feature/scrum-84-settings-income`, `SCRUM-88: Firestore rules and tests for profile settings`).
- [ ] Sprint completed/closed in Jira (to be closed after the 10/20 demo)

---

## Blockers & Scope Changes

- **Major blockers:**
  - The AI API costs money, so we kept the Claude categorizer off and shipped free keyword rules instead (about 97% of test transactions categorized).
  - Firebase asked for a Secret Manager key on every deploy until we moved the AI function out of the deployed code.
  - Credit card payments counted as income and inflated budgets until card payments became Transfers (SCRUM-108).
- **Scope changes:** 17 issues (39 points) added mid-sprint from demo feedback and testing with real statements: dashboard readability (SCRUM-93, 97 – 100), Auto budget (SCRUM-101 – 105), statement delete and credit cards (SCRUM-91, 92, 106 – 108), and process tasks (SCRUM-89, 90). Nothing was removed.
- **Why work spilled over:** None. All 36 issues (88 / 88 points) were completed in the sprint.

---

## Jira Evidence Links

- **Sprint report link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1/reports/sprint-retrospective
- **Backlog link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog
- **Board link (filtered to sprint):** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1
