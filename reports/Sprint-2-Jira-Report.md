# Sprint 2 Jira Report

**Jira Project:** Software Engineering (Financial Planner)
**Jira Link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1
**Sprint:** SCRUM Sprint 2 (22 Sep – 6 Oct 2026)
**Sprint Goal:** Users can create an account, give consent, and import a bank statement whose transactions are saved to Firestore.

---

## Sprint Commitment vs Delivery

| Metric | Count |
|---|---|
| Issues committed at sprint start | 16 (SCRUM-14 – SCRUM-29) |
| Issues completed | 23 |
| Issues not completed | 0 |
| Issues added mid-sprint | 7 (SCRUM-61 – SCRUM-67) |

---

## Issue Breakdown by Type

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 0 |
| Task | 0 | 0 | 23 |
| Bug | 0 | 0 | 0 |

| Epic | Issues | Points | Done |
|---|---|---|---|
| Account & Onboarding | 6 (SCRUM-14 – 19) | 14 | 6 |
| Statement Import | 10 (SCRUM-20 – 29) | 25 | 10 |
| No epic (infrastructure: repos, hosting, Firebase wiring) | 7 (SCRUM-61 – 67) | 10 | 7 |

---

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| ZS (Zachary Sheppard) | 16 | 16 | 30 |
| TP (Tyler Petersen) | 7 | 7 | 19 |

- **ZS:** Firebase Auth setup, security rules, signup/login/consent screens, dashboard shell, file-size validation, upload progress, upload Cloud Function (SCRUM-14 – 19, 21 – 23), plus repo split, Firebase Hosting auto-deploy, and connecting the UI to Auth/Firestore (SCRUM-61 – 67).
- **TP:** File upload UI, CSV parsing, PDF parsing, writing transactions to Firestore, partial-failure handling, status updates, and empty/error states (SCRUM-20, 24 – 29).

---

## Estimation & Accuracy

| Metric | Value |
|---|---|
| Story points committed at sprint start | 39 |
| Story points added mid-sprint | 10 |
| Total story points completed | 49 |
| Completion % (of committed) | 100% |
| Completion % (of final scope) | 100% (49 / 49) |

Ticket sizes stayed small: every issue was estimated at 1–3 points, and most 3-point items were broken into subtasks on the board.

---

## Workflow Discipline

- [x] Issues moved through workflow states (To Do → In Progress → Done)
- [x] Issues closed only after acceptance criteria met
- [x] Branches and commits reference Jira keys (e.g. `feature/SCRUM-22-upload-to-storage`, `SCRUM-15: add firestore security rules unit tests`)
- [ ] Sprint completed/closed in Jira (to be closed after the 10/06 demo)

---

## Blockers & Scope Changes

- **Major blockers:** Deploying the web app needed the Firebase config secrets passed into the GitHub Actions hosting build (fixed in web PR #14). Rules testing required setting up the Firestore emulator.
- **Scope changes:** 7 infrastructure tasks (10 points) were added mid-sprint after we decided to split the monorepo into the professor's `budgetly_*` repo structure and to auto-deploy to Firebase Hosting (SCRUM-61 – 66), plus a task to connect the existing UI to Firebase Auth/Firestore (SCRUM-67). Nothing was removed; PDF parsing (SCRUM-25) was considered for a cut but kept.
- **Why work spilled over (if any):** No spillover. All committed and added issues were completed within the sprint.

---

## Jira Evidence Links

- **Sprint report link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1/reports/sprint-retrospective
- **Backlog link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1/backlog
- **Board link:** https://team3csci675.atlassian.net/jira/software/projects/SCRUM/boards/1
