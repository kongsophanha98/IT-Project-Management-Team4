# Governance · Realtime Quiz hybrid life cycle

Sources: [charter](../lab01/project-charter.md), [MoSCoW list](../lab02/moscow-list.md), [life cycle](life-cycle.mmd), [decision record](tailoring-decision-record.md), [Scrum setup](scrum-setup.md)

Budget baseline: 4 students x 10 h x 14 weeks = 560 h, split into stage budgets of 120 h (S1), 160 h (S2), 160 h (S3), 120 h (S4). Cash budget: Linode VPS about 25 USD/month, one domain, total cash plan <= 150 USD.

## Stage gates

### G1 · Plan approved · end of week 3 (2026-10-19)
- [ ] Charter and stakeholder list approved by the sponsor in writing (evidence: signed charter, git tag `charter-v1.0`)
- [ ] Scope statement and WBS to level 2 cover 100 % of the Must FR ids (evidence: traceability table FR id -> WBS element, 0 uncovered Must ids)
- [ ] Milestone schedule shows G1-G4, four 14-day sprints and the pilot in week 14 (evidence: `life-cycle.mmd`, 4 `:milestone` lines)
- [ ] Budget in hours allocated to 4 stages = 560 h with a reserve of at least 56 h (10 %), cash plan <= 150 USD (evidence: budget table in the plan)
- [ ] Risk register has at least 10 risks, each with owner and response; the WebSocket-behind-campus-proxy risk has a test scheduled in sprint 1 (evidence: risk register, sprint 1 backlog)

Inputs: charter, scope statement, WBS, milestone schedule, budget in hours, risk register, sprint 1 backlog
Decision maker: sponsor (advised by the PM) · Outcomes: continue / continue with changes / stop / repeat

### G2 · MVP checkpoint · end of week 7 (2026-11-16)
- [ ] Live demo at the sprint 2 review: an instructor creates a quiz, one student joins and answers, the score appears without page reload (evidence: review notes with sponsor feedback)
- [ ] All items of sprints 1 and 2 meet the Definition of Done and velocity of each sprint >= 20 points (evidence: backlog export, velocity chart)
- [ ] Line coverage of new service code >= 70 % (evidence: JaCoCo report in CI)
- [ ] WebSocket test from the campus network with 20 simulated clients, p95 message latency < 1 s (evidence: test report)
- [ ] Hours used <= 308 h (280 h plan + 28 h tolerance) and no open risk with score > 12 (evidence: timesheet total, risk register)

Inputs: sprint 1 and 2 review notes, CI report, timesheet, risk register
Decision maker: sponsor with the PM · Outcomes: continue / continue with changes / stop / repeat

### G3 · Release candidate · end of week 11 (2026-12-14)
- [ ] All Must items and at least 80 % of the Should points meet the DoD (evidence: backlog export)
- [ ] Line coverage >= 80 % on service and realtime packages (evidence: JaCoCo report in CI)
- [ ] Load test with 100 simulated students in 5 concurrent sessions, p95 broadcast latency < 500 ms (evidence: load test report)
- [ ] Security checklist signed, no secret in the repository, 0 open critical and <= 5 open major defects (evidence: checklist file, secret scan, defect list)
- [ ] Hours used <= 476 h (440 h plan + 36 h tolerance) and runbook draft deployed once on a clean VPS (evidence: timesheet, deployment log)

Inputs: sprint 3 and 4 review notes, CI report, load test report, defect list, risk register
Decision maker: sponsor with the PM · Outcomes: continue / continue with changes / stop / repeat

### G4 · Acceptance and closure · end of week 14 (2027-01-04)
- [ ] Pilot held with at least 50 distinct students over at least 2 sessions (evidence: session log export)
- [ ] At least 80 % of the survey answers rate the system 4 or 5 out of 5 (evidence: survey export)
- [ ] 0 open critical defects and at most 3 open major defects, each with a documented workaround (evidence: defect list)
- [ ] A person outside the team redeploys the system from the runbook in <= 60 minutes (evidence: signed test log)
- [ ] Total hours <= 560 h and the sponsor signs the acceptance form (evidence: final timesheet, signed form)

Inputs: pilot log, survey, defect list, runbook, final timesheet, lessons learned log
Decision maker: sponsor · Outcomes: accept and close / accept with changes / extend pilot (repeat) / stop

## Tolerances (manage by exception)
Risk score = probability (1-5) x impact (1-5). Scope tolerance refers to Should points; Must items may never be removed.

| Tolerance    | Stage 1 (W1-3) | Stage 2 (W4-7) | Stage 3 (W8-11) | Stage 4 (W12-14) |
|--------------|----------------|----------------|-----------------|------------------|
| Time         | G1 may slip max 2 working days | each sprint end +/- 1 working day, G2 max +2 days | each sprint end +/- 1 working day, G3 max +3 days | 0 days: pilot start fixed, G4 max +0 days |
| Cost (hours) | +10 % (12 h of 120 h) | +10 % (16 h of 160 h) | +5 % (8 h of 160 h) | 0 % (120 h, no overtime in the pilot week) |
| Scope        | WBS may change up to 2 work packages | max 20 % of Should points moved to Could, 0 Must removed | max 10 % of Should points moved, 0 Must removed | 0 % change, only defect fixes |
| Quality      | max 3 major review comments open at G1 | coverage >= 70 %, 0 critical defects at sprint end | coverage >= 80 %, <= 5 major defects | coverage >= 80 %, 0 critical and <= 3 major defects |
| Risk         | no risk with score > 15 without a response | no risk with score > 12, max 3 risks with score >= 10 | no risk with score > 10, max 2 risks with score >= 10 | no risk with score > 8 |

Escalation: developers -> scrum master -> PM -> sponsor
- A developer informs the scrum master when an item is forecast to slip by more than 1 working day.
- The scrum master informs the PM when the sprint goal or a Must item is at risk, within 1 working day.
- The PM informs the sponsor with an exception report within 2 working days.

Exception report when: any forecast value is expected to leave a tolerance of the current stage, or a Must item cannot be finished before the next gate, or a risk exceeds its threshold for two consecutive weekly reports. Until the sponsor decides, the team continues only work that is unaffected by the deviation.

## Reporting
**Weekly highlight report.** Written by the scrum master, sent to the PM every Friday by 17:00, one page and at most 250 words, with four headings: *Done* (items meeting the DoD, hours used), *Next* (plan for the coming week), *Risks* (top 3 with score) and *Tolerance status* (time, cost, scope, quality, risk as green / amber / red; amber = 75 % of tolerance used).

**Sprint review as checkpoint.** At the end of each sprint the PM attends the review (the sponsor is invited), checks the velocity, burndown and hours against the stage tolerances and records one decision: continue, adjust the backlog, or raise an exception.

**Exception report (three lines).**
1. Deviation: what is forecast to exceed which tolerance, by how much, since when.
2. Options: two or three options with effect on time, hours, scope, quality and risk.
3. Recommendation: the chosen option, the decision needed from the sponsor and the date by which it is needed.

## Closure criteria
| Area                   | Criterion | Verified by | Owner |
|------------------------|-----------|-------------|-------|
| Acceptance             | Sponsor signs the acceptance form after the pilot; all Must items meet the DoD; G4 checklist fully ticked | Sponsor, PM | Product owner |
| Hand-over              | Git repository (tag `v1.0`, README with build and run steps), VPS credentials transferred to the IT department through the agreed password manager and rotated, runbook with deploy, backup, restore and rollback steps tested by a person outside the team | IT department representative | Scrum master |
| Lessons learned        | Four sprint retrospectives documented with closed or carried actions, closure workshop held in week 14 (60 min, whole team and PM), lessons log with at least 8 entries | PM | Scrum master |
| Administrative closure | Final timesheet (total <= 560 h), cash costs reconciled against the 150 USD plan, risk register and issue list closed, domain and VPS renewal owner named, all documents archived in the repository tag `closure` | PM | PM |
