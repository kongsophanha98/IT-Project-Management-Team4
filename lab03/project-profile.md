# Project profile · Realtime Quiz

Sources: [project charter](../Lab-01-Realtime%20%20%20-Quiz/Lab-01-Realtime-Quiz/lab01/project-charter.md), [MoSCoW requirements (`features.csv`)](../lab02/features.csv)

| # | Criterion | Evidence (one fact) | Weight | Adaptive score (1–5) | W × S |
|---|---|---|---:|---:|---:|
| 1 | Requirements stability | The requirements list fixes 8 Must features, while 5 Should and 4 Could features leave lower-priority scope flexible. | 25 | 3 | 75 |
| 2 | Technical uncertainty | The charter identifies campus proxy WebSocket blocking and late-answer race conditions as risks. | 25 | 4 | 100 |
| 3 | Team experience with agile | The brief says the four students are doing their first Scrum project. | 15 | 2 | 30 |
| 4 | Contract and governance constraints | The charter requires sponsor approval for changes to Must scope, milestone dates, or the $200 cash cap. | 20 | 2 | 40 |
| 5 | Need for early delivery and feedback | The charter schedules an MVP demo in week 7 and a 50-student pilot in week 14. | 15 | 5 | 75 |
|   | **Profile** = SUM(W × S) / 100 | **(75 + 100 + 30 + 40 + 75) / 100 = 3.20** | **100** |  | **3.20** |
| 6 | (optional) Sponsor availability | The Head of the IT Department is named as sponsor, but the charter does not confirm reviews every two weeks. | – | 3 (provisional) | – |

Score 1–5: 1 = the fact favours a predictive approach; 5 = the fact favours an adaptive approach. The sponsor availability score is provisional and excluded from the total.

Interpretation: < 2.5 predictive · 2.5–3.5 hybrid · > 3.5 agile

## Profile summary

Realtime Quiz has a defined Must scope and fixed milestones, with technical risks and room to refine lower-priority requirements as the team learns. Requirements stability and technical uncertainty dominate the profile at 25% weight each. The weighted score is 3.20 in the hybrid band, so Task 2 should compare predictive, agile, and hybrid approaches.
