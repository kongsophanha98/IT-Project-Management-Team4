# Scrum setup - Realtime Quiz

## Roles

| Role | Person | Accountable for | Not responsible for |
|---|---|---|---|
| Product owner | Student A | Maximizing product value; setting the product goal; ordering and clarifying the product backlog | Assigning work to Developers or facilitating every Scrum event |
| Scrum master | Student B | Establishing Scrum; helping the team use Scrum effectively; removing impediments | Owning the product backlog or assigning work |
| Developers (all four) | Students A, B, C and D | Creating a usable, quality increment each sprint; planning and adapting the Sprint Backlog | Taking requirements or task assignments from the sponsor or PM |
| Project manager (lecturer, outside Scrum) | Mr. Tongsreng, supervising lecturer | Predictive plan, schedule, budget, gate evidence and exception reporting | Directing the Developers' day-to-day work or replacing the Product Owner |
| Sponsor (Head of IT) | Head of IT | Funding and major scope/date decisions; timely feedback at sprint reviews | Managing the Sprint Backlog or directing Developers during a sprint |

Student A also develops, so their development work is limited to agreed Sprint Backlog items and another Developer checks their work against the published acceptance criteria; Student B is the separate Scrum Master.

## Sprint goal (sprint 1, weeks 4-5)

By the end of Sprint 1, an instructor can sign in, create and save a multiple-choice quiz, manage its questions and set a timer for each question.

## Event calendar - sprint 1

All times are Cambodia ICT (UTC+7). The sprint dates follow the Gantt: 20 October through 2 November 2026.

| Event | Date(s) | Time | Timebox | Attendees | Output |
|---|---|---|---|---|---|
| Sprint planning | Tue 20 Oct 2026 | 13:00-17:00 | 4 h maximum | Scrum Team | Sprint Goal, selected Product Backlog items and initial Sprint Backlog |
| Daily scrum (one row for all ten weekdays) | 21, 22, 23, 26, 27, 28, 30 Oct and 2 Nov 2026 | 09:00-09:15 | 15 min maximum | Developers; Scrum Master facilitates if needed | Inspection of progress toward the Sprint Goal and an updated plan for the next day |
| Backlog refinement | Wed 28 Oct 2026 | 13:00-14:00 | 1 h | Product Owner, Developers and Scrum Master | Clarified and estimated candidate backlog items for a later sprint |
| Sprint review (sponsor invited) | Mon 2 Nov 2026 | 10:00-12:00 | 2 h maximum | Scrum Team, Head of IT invited, PM | Inspected increment, stakeholder feedback and updated Product Backlog |
| Sprint retrospective | Mon 2 Nov 2026 | 13:00-14:30 | 1.5 h maximum | Scrum Team | A small number of actionable improvements for the next sprint |

There is no daily scrum on 20 October; sprint planning that afternoon starts the sprint and the first daily scrum is on 21 October.

Public holiday: Thursday 29 October is King's Coronation Day in Cambodia, so the daily scrum is skipped that day. Daily scrums are held on the other working days of the sprint, which keeps the timebox at 15 minutes. Holiday listing: [Cambodia public holidays 2026](https://www.officeholidays.com/countries/cambodia/2026).

## Definition of ready

1. The item cites one or more requirement IDs present in the MoSCoW list; enabling project setup may use `-`.
2. Testable acceptance criteria are written in Given/When/Then form.
3. The Developers have agreed a Fibonacci story-point estimate.
4. Dependencies are named, sequenced and available, or have a clear plan to resolve them.
5. A simple sketch or technical flow is linked and reviewed by the Product Owner and Developers.

## Definition of done

1. The item meets its acceptance criteria and is integrated into the shared codebase.
2. The CI build completes successfully.
3. All required automated unit and integration tests pass in CI.
4. CI reports at least 80% line coverage for new or changed service code.
5. Changes receive a peer review and required review feedback is resolved.
6. No open critical or high-severity defect is known in the completed work.
7. Relevant technical and user-facing documentation is updated.
8. The increment is deployable using the team's documented process, with no secrets committed.

## Planning velocity

Planning velocity: 30 points; capacity: 80 hours (4 students x 10 h/week x 2 weeks); Sprint 1 backlog: 29 points.

## Sprint 1 item sketches

These low-fidelity flows are the sketch references for the backlog items; the item dependencies are recorded in the CSV.

### B-01 - Project skeleton and CI

`Source change -> CI build -> automated tests -> coverage report`

### B-02 - Account login

`Login form -> credential check -> authenticated account`

### B-03 - Role authorization

`Account -> role check -> permitted action OR access denied`

### B-04 - Create and save quiz

`Quiz list -> create quiz form -> saved quiz draft`

### B-05 - Add multiple-choice question

`Quiz editor -> question and answer options -> select correct answer -> save`

### B-06 - Edit or remove question

`Question list -> edit/remove action -> updated question list`

### B-07 - Set question timer

`Question editor -> timer value -> saved question settings`
