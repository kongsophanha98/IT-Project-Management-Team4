# Change Requests and Trade-Off Analysis · Realtime Quiz
*Capacity: 40 h/week · Contingency: 56 h · Paid capacity rate: 12 USD/h*[cite: 1]

## CR-01 · Add chat (F14, 40 h) to Must scope · Requested by Sponsor
| Option | Time Impact | Cost Impact | Quality / Scope Impact | Fixed Side? |
|---|---|---|---|---|
| A. Slip the pilot | +1 week (40/40 h) | 0 USD | Delays graduation check | **Violates C-01** (Fixed date) |
| B. Swap: defer F13 (Multimedia, 24h) + F12 (Notifications, 12h) + 4h buffer | 0 weeks | 0 USD | Text-only quiz during pilot; notifications dropped | **OK** |
| C. Pay for TA capacity | 0 weeks | $40 \times 12 = $480 | Full chat added without scope loss | **Violates C-03** (Cash budget $200) |

**Recommendation:** **Option B.** It preserves the fixed pilot date and cash budget by swapping out lower-priority Should features that have valid workarounds for a pilot.

---

## CR-02 · Add anonymous joining with nickname (F15, 12 h) · Requested by Students
| Option | Time Impact | Cost Impact | Quality / Scope Impact | Fixed Side? |
|---|---|---|---|---|
| A. Slip the schedule | +0.3 weeks | 0 USD | Minor schedule compression | **Violates C-01** |
| B. Swap: defer F17 (Admin role, 12 h rated Won't) | 0 weeks | 0 USD | PM continues manual SQL account management | **OK** |
| C. Decline request | 0 weeks | 0 USD | Students must use authenticated university logins | **OK** |

**Recommendation:** **Option B.** Swapping out F17 (which was already rated Won't in MoSCoW) accommodates student convenience without breaking time or cost constraints.

---

## CR-03 · Semester shortened by 2 weeks: pilot moves to week 12 · Requested by Dean
*Capacity lost:* $2 \text{ weeks} \times 40\text{ h} = 80\text{ h}$. *Contingency shrinks:* $56\text{ h} \rightarrow 48\text{ h}$ (10% of new 480h capacity). Planned work (504 h) now exceeds capacity (480 h) by 24 h before risks.

| Option | Time Impact | Cost Impact | Quality / Scope Impact | Fixed Side? |
|---|---|---|---|---|
| A. Keep all Must, drop all Should/Could items (F10-F17 = 94 h) | 0 weeks | 0 USD (saves 94h effort) | Must features intact; analytics/export deferred | **OK** |
| B. Keep full scope, pay TA for 104 h | 0 weeks | $104 \times 12 = \$1,248$ | Full scope delivered on time | **Violates C-03** ($200 budget) |
| C. Keep scope, keep pilot in week 14 | +2 weeks | 0 USD | Direct violation of academic calendar | **Violates C-01** (Dean's constraint) |

**Recommendation:** **Option A.** It restores a 70-hour buffer (larger than original contingency), protects all Must requirements, and strictly obeys both the new time constraint and cash budget.

---

## Change Request Process Flow
```mermaid
flowchart LR
    R["Change request CR-nn arrives"] --> S{"Inside the scope baseline?"}
    S -- "yes" --> D["Do it, log it, no trade-off"]
    S -- "no" --> I["Estimate time, cost, quality"]
    I --> O["Options: slip, swap, pay, decline"]
    O --> P{"Sponsor decides"}
    P -- "approve" --> B["Re-baseline, decision record"]
    P -- "reject" --> L["Record, keep baseline"]