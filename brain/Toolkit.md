# Toolkit.md — Skills, Plugins, Extensions, MCP, Libraries

## VS Code / Cursor extensions
Python + Pylance, Ruff, Jupyter, ESLint, Prettier, Tailwind CSS IntelliSense, ES7 React snippets, Error Lens, GitLens, Thunder Client, Docker, Live Share (team pairing), Markdown Preview Enhanced, Path Intellisense, Better Comments

## MCP servers (give the AI tools)
- **Context7** — up-to-date library docs (stops hallucinated APIs)
- **GitHub** — issues/PRs/commits
- **Filesystem** — scoped project access
- **Playwright** — AI can test the UI in a browser
- **Supabase/Postgres** — query DB directly
- **Sequential Thinking** — better planning on hard tasks

## Claude Code helpers
- Custom slash commands in `.claude/commands/`:
  - `start.md` → Session Start prompt
  - `update-memory.md` → Session End prompt
  - `decode-ps.md` → runs PS_Decoder
  - `review.md` → "review diff against Rules.md"
- Subagents (optional): reviewer, test-writer, ui-polisher
- Skills for docs: pptx (pitch deck), pdf, docx, xlsx — use Claude to produce the final deck/report quickly

## Real-time predictive analytics libraries
| Need | Use |
|---|---|
| Forecasting | statsmodels (Holt-Winters/SARIMAX), Prophet, LightGBM with lag features |
| Online learning | river |
| Anomaly detection | IsolationForest, rolling z-score, EWMA, PyOD |
| Explainability | SHAP |
| Streaming | FastAPI WebSocket / SSE, Redis Streams (optional), Kafka only if PS demands |
| Storage | SQLite → Postgres (Supabase), DuckDB for fast analytics |
| Charts | Recharts, Plotly, ECharts |
| Maps | Leaflet / Mapbox |
| LLM insight layer | Gemini/Groq free tier for "explain this prediction" text |

## Datasets to pre-download (Kaggle / UCI / public)
Energy consumption, NYC taxi, air quality (AQI), stock/crypto ticks, IoT sensor/predictive maintenance (NASA C-MAPSS), weather, traffic, retail sales, patient vitals (MIMIC demo), agriculture/crop prices (AGMARKNET). Keep each as CSV + a "replay as stream" script idea.

## Deploy
Frontend: Vercel/Netlify. Backend: Render/Railway/Fly. Fallback: ngrok or Cloudflare Tunnel from laptop.

## Pitch/design tools
Figma (optional), Canva, Excalidraw (architecture diagram), Loom/OBS (backup demo video), Mermaid (diagrams in docs)
