# TDR-01 · Life cycle and methodology for the Realtime Quiz project
Status: proposed · 2026-10-12 · to be decided by the sponsor (Head of IT) and the PM (supervising lecturer) at gate G1 on 2026-10-19

Sources: [project profile](project-profile.md), [approach comparison](approach-comparison.md), [scoring sheet](approach-scoring.csv), [life cycle](life-cycle.svg)

## Context
The project is built by four students who work about 10 h/week each, 560 h in total, over 14 weeks starting 2026-09-29. The sponsor wants an approved plan by the end of week 3 and a pilot with 50 students in week 14, so both dates are fixed. The Must list of 8 features is fixed in the charter, but screens and real-time behaviour are not specified. Technical uncertainty is high: the campus proxy may block WebSocket and the Spring Boot 4 examples are outdated. The team has never run a Scrum project and learned Java and Spring in a parallel course. The project profile scores 3.20, which is in the hybrid band (2.5 to 3.5).

## Options considered
1. Waterfall (score 2.75): freeze all requirements at week 3 and build in one pass; strong governance but the sponsor sees a working quiz only in week 12.
2. Pure Scrum (score 3.70): sprints and a reordered backlog from week 1; strong feedback but no gate to protect the plan approval and the pilot date.
3. Hybrid (score 3.85): predictive plan and four gates around four two-week sprints; keeps the sponsor's control and gives a playable quiz in week 7.

## Decision
Choose option 3, the hybrid life cycle (predictive plan and gates G1-G4 around Scrum sprints). The two strongest reasons are:
1. It has the highest weighted score (3.85 against 3.70 for Scrum and 2.75 for waterfall) and stays first when team experience is weighted more heavily (Test 2: 3.75).
2. It meets both fixed sponsor demands, an approved plan at G1 in week 3 and the pilot at G4 in week 14, while still showing working software to the sponsor at every sprint review from week 5.

## Consequences
+ The sponsor sees an increment every two weeks and can play the first live quiz at the sprint 2 review in week 7.
+ The week-3 baseline (scope statement and WBS to level 2) gives a fixed reference for later scope and change control.
+ Four gates give the sponsor clear stop, re-plan or continue decisions in weeks 3, 7, 11 and 14.
+ Technical risks such as WebSocket behind the campus proxy are found in sprints 1 and 2, not at integration in week 12.
- Gates and reports consume team hours -> mitigation: one-page weekly highlight report and gate checklists of five items that reuse CI reports as evidence.
- The team is new to Scrum and may apply the events badly -> mitigation: a scrum master from week 4, a retrospective after every sprint and a written definition of ready and done.
- Scope creep from Could features can break the baseline -> mitigation: the Must list is baselined at G1 and any new item enters only through a change request with a scope tolerance.
- There is no float before the week-14 pilot -> mitigation: hardening is reserved in weeks 12-13, G3 checks hours used against 90 % of 560 h, and there is no overtime in the pilot week.

## Tailoring
| Keep from predictive | Keep from agile | Drop |
|----------------------|-----------------|------|
| Charter, scope statement and WBS to level 2 (needed for the scope baseline and the G1 approval) | Two-week sprints with sprint review and retrospective (the sponsor sees an increment every 2 weeks) | Detailed up-front design of every screen (screens are unspecified and would change after the first reviews) |
| Four stage gates G1-G4 with measurable checklists (the sponsor demands a plan in week 3 and a pilot in week 14) | Product backlog with story points, definition of ready and definition of done (items are estimated and checkable) | Separate test phase after the build (tests run in every sprint through CI; only hardening in weeks 12-13 remains) |
| Risk register and weekly highlight report (known risks such as the campus proxy need owners and a weekly status) | Daily scrum of 15 minutes (a team of four with 10 h/week each keeps blockers visible) | Formal change control board (the PM and sponsor decide at gates and by exception report) |
| Tolerances per stage and exception reporting (the sponsor is not present in the daily work) | Definition of done with CI checks for tests, coverage and build (gives automatic evidence for the gates) | Open-ended backlog with no end date (the pilot date is fixed, so scope is cut, not time) |

## Phase gates
| Gate | Week / date | Evidence required | Decision maker | Outcomes |
|------|-------------|-------------------|----------------|----------|
| G1 plan approved | W3 · Mon 2026-10-19 | Scope statement and WBS to level 2 committed in the repository; milestone schedule and 560 h budget approved; risk register with at least 8 risks, each with an owner | Sponsor | continue / continue with changes / stop / repeat |
| G2 MVP checkpoint | W7 · Mon 2026-11-16 | One quiz created, played live by 10 simulated students and scored, on the VPS (demo at the sprint 2 review); CI build green with line coverage of new service code >= 80 % in the JaCoCo report; hours used <= 55 % of 560 h | Sponsor with the PM | continue / continue with changes / stop / repeat |
| G3 release candidate | W11 · Mon 2026-12-14 | All Must and at least 80 % of Should items meet the definition of done (backlog export); load test with 100 simulated students and p95 broadcast < 500 ms (report); hours used <= 90 % of 560 h | Sponsor with the PM | continue / continue with changes / stop / repeat |
| G4 acceptance and closure | W14 · Mon 2027-01-04 | Pilot with 50 students completed (attendance sheet); no open critical defect (issue list); acceptance form signed and repository, VPS access and runbook handed over | Sponsor | continue / continue with changes / stop / repeat |
