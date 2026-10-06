# 🧠 brain-template

A reusable "project brain" for hackathons (and any build). Make a new repo from this template, give an AI your problem statement, and it configures all the docs for you.

## Use it
1. Click **Use this template → Create a new repository**
2. Clone it and open the folder in VS Code (GitHub Copilot Chat → **Agent** mode)
3. Type `/bootstrap` followed by your problem statement, event length and judging criteria
   (or say: `Read brain/BOOTSTRAP.md and follow it. Problem statement: <paste>`)
4. The AI fills the PRD, tailors Architecture / Phases / Design / Rules, then waits for your "go"

## Using a chat AI (no repo access)?
Upload the `brain/` folder (or paste `brain/BOOTSTRAP.md`) and say:
`Follow BOOTSTRAP.md for this problem statement: <paste>`

## What's inside
Everything lives in `brain/`. Start with `brain/README.md`.
Auto-load files make coding AIs read the brain by themselves:
- GitHub Copilot (VS Code): `.github/copilot-instructions.md`, `AGENTS.md`
- Claude Code: `CLAUDE.md`, `.claude/commands/`
- Cursor: `.cursorrules`, `.cursor/rules/`

Copilot chat shortcuts (type in chat): `/bootstrap` `/start` `/task` `/update-memory` `/review` (from `.github/prompts/`)

> Docs only. No app code is included, so it's safe if an event bans pre-written code.
