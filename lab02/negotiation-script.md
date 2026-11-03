# Negotiation · sponsor asks for all Should features by week 10

Scenario: end of week 4 (2026-10-23). The week-14 pilot stays. Two sprints are done.

## Data sheet (week 4)

| Measure                                                         | Value                                  |
| --------------------------------------------------------------- | -------------------------------------- |
| Capacity W5-W10                                                 | 6 x 40 = 240 h                         |
| Must remaining (300 h, 148 h done)                              | 300 - 148 = 152 h                      |
| Should total (Task 2 rating: F09 20 + F10 30 + F11 24 + F12 12) | 86 h                                   |
| Needed by W10 = Must remaining + Should                         | 152 + 86 = 238 h                       |
| Surplus on paper, 0 h contingency, Could untouched              | 240 - 238 = 2 h                        |
| Contingency at the project's 10 % rate                          | 10 % x 238 = 24 h                      |
| Needed with contingency                                         | 238 + 24 = 262 h                       |
| Shortfall by W10 with contingency                               | 262 - 240 = 22 h = 22 / 40 = 0.55 week |
| Velocity, sprints 1-2 (points done)                             | 18, 21 -> 19.5 avg                     |

Conclusion: "everything by week 10" has 2 h of slack on paper and a 22 h (0.55 week) shortfall once the standard buffer is kept. It is not fundable without a change.

## Script

**Sponsor 1:** I need every Should feature demonstrable at the open day in week 10. It is mostly small stuff, a small change really.

**PM 1:** Let me size "small" together. The four Should features total 86 h, on top of 152 h of Must work still open. That is 238 h against 240 h of capacity in weeks 5 to 10.

**Sponsor 2:** So it fits. Then there is no problem.

**PM 2:** It fits by 2 h, with zero contingency. We keep a 10 % buffer on every estimate, which is 24 h here. With it we need 262 h against 240 h, a gap of 22 h, about half a week.

**Sponsor 3:** Then work a bit harder. 22 h is not much for four people over six weeks.

**PM 3:** The team capacity is 4 x 10 h/week = 40 h/week, fixed by the course (C-02). Our sprint 1 delivered 18 points against an average of 19.5, which is 8 % lower; the same dip over 240 h costs about 18 h and uses almost all of the 22 h gap.

**Sponsor 4:** Other teams manage this kind of scope. Last year's team showed everything at their open day.

**PM 4:** I am happy to compare with their numbers if you share their hours. For our team the arithmetic is 262 h needed against 240 h available, and our velocity of 19.5 points per sprint is the only evidence we have.

**Sponsor 5:** Fine. Keep the target and we decide later, in week 8, whether anything needs to be cut.

**PM 5:** Waiting costs hours. Each week spends 40 h of the 240 h. After two weeks 160 h remain against 262 h needed, so the gap grows from 22 h to 102 h. A decision today keeps a buffer of 38 h in one of the options below.

**Sponsor 6:** What can you actually give me for the open day, then?

**PM 6:** Here are two ways to give you a strong open day. Option 1: Must complete plus Responsive design (20 h) and Analytics (30 h) by week 10, so 152 + 20 + 30 = 202 h and a 38 h buffer. It displaces Export (24 h) and Notifications (12 h), which move to the week-14 pilot, and no Could work starts before week 11. Option 2: a demo build with mocked analytics (8 h): 152 + 20 + 8 = 180 h and a 60 h buffer. It displaces 8 h of throwaway work and pushes real Analytics (30 h), Export (24 h) and Notifications (12 h), 66 h in total, into weeks 11 and 12 (80 h of capacity), leaving 14 h and no Could work.

**Sponsor 7:** Option 2 looks safer, but real analytics is what the visitors want to see. How risky is option 1?

**PM 7:** The 38 h buffer is 16 % of the 240 h and above the 24 h standard buffer. The risk is that Analytics (30 h) slips; I will log it as R-10 and keep the 8 h mocked-data fallback ready, which fits inside the 38 h.

**Sponsor 8:** Then I choose option 1.

**PM 8:** Understood. I will record this as DR-01 today (2026-10-23) and update the baseline by W5: a new milestone "Open day demo" in W10, Export and Notifications at the W14 pilot, and the risk R-10 in the register.
