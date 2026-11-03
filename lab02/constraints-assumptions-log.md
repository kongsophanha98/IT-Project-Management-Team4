# Constraints and assumptions log · Realtime Quiz · v0.1 · week 3 (2026-10-13)

Authoritative inputs: lab01/charter.md, lab02/features.csv (504 h, 17 features). Every statement carries a number, a date or a named component.

## Constraints (imposed from outside the team, not negotiable by the team)

| Id   | Type       | Statement (measurable)                                                                                                                                | Source that imposed it                                                  | Validate by |
| ---- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------- |
| C-01 | Constraint | Go-live is a pilot with 50 students in week 14 of a 14-week semester that starts 2026-09-29 (pilot date moves to week 12 only if CR-03 is approved)   | Semester calendar and charter, section "Milestones"                     | fixed       |
| C-02 | Constraint | Effort capacity is 4 students x 10 h/week = 40 h/week = 560 h over 14 weeks (504 h planned work + 56 h contingency)                                   | Course regulation (10 h/week per student), charter, section "Resources" | fixed       |
| C-03 | Constraint | Cash budget is 200 USD: Linode VPS at gicitc.com 25 USD x 4 months = 100, domain 15, tools and reserve 85; no approver exists for overspend           | Head of IT (sponsor), charter, section "Budget"                         | fixed       |
| C-04 | Constraint | Technical: a result broadcast reaches every client in under 500 ms with 50 concurrent WebSocket connections; the system runs on the single Linode VPS | Non-functional requirements table, Lab-01 brief                         | fixed       |
| C-05 | Constraint | Policy: the user interface meets WCAG 2.1 level AA and the CI pipeline is green before any merge to main (Definition of Done)                         | Department accessibility policy and Definition of Done, Lab-01 brief    | fixed       |
| C-06 | Constraint | The project manager (supervising lecturer) is available 2 h/week; all approvals above 40 h of scope change go to the Head of IT                       | Charter, section "Roles"                                                | fixed       |

## Assumptions (believed true, not yet proven)

| Id   | Type       | Statement (measurable)                                                                                                                           | Owner                                | Validate by -> risk                     |
| ---- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------ | --------------------------------------- |
| A-01 | Assumption | At least 50 students register for the pilot by the end of week 11                                                                                | owner: student representative        | W10 -> R-01                             |
| A-02 | Assumption | Linode keeps the price at 25 USD/month for the 1 GB plan until week 14 (total 100 USD)                                                           | owner: infrastructure lead (student) | W3 -> R-02                              |
| A-03 | Assumption | The feature estimates in features.csv (504 h) are accurate within +/- 20 %; sprint velocity stays at or above 18 points (sprints 1-2: 18 and 21) | owner: supervising lecturer (PM)     | W7 (MVP checkpoint, 2026-11-16) -> R-03 |
| A-04 | Assumption | All four students deliver 10 h/week; no member loses more than 10 h in total before week 12                                                      | owner: team lead (student)           | W7 -> R-04                              |
| A-05 | Assumption | The two pilot instructors accept text-only quizzes (F13 Multimedia moved from Should to Could)                                                   | owner: supervising lecturer (PM)     | W6 -> R-05                              |
| A-06 | Assumption | The pilot room network sustains 50 simultaneous WebSocket connections with a latency under 500 ms                                                | owner: IT department contact         | W12 -> R-06                             |
| A-07 | Assumption | The sponsor decides on CR-03 (pilot in week 12) by 2026-10-30; without a decision Should work starts in W6                                       | owner: Head of IT (sponsor)          | W5 -> R-07                              |
| A-08 | Assumption | (added 2026-10-23, DR-01) Analytics (F10, 30 h) is demo-ready by the end of week 10 for the open day                                             | owner: backend lead (student)        | W9 -> R-10                              |

Review at every milestone. An overdue assumption becomes an open issue and is escalated to the sponsor.
