# setup.md — Environment Setup (do by 10 Oct)

## Hardware / logistics
- Laptop (16GB RAM ideal), charger, extension board, mouse, mobile hotspot, power bank
- Offline copies of: brain/, cheat sheets, 2–3 datasets, a pip/npm cache

## Core installs
- Git, GitHub account + SSH key
- VS Code (+ extensions in Toolkit.md) or Cursor
- Python 3.11/3.12 + `uv` (or venv)
- Node 20 LTS + pnpm (or npm)
- Docker Desktop (optional but useful)
- Postman/Thunder Client, Chrome

## AI tools
- Claude (Code/app), Cursor or Copilot — have 2 options in case one rate-limits
- Check rate limits/credits BEFORE the event; teammates should use separate accounts

## Accounts (pre-created, logged in on laptop)
GitHub, Vercel, Render or Railway, Supabase (or Neon), Hugging Face, Kaggle, Google Cloud/Firebase (optional), Groq/Gemini API key (free LLM tier)

## Python base (create `requirements.txt` now, test install)
```
fastapi uvicorn[standard] websockets pydantic pandas numpy scikit-learn
statsmodels lightgbm xgboost prophet river shap joblib
sqlalchemy aiosqlite python-dotenv httpx pytest ruff
```
(Prophet can be painful to install — test it; fall back to statsmodels.)

## Frontend base
```
npm create vite@latest web -- --template react-ts
cd web && npm i recharts tailwindcss @tailwindcss/vite lucide-react framer-motion zustand axios
```

## Repo bootstrap (event day, 5 min)
1. Open github.com/<you>/brain-template → green **Use this template** → Create new repository (name it after the project)
2. `git clone <new-repo-url> && cd <new-repo>`
3. Open the folder in your AI tool (Claude Code / Cursor / Codex)
4. Say: "Read brain/BOOTSTRAP.md and follow it. Problem statement: ..."
Branch rule: `main` always runs. Work on `feat/<n>`. Merge every ~2 hrs.

## Sanity test (do this before the event)
1. `uvicorn api.main:app --reload` serves /health
2. React app fetches /health and shows it
3. WebSocket streams a number every second into a chart
4. Deploy this tiny thing to Vercel + Render once, so deploy is no surprise
