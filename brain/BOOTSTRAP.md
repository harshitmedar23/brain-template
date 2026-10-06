# BOOTSTRAP.md — START HERE (for any AI)

You are inside a project template. The human will give you a **problem statement (PS)**.
Your job in this FIRST session is to **configure the brain for that PS — NOT to write app code.**

## Session rules
- Do not write app code. Do not scan the whole repo. Only touch files inside `brain/`.
- Ask all your questions in ONE message (max 4). Don't ask what the user already told you.
- If the user gives no answer, use the defaults in brackets and say so.

## Steps (in order)

**0. Ask (one message, skip what's already known)**
- Is pre-written code / boilerplate allowed in this event? [assume NO: docs only until told]
- Event duration or deadline, team size, who knows what? [assume 24h, 3–4 people]
- Judging criteria and deliverable (app / model / deck / video)? [assume demo + pitch]

**1. Decode** — Run `brain/PS_Decoder.md` on the PS. Write the answers into that file.

**2. Options** — Give 3 solution options scored on wow / feasibility / data. Recommend one.
Wait for the user's pick (unless they said "just go").

**3. PRD** — Fill `brain/PRD.md`. MVP = 3 must-haves max. Include a cut list.

**4. Architecture** — Tailor `brain/Architecture.md`: keep the default stack unless the PS demands
otherwise. If the PS is not data/ML, use PS_Decoder section 8 (web app + workflow + one smart feature).
Update folders, API contract, data flow for THIS project.

**5. Phases** — Rewrite `brain/Phases.md`: rescale the times to the real duration, make tasks specific
to this PS. Feature freeze at 75% of total time.

**6. Design** — Tailor `brain/Design.md` to the domain (see table below). Keep contrast + chart rules.

**7. Rules** — In `brain/Rules.md`, add any extra libraries this domain needs under a heading
"Added for this project". Never delete existing rules.

**8. Memory** — Overwrite `brain/Memory.md`: Status: CONFIGURED, project name, Phase 0, next 3 tasks,
key decisions.

**9. Report and STOP** — Show a summary (max 10 lines): what changed in each file, open questions.
End with: "Ready for Phase 0 — go?" Then wait.

## Domain hints (starting points, not laws)
| Domain | Vibe / palette | Likely data + model ideas |
|---|---|---|
| Health | calm blue/teal, white space | vitals, risk scores, triage |
| Agriculture | green/earth tones | weather, crop prices, yield forecast |
| Finance | dark navy + green/red | ticks, fraud/anomaly, risk |
| Energy / Smart city | dark, cyan accents, maps | load forecast, traffic, AQI |
| Education | warm, friendly, light | engagement, dropout risk, recommendations |
| Industry / IoT | dark, amber alerts | sensor streams, predictive maintenance |
| Not data-related | pick from PS | web app + workflow + one smart feature |

## After bootstrap
Work normally: one phase at a time, small diffs, run it, commit it, update `Memory.md`.
See `brain/instruction.md` for session prompts.

## Reuse
This brain stays in EVERY project made from the template. If you learn something that would help next
time (a better prompt, a rule that saved you), add it to the master `brain-template` repo, not just the project copy.
