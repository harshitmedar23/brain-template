# PRD.md — Product Requirements Document
Status: TEMPLATE (BOOTSTRAP.md fills this). Fill from PS_Decoder.md within first 30 minutes of the event.

## 1. Project name & tagline
<Name> — <one line value>

## 2. Problem
<2–3 sentences from the PS>

## 3. Target users
| Persona | Role | Pain | What they need |
|---|---|---|---|
| | | | |

## 4. Goals & success metrics
- Primary goal:
- Metrics (demo-able): prediction accuracy (MAE/F1), latency <1s, alerts raised, time saved

## 5. Scope
### Must-have (MVP)
1. Live data ingestion (real or replayed stream)
2. Prediction/forecast served in real time
3. Dashboard showing live + predicted values
### Should-have
4. Anomaly alerts
5. Explainability ("why this prediction")
6. What-if / scenario slider
### Could-have
7. Auth/roles, 8. Export report, 9. Mobile responsive, 10. Multilingual
### Out of scope
-

## 6. User stories
- As a <user>, I want <action> so that <benefit>.

## 7. Functional requirements
| ID | Requirement | Priority | Phase |
|---|---|---|---|
| FR-1 | | Must | 1 |

## 8. Non-functional
Latency, reliability (works offline/replay), simple deploy, secure keys, clean UI.

## 9. Data
Source(s), schema, volume, refresh rate, license, how we simulate streaming.

## 10. Model plan
Baseline → better model → evaluation metric → explainability. Keep a naive baseline to show improvement.

## 11. Demo story (60 sec)
1. Problem hook 2. Live data flowing 3. Prediction + alert 4. Explain why 5. Impact numbers

## 12. Assumptions & risks
-
