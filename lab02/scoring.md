# Weighted Scoring Analysis · Build, Buy, or Hybrid · Realtime Quiz

## 1. Criteria and Weights (Agreed 2026-10-06, before scoring)
Weights sum to 100 and reflect the educational goals and project constraints of the capstone:
- **Learning value for the capstone (40%):** Measures how much software engineering and architecture experience the 4-student team gains by building it from scratch.
- **Cost within the 200 USD cash budget (25%):** Measures financial feasibility against the fixed cash limit for VPS and domain costs.
- **Time to the week-14 pilot (20%):** Measures confidence in meeting the immovable semester deadline[cite: 1].
- **Fit to the 47 functional requirements (15%):** Measures how closely the solution matches the specific case-study requirements.

## 2. Option Descriptions
- **Build:** The planned in-house development across 10 phases over 12 weeks using Node.js/WebSockets[cite: 1].
- **Buy:** Purchasing a hosted enterprise SaaS quiz platform (e.g., Kahoot! or Slido team tier at ~$40/month × 4 months = $160)[cite: 1].
- **Hybrid:** Buying a live-session WebSocket engine or component library, while building the authoring, analytics, and export features in-house[cite: 1].

## 3. Scoring Table and Evidence
| Criterion | Weight | Build | Buy (SaaS) | Hybrid | Evidence / Notes |
|---|---|---|---|---|---|
| Learning value | 40 | 5 | 1 | 3 | Build maximizes coding experience; Buy offers zero custom engineering value. |
| Cost within budget | 25 | 4 | 3 | 3 | Build uses existing infrastructure ($100 Linode); Buy consumes most cash budget ($160). |
| Time to pilot | 20 | 3 | 5 | 4 | Buy is instantly ready; Build requires 504 hours of development under tight schedule. |
| Fit to requirements | 15 | 5 | 3 | 4 | Build satisfies all 47 FRs precisely; SaaS restricts custom CSV/PDF export formats. |
| **Weighted Score** | **100** | **435** | **260** | **335** | *Computed via SUMPRODUCT in scoring.csv*[cite: 1] |
| **Percent of Max** | | **87%** | **52%** | **67%** | |

## 4. Sensitivity Check
*Shifted 10 points of weight from Learning Value (30) to Fit to Requirements (25):*
- **Build:** $30 \times 5 + 25 \times 4 + 20 \times 3 + 15 \times 5 = 150 + 100 + 60 + 75 = 425$ (85%)
- **Buy:** $30 \times 1 + 25 \times 3 + 20 \times 5 + 15 \times 3 = 30 + 75 + 100 + 45 = 250$ (50%)
- **Hybrid:** $30 \times 3 + 25 \times 3 + 20 \times 4 + 15 \times 4 = 90 + 75 + 80 + 60 = 305$ (61%)

**Conclusion:** The winner remains **Build**, proving the model is robust against weight variations.