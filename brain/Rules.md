# Rules.md — AI Guardrails

## Always
- Read Memory.md, then this file, before coding.
- Work only on the current phase and task given.
- Show a 3-bullet plan, then code. Keep diffs small.
- Type everything: Python type hints + Pydantic; TypeScript strict.
- Handle errors: try/except at service boundaries, return clean JSON errors `{error, detail}`, log with `logging` (no bare print in api/).
- Keep secrets in `.env`; update `.env.example`. Never hardcode keys.
- Add a fallback for every external dependency (API, dataset, LLM) so the demo never dies.
- Write 1 smoke test per endpoint for core paths.
- Run the code/tests before saying it works.
- Ask when requirements are unclear instead of guessing.

## Never
- Don't add libraries not in the Allowed list without asking.
- Don't rewrite or refactor unrelated files.
- Don't invent APIs/functions — check docs (Context7) or ask.
- Don't scan the whole repo; open only needed files.
- Don't commit data >20MB, models >50MB, or `.env`.
- Don't use placeholder/fake metrics in the pitch; label simulated data honestly.
- Don't leave TODO-silent failures.

## Allowed libraries
Python: fastapi, uvicorn, pydantic, pandas, numpy, scikit-learn, statsmodels, lightgbm, xgboost, prophet, river, shap, joblib, sqlalchemy, httpx, python-dotenv, pytest, ruff, aiosqlite, websockets, pyod, duckdb, redis
JS: react, react-dom, typescript, vite, tailwind (@tailwindcss/vite), recharts, echarts, plotly.js, zustand, axios, lucide-react, framer-motion, react-router, leaflet
BOOTSTRAP may add more under a heading "Added for this project" below. Anything else: ask first.

### Added for this project
(none yet)
## Avoid
TensorFlow/PyTorch (heavy) unless PS requires deep learning; Kafka/Spark (overkill); large UI kits that slow setup; Redux.

## Code style
- Python: ruff, snake_case, functions <40 lines, docstring on public funcs
- TS: functional components, hooks, camelCase, no `any`
- Commits: `feat:`, `fix:`, `chore:`, `docs:` — commit after each working task

## Definition of done (per task)
Runs locally, no console errors, matches PRD item, committed, Memory.md updated if milestone.

## Escalation
Stuck >20 minutes → simplify scope or swap approach. Tell the lead.
