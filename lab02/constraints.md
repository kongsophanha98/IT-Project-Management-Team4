\# Constraint analysis · Realtime Quiz · v0.1



Evidence uses the Lab-02 brief’s recap of Lab-01, as instructed when charter details are unavailable.



| Constraint | Fixed or flexes | Evidence | If violated |

|---|---|---|---|

| Time | \*\*FIXED — driver\*\* | “14-week semester; go-live is a pilot with 50 students in week 14” (Lab-02 brief, Inputs from Lab-01). | Missing the week-14 pilot misses the semester go-live. |

| Cost | \*\*FIXED\*\* | “Cash budget: 200 USD” (Lab-02 brief, Inputs from Lab-01). | Spending over $200 exceeds the cash budget and needs sponsor approval. |

| Scope | \*\*FLEXES\*\* | `features.csv` has 8 Must, 5 Should, and 4 Could features. Should and Could work can be deferred. | Dropping a Must feature would leave essential pilot functions incomplete. |

| Quality | \*\*FIXED floor\*\* | “broadcast under 500 ms, WCAG AA, CI green” (Lab-02 brief, Quality). | The pilot may be too slow, inaccessible, or unreliable. |

| Resources | \*\*FIXED\*\* | “4 students × 10 h/week = 40 h/week” (Lab-02 brief, Team); 40 × 14 = 560 available hours. | Extra work cannot be assumed; the plan has 56 hours of contingency. |

| Risk | \*\*FLEXES — managed\*\* | The Lab-01 charter’s Risks section identifies that the campus proxy may block WebSocket and suggests testing early and using a fallback. | Real-time participation may fail if WebSocket is blocked and no fallback is ready. |



\## Project shape



Realtime Quiz is a fixed-date, fixed-budget project. Time is the driver because the week-14 pilot date is fixed, and cost is the second fixed side. Scope absorbs surprises: defer Should and Could features before reducing the Must features.



\## Quality floor (never traded)



1\. Broadcast updates reach connected clients in under 500 ms.

2\. Primary quiz flows meet WCAG AA contrast and support keyboard operation.

3\. CI is green on every merge, and line coverage is at least 80% before the pilot.



!\[Iron triangle for Realtime Quiz](triangle.png)

