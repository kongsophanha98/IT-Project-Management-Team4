# Retrospective template · Realtime Quiz

Use one copy per sprint. Timebox: 1.5 h for a two-week sprint. The scrum master facilitates.

Sections: sprint · attendees · data (velocity, burndown observations) · what went well · what to improve · actions (action, owner, due, check in next retrospective).

---

# Retrospective · Sprint 1 (filled)

## Sprint
Sprint 1, weeks 4-5, 2026-10-20 to 2026-11-02. Retrospective on Monday 2026-11-02, 15:30-17:00.

## Attendees
Student A (product owner), Student B (scrum master, facilitator), Student C, Student D. PM invited as observer.

## Data
- Committed 30 points, velocity 25 points (83 %); one 5-point item returned to the product backlog.
- Burndown: flat at 30 points on D0-D2 (no item finished in the first 3 days), flat again on D4-D5 (23 points), maximum gap to the ideal line 8 points on D5-D6, final gap 5 points.
- Hours used about 80 h of 80 h capacity, about 3.2 h per point against the 2.5 h assumed at planning.

## What went well
- The team delivered 25 points in its first Scrum sprint and kept the daily scrum at 15 minutes.
- Burn rate was steady from D6 (15 points in 4 days) after the CI pipeline worked.
- The sponsor attended the review and accepted the register and login demo.

## What to improve
- Nothing was finished for 3 days: the skeleton, Docker and Flyway blocked everybody.
- Items stayed open until the end; the DoD check (coverage, review) happened too late for the last item.
- The estimate of 2.5 h per point was too optimistic.

## Actions
| Action | Owner | Due | Check in next retrospective |
|--------|-------|-----|-----------------------------|
| Have the project skeleton with CI and Docker working on day 1 of every sprint, and split every item so that it can be finished in at most 2 working days | Student A (PO) with Student C | Sprint 2 planning, 2026-11-03 | Burndown shows the first reduction by D2 (remaining <= 27 points at D2) |
| Check the Definition of Done at D5 and D8 in the daily scrum for every open item; no new item is started while 2 items are in review | Student B (SM) | From 2026-11-04 | No item enters D10 not meeting the DoD, returned points = 0 |
| Plan sprint 2 with 25 points and 3.2 h per point; keep a 10 % buffer | Student A (PO) | 2026-11-03 | Committed points <= 25 and velocity >= 90 % of commitment |
