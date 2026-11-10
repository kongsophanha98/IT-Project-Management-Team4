# Sprint 1 planning (simulated) · 2026-10-20

Tuesday 2026-10-20, 10:00-12:00 (2 h timebox). Attendees: Student A-D (A = product owner, B = scrum master), PM as observer. Scale: 1, 2, 3, 5, 8, 13. Rule: if highest and lowest estimates are more than one Fibonacci step apart, the two students explain and everybody re-estimates.

## Planning poker

| Item | A | B | C | D | Agreed | Note |
|------|--:|--:|--:|--:|-------:|------|
| B-01 Project skeleton, CI, Docker, Flyway | 3 | 3 | 5 | 2 | 3 | 2 and 5 are two steps apart. C (5): Docker, Flyway and the CI pipeline are new to us and may take a week to debug. D (2): the Spring Boot skeleton from the Software Engineering course already builds with Maven; only Docker and Flyway are new. Re-estimate: 3, 3, 3, 3 |
| B-02 Register with email, name, role | 3 | 2 | 3 | 3 | 3 | 2 and 3 are adjacent, no discussion needed; B agrees because validation and password hashing are included |
| B-03 Log in, JWT with 12 h expiry | 5 | 8 | 5 | 5 | 5 | 5 and 8 are adjacent. B (8) fears the token filter and expiry tests; the others point to the Spring Security example; team keeps 5 and adds a time-box on the spike |
| B-04 Role checks, instructor/student pages | 3 | 3 | 3 | 5 | 3 | D (5) wants separate page layouts; agreed to use one layout with role-based menus, so 3 |
| B-05 Create quiz (title, description, visibility) | 5 | 5 | 3 | 5 | 5 | C (3) ignores validation and visibility rules; after the explanation the team keeps 5 |
| B-06 Add, edit, reorder, delete questions | 8 | 13 | 8 | 8 | 8 | 8 and 13 are adjacent, but B explains the drag-and-drop reorder as the main cost; team agrees to keep 8 and puts drag-and-drop out of scope (buttons up/down instead) |
| B-07 Single- and multi-answer questions | 3 | 2 | 3 | 3 | 3 | B (2) assumes one shared answer table; A points out the multi-answer scoring rule, B agrees to 3 |

## Capacity check
Committed: 3 + 3 + 5 + 3 + 5 + 8 + 3 = **30 points** (~ 75 h at 2.5 h per point, of 80 h capacity = 4 x 10 h x 2 weeks). The buffer of 5 h (about 6 %) is thin; because the planning velocity of 30 is only a first guess for a first-time team, the sponsor and PM are told at the review that 25 points would be a normal outcome.

Sprint goal: *By 2 November 2026 a registered student or instructor can log in with the right role, and an instructor can create a quiz with single- and multi-answer questions, all built and tested automatically.*

## Burndown analysis
Chart: [burndown.mmd](burndown.mmd). Remaining points: D0 30, D1 30, D2 30, D3 26, D4 23, D5 23, D6 20, D7 15, D8 11, D9 8, D10 5. Ideal line burns 3 points per day. The gap between actual and ideal is 0, 3, 6, 5, 5, 8, 8, 6, 5, 5, 5 points (D0 to D10).

- **First two days behind:** day **D2**. At D2 the team has 30 points left against an ideal of 24; the gap of 6 points equals two days of ideal burn (2 x 3). The gap peaks at 8 points on D5 and D6 and never closes.
- **Velocity achieved:** 30 - 5 = **25 points** (only items that met the DoD count; 83 % of the commitment, about 3.2 h per point with 80 h used).
- **Returned to backlog:** one 5-point item. The data only says that the 5 open points are one single item; I assume it is **B-05 Create quiz** (not finished against the DoD, e.g. validation and coverage missing) and it goes to the top of the product backlog for sprint 2. If it was B-03, the reasoning below does not change.
- **Forecast sprints 2-4:** remaining Must + Should backlog = 120 - 25 = 95 points. At velocity 25 that needs 95 / 25 = 3.8 sprints, but only 3 sprints remain (about 75 points), so **20 points do not fit**. Even at the planned velocity of 30 only 90 points fit (5 short). Options for the G2 and sponsor discussion: keep all Must items and move at least 20 points of Should items (for example analytics and CSV/PDF export) to Could; use part of the hardening weeks only for defects, not for new features; do not raise the commitment above 25 points per sprint.
