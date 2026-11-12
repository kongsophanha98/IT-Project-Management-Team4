# Approach comparison · Realtime Quiz
Sources: [project profile](project-profile.md), [charter](../lab01/project-charter.md), [MoSCoW](../lab02/moscow.md), [constraints](../lab02/constraints.md)

| Approach   | Requirements | Sponsor control | First quiz | Two main risks | Fit |
|------------|--------------|-----------------|-----------:|----------------|-----|
| Waterfall  | All requirements frozen in the week-3 baseline; changes only through formal change requests | Milestone review at the end of each phase; the sponsor sees a working system only after integration | week 12 | 1. WebSocket and campus-proxy problems and outdated Spring Boot 4 examples are found only at integration in week 12. 2. Screens and real-time behaviour are not specified, so the result may not match the sponsor's expectation and there is no time left to change it before the week-14 pilot. | low: strong on governance (5), weak on technical uncertainty (1) and early feedback (1) |
| Pure Scrum | Product backlog reordered every sprint; no baseline | Sprint review every 2 weeks, but no gate to stop or re-plan; budget tracked only by velocity | week 7 | 1. A first-time Scrum team drifts without an approved plan. 2. The fixed pilot date and the 560 h budget are not protected, and Could features creep into the backlog. | medium: strong on feedback (5) and uncertainty (5), weak on the governance criterion (2) and team experience (2) |
| Hybrid     | Must list baselined at G1 (week 3); Should and Could items are reordered per sprint inside that scope | Four gates G1-G4 plus a sprint review every 2 weeks; tolerances per stage | week 7 | 1. Gates and reports consume part of the 10 h/week per student. 2. The team is new to both Scrum and gate governance, and backlog changes can conflict with the baseline. | high: balances governance (4), uncertainty (4) and early feedback (4) |

Columns: how requirements are handled · how the sponsor controls the project (governance) · week in which the sponsor first plays a working quiz · two main risks · fit with the Task 1 profile.

"First quiz" is the first week in which the sponsor can play a quiz live. Sprint 1 (weeks 4-5) delivers login and quiz authoring only, so the first playable quiz is shown at the sprint 2 review in week 7 (2026-11-16, gate G2). In waterfall it appears at integration testing in week 12.

## Weighted score (from approach-scoring.csv)
Weights are copied from the Task 1 profile and add up to 100. Fit scores run from 1 (poor) to 5 (excellent). Formula in the spreadsheet: `=SUMPRODUCT($B$2:$B$6,C$2:C$6)/100`, copied across to D and E.

| Criterion                            | Weight | Waterfall | Scrum | Hybrid |
|--------------------------------------|-------:|----------:|------:|-------:|
| Requirements stability               | 25     | 3         | 4     | 4      |
| Technical uncertainty                | 25     | 1         | 5     | 4      |
| Team experience with agile           | 15     | 4         | 2     | 3      |
| Contract and governance constraints  | 20     | 5         | 2     | 4      |
| Need for early delivery and feedback | 15     | 1         | 5     | 4      |
| **Weighted score**                   | 100    | **2.75**  | **3.70** | **3.85** |

Hand check for Hybrid: (25 x 4 + 25 x 4 + 15 x 3 + 20 x 4 + 15 x 4) / 100 = 385 / 100 = 3.85.

Waterfall 2.75 · Scrum 3.70 · Hybrid 3.85

## Sensitivity
- Test 1: governance weight 20 -> 10 and early delivery weight 15 -> 25. Waterfall 2.35, Scrum 4.00, Hybrid 3.85. Scrum moves ahead by 0.15, so the hybrid lead depends on the governance criterion keeping a weight of about 20.
- Test 2: team experience weight 15 -> 25 and technical uncertainty weight 25 -> 15 (the criterion hardest to judge, because the proxy and framework risks are not yet tested). Waterfall 3.05, Scrum 3.40, Hybrid 3.75. Hybrid stays first and its lead grows to 0.35.

## Recommendation
Choose the Hybrid approach (3.85). The runner-up is pure Scrum (3.70). I would choose Scrum instead only if the sponsor drops the week-3 plan approval and the stage gates, and attends every sprint review, because then the governance weight falls and Test 1 shows Scrum ahead.
