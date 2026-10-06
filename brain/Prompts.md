# Prompts.md — Copy-paste prompts

## Bootstrap (first prompt of every new project)
"Read brain/BOOTSTRAP.md and follow it. Problem statement: <paste>. Event: <duration, team size>. Judging: <criteria>."

## Decode PS → PRD
"Here is the problem statement and judging criteria: <paste>. Using brain/PS_Decoder.md, give me 3 solution options scored on wow/feasibility/data, recommend one, then fill brain/PRD.md. Keep MVP to 3 must-haves."

## Tailor architecture
"Based on brain/PRD.md, adjust brain/Architecture.md and brain/Phases.md for this project. Keep the default stack unless the PS requires otherwise. List what changed."

## Scaffold
"Phase 0 only. Create the folder structure from Architecture.md, hello-world FastAPI with /health, Vite React page calling it, .env.example, README run steps. Nothing else."

## Data pipeline
"Phase 1. Write scripts/replay_stream.py that replays data/processed/<file>.csv over WebSocket /ws/stream at configurable speed. Add Pydantic schema for messages."

## Model
"Phase 2. Build a naive baseline and a LightGBM/statsmodels model for <target>. Report MAE/RMSE on a time-based split. Save artifact with joblib. Add a predict() service function."

## Dashboard
"Phase 3. Build Dashboard page per brain/Design.md: KPI cards, live chart with forecast dashed line and confidence band, alerts panel. Use hooks/useStream.ts."

## Wow feature
"Phase 4. Add SHAP-based 'why this prediction' panel (top 5 features) via /api/explain and a card in the UI."

## Review
"Review my git diff against brain/Rules.md. List violations, bugs, and missing error handling. Don't change code yet."

## Debug
"Error: <paste>. File: <path>. Expected: <x>. Give root cause first, then minimal fix."

## Context handoff
"Update brain/Memory.md with current state so a new chat can continue with zero re-reading."

## Pitch deck
"Create a 7-slide deck from brain/PRD.md and brain/Pitch.md: problem, solution, live demo, architecture, impact, tech/differentiator, roadmap/team."
