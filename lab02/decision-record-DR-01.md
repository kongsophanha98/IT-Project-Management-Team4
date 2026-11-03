# DR-01 · Open-day demo scope, week 10

Status: approved 2026-10-23 · Requested by: Head of IT (sponsor) · Recorded by: PM (supervising lecturer)

## Context

The sponsor asked for every Should feature to be demonstrable at the open day in week 10; the week-14 pilot stays. Fixed facts:

- C-01 Pilot with 50 students in week 14 (charter date; CR-03 asking for week 12 is still undecided, due 2026-10-30).
- C-02 Capacity 4 x 10 h/week = 40 h/week; W5-W10 = 240 h.
- C-03 Cash budget 200 USD, so no paid capacity.
- Remaining Must work: 300 - 148 = 152 h. Should total: 86 h (F09 20, F10 30, F11 24, F12 12). Needed with a 10 % buffer: 262 h, a 22 h shortfall (0.55 week).

## Options considered

| Option                                  | Time                       | Cost                                                | Quality                                                                        |
| --------------------------------------- | -------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------ |
| 0 Everything by W10 (original request)  | +0.55 week or 22 h missing | 0 USD (paying 22 h would cost 264 USD, breaks C-03) | Buffer 0 h; Must work at risk                                                  |
| 1 Must + F09 (20 h) + F10 (30 h) by W10 | 202 h in 240 h, 0 weeks    | 0 USD                                               | Buffer 38 h; F11 and F12 at the pilot                                          |
| 2 Demo with mocked analytics (8 h)      | 180 h in 240 h, 0 weeks    | 0 USD                                               | Buffer 60 h; 8 h throwaway; real Should work (66 h) in W11-W12 with 14 h spare |

## Decision

Option 1 (counter-proposal 1). F09 Responsive design and F10 Analytics move to a new W10 "Open day demo" milestone. F11 Export and F12 Notifications stay at the W14 pilot. No Could work starts before W11.

## Consequences

- New milestone "Open day demo" in W10 in the schedule baseline; scope baseline updated by W5.
- Won't for the W10 demo: F11, F12 (move to the pilot), F13, F14, F15, F16 (Could, no work before W11). F17 stays Won't for the pilot (Task 2).
- New risk R-10 "Demo on unfinished analytics" (fallback: mocked data, 8 h, inside the 38 h buffer); assumption A-08 added to the log.
- New risk R-11 "CR-03 moves the pilot to W12": the W11-W12 window shrinks to 80 h for 36 h of Should and the Could class; re-check when the sponsor decides CR-03.

## Approvers

- Head of IT (sponsor), approved 2026-10-23
- Supervising lecturer (project manager), approved 2026-10-23
- Team lead (student), acknowledged 2026-10-23

Linked from: lab02/README.md (Decisions) and the schedule baseline.
