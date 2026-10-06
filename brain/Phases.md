# Phases.md — Build Order
Mark each task [ ] → [x]. AI works on ONE phase at a time. Times assume 24h event.

## Phase 0 — Decode & Setup (0:00–1:15)
- [ ] PS_Decoder.md filled, PRD.md finalized
- [ ] Tailor Architecture.md, Design.md
- [ ] Repo + branches + CLAUDE.md pointer + .env
- [ ] Hello-world API + web connected

## Phase 1 — Data & Skeleton (1:15–3:00)
- [ ] Load/clean dataset, save processed sample
- [ ] Replay-stream script
- [ ] /health, /api/history, /ws/stream working
- [ ] Dashboard shell with live line chart

## Phase 2 — Core Intelligence (3:00–8:00)
- [ ] Baseline model + metric
- [ ] Improved model, compare vs baseline
- [ ] Real-time inference in stream
- [ ] Persist model artifact, load at startup
- [ ] Unit/smoke tests

## Phase 3 — Dashboard & UX (8:00–13:00)
- [ ] KPI cards, forecast chart with confidence band
- [ ] Alerts panel
- [ ] Loading/empty/error states
- [ ] Responsive layout

## Phase 4 — Wow Feature (13:00–17:00)
Pick ONE: explainability (SHAP), what-if simulator, auto-generated insights (LLM), map view, alert notifications (email/Telegram)
- [ ] Implement
- [ ] Add to demo flow

## Phase 5 — Deploy & Harden (17:00–20:00)
- [ ] Deploy web + api, env vars set
- [ ] Seeded demo mode + offline fallback
- [ ] README with run steps, architecture diagram, screenshots
- [ ] Backup demo video (60–90 sec)

## Phase 6 — Pitch (20:00–22:00)
- [ ] Deck (Pitch.md structure), 3-min rehearsal ×3
- [ ] Q&A prep
- [ ] Feature freeze already happened; only bug fixes

## Phase 7 — Submit (22:00–24:00)
- [ ] Submit repo/links/video on time
- [ ] Final git tag `v1.0-submission`
