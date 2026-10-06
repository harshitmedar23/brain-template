# instruction.md — How to work with the AI

## Principles
1. One phase at a time. Never ask "build the whole app".
2. Docs are the spec. If it's not in PRD/Architecture, ask before adding.
3. Small prompts, small diffs, run it, commit it.
4. After every working milestone: update Memory.md.
5. New chat/tool? Paste the Session Start prompt. Don't re-explain.

## Session Start prompt (paste in every new chat)
```
Read these files in order: brain/Memory.md, brain/Rules.md, brain/PRD.md, brain/Architecture.md, brain/Phases.md.
If Memory.md says UNCONFIGURED, read brain/BOOTSTRAP.md instead and follow it.
Do NOT read the whole codebase. Tell me: (1) what is done, (2) current phase, (3) the next 3 tasks.
Wait for my go-ahead before writing code.
```

## Task prompt template
```
Phase: <N>. Task: <one clear task>.
Files you may touch: <paths>.
Done when: <testable outcome>.
Follow brain/Rules.md. Show the plan in 3 bullets first, then code.
```

## Session End prompt
```
Update brain/Memory.md: what we finished, files changed, decisions made, bugs open, next steps. Keep it under 60 lines.
```

## Auto-load pointer (root of repo)
ALREADY INCLUDED in the template. If you ever need to recreate them, make these at repo root so tools load the brain automatically (same content in each):
- `CLAUDE.md` (Claude Code)
- `AGENTS.md` (Codex / generic)
- `.cursor/rules/brain.mdc` or `.cursorrules` (Cursor)
Content:
```
Before doing anything, read brain/Memory.md and brain/Rules.md.
Project docs live in brain/. Follow brain/Phases.md. Never scan the full repo unless asked.
Update brain/Memory.md after each milestone.
```

## When AI drifts
Say: "Stop. Re-read brain/Rules.md and brain/Phases.md. We are on Phase X, task Y only."

## Debug protocol
Paste: exact error + file + what you expected. Ask for root cause first, fix second. Max 3 attempts, then change approach (simplify or swap library).

## GitHub Copilot (VS Code) quick use
- Use Copilot Chat in **Agent** mode.
- Auto-loaded: `.github/copilot-instructions.md` (points to the brain).
- Shortcuts in chat: `/bootstrap <problem statement>` first, then `/start` in each new chat, `/task <one task>` while building, `/update-memory` at the end, `/review` before merging.
- If it drifts: "Stop. Re-read brain/Rules.md and brain/Phases.md. We are on Phase X, task Y only."
