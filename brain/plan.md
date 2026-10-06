# plan.md — Master Plan

Event: Manthan hackathon, 29 Oct 2026. Problem statement revealed on the spot.
Likely domain (from site): Real Time Predictive Analytics (Domain_001). Other domains may exist — prep generic, lean data/ML.

## Strategy
We can't know the PS, so we prepare: (1) the doc system, (2) a decoding routine, (3) tooling that works, (4) practice runs. Winning = clear problem fit + working live demo + clean story, not feature count.

## Check first (IMPORTANT)
Read the hackathon rules: is pre-written code/boilerplate allowed? If "no pre-built code", prep only docs, tools, accounts and practice — NOT a starter app. Never risk disqualification.

## Prep timeline (3 Oct → 28 Oct)
**Week 1 (3–9 Oct) — Foundation**
- Finalize brain/ docs, create GitHub org/repo template (docs only)
- Install everything in setup.md on every teammate's laptop
- Create accounts: GitHub, Vercel, Render/Railway, Supabase, Hugging Face, Kaggle
- Decide team roles (below)

**Week 2 (10–16 Oct) — Skills drill**
- Each person: build a tiny live-streaming demo (fake data → API → chart) in <3 hrs
- Practice: sklearn forecasting, anomaly detection, FastAPI WebSocket, React chart
- Collect 5 datasets (Datasets list in Toolkit.md)

**Week 3 (17–23 Oct) — Full dress rehearsal**
- Mock hackathon: pick a random PS (e.g. "predict traffic congestion", "predict machine failure"), run PS_Decoder.md, build MVP in 6 hrs using the brain workflow
- Time each phase; fix bottlenecks
- Practice the 3-min pitch (Pitch.md) twice

**Week 4 (24–28 Oct) — Polish & rest**
- Re-run a mock, update templates with lessons learned
- Pack: laptops, chargers, extension boards, hotspot, ID, water bottle
- Test internet fallback (mobile hotspot), offline docs, local-only demo mode
- Sleep. Seriously.

## Event-day schedule (assume 24h; scale proportionally if different)
| Time | Phase | Output |
|---|---|---|
| 0:00–0:30 | Decode PS (PS_Decoder.md) | PRD.md filled |
| 0:30–1:15 | Brain setup | Architecture/Phases/Design tailored, repo up |
| 1:15–3:00 | Phase 1: data + skeleton | API + fake/real data streaming |
| 3:00–8:00 | Phase 2: core model/feature | the thing that solves the PS |
| 8:00–13:00 | Phase 3: dashboard UI | live visuals |
| 13:00–17:00 | Phase 4: wow feature + robustness | explainability / alerts / what-if |
| 17:00–20:00 | Phase 5: deploy + polish | public URL + fallback |
| 20:00–22:00 | Pitch + demo rehearsal | Pitch.md done |
| 22:00–24:00 | Buffer / submission | Never build new features here |

Feature freeze at 75% of total time.

## Roles (3–4 people)
- **Lead/Integrator**: owns brain docs, Memory.md, git merges, pitch
- **Data/ML**: datasets, models, evaluation, explainability
- **Backend**: API, streaming, DB, deploy
- **Frontend/Design**: dashboard, UX, demo flow
(Fewer people → combine; everyone must understand the pitch.)

## Risks & mitigations
| Risk | Mitigation |
|---|---|
| Wi-Fi dies | Hotspot + local demo mode + cached data |
| AI hallucinates libs | Rules.md allowed-libs list + Context7 MCP |
| Merge conflicts | Feature branches by folder ownership |
| Scope creep | Phases.md + feature freeze |
| Live demo breaks | Pre-recorded 60s backup video + seeded data |
| PS is not data-related | PS_Decoder.md has generic path; stack stays flexible |
