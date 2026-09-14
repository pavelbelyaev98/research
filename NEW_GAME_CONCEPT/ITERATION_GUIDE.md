# Iteration Guide — how to improve this design with new research

This repo has two layers: **evidence** (review analyses + raw data) and **the game** (decisions +
concept). This guide defines how to run a research iteration without contaminating the design.

## 1. Folder roles

| Path | Role | Feed to AI? |
|---|---|---|
| `RESEARCH/research_data/*.json` | Raw scraped review data | Only for analysis passes |
| `RESEARCH/*_REVIEW_ANALYSIS.md` | Per-game research documents being iterated on | Yes, as evidence |
| `NEW_GAME_CONCEPT/DECISIONS.md` | The decision register — single source of truth | **Always** |
| `NEW_GAME_CONCEPT/CONCEPT/` | The game design | For updates only, not as research input |
| `NEW_GAME_CONCEPT/CONCEPT/13_OPEN_QUESTIONS.md` | Every intentionally undecided item | **Always** |

## 2. The two-stage iteration

### Stage 1 — Improve the research documents
1. Take `RESEARCH/research_data/*.json` (and any new data) and iterate on the matching
   `RESEARCH/*_REVIEW_ANALYSIS.md`.
2. Keep the analysis format: quantified themes, verbatim quotes, sentiment, caveats.
3. Do not touch the game design in this stage.

### Stage 2 — Delta against the decisions
Feed a fresh AI session exactly this pack:

- `NEW_GAME_CONCEPT/DECISIONS.md`
- `NEW_GAME_CONCEPT/CONCEPT/13_OPEN_QUESTIONS.md`
- the updated/new research section(s)

And request this output format:

> For every research finding relevant to a decision in the register, output a row:
> **Finding | Affected decision ID(s) | CONFIRMS / CONTRADICTS / ADDS NUANCE | Confidence | New question (only if it contradicts or adds nuance)**
> Do not redesign systems, do not propose numbers, do not treat the reference bible as this
> game's spec.

### Stage 3 — Bring the delta back
The design session (this one) then:

1. Logs changed decisions in `DECISIONS.md` with date + reason (old entries struck through, never
   deleted).
2. Updates the affected concept files (mapping below).
3. Moves answered questions out of `13_OPEN_QUESTIONS.md`.
4. Marks decisions that new evidence contradicts with a flag — evidence never silently overrides the
   developer's choice.

## 3. Decision ID scheme

| Prefix | Domain | Prefix | Domain |
|---|---|---|---|
| `Q` | Vision, identity, scope, business | `I` | Interface, controls, accessibility |
| `W` | World, terrain, site | `F` | Art, audio, feel |
| `S` | Systems, progression, economy | `P` | Process/production outcomes that are design-relevant |
| `D` | Discoveries, content | `A` | Asset policy |
| `C` | Confirmed concept proposals | `L` | (retired — legacy claim tracker, archived) |

## 4. Update map (decision topic → concept file)

| Topic | File |
|---|---|
| Fantasy, tone, humor, mystery framing | `CONCEPT/01_FANTASY_AND_TONE.md`, `11_ENDING_AND_MYSTERY.md` |
| Loop, pacing, sessions | `CONCEPT/02_CORE_LOOP.md` |
| Site, zones, materials, lighting, randomization | `CONCEPT/03_WORLD_AND_SITE.md` |
| Tool, adaptation, jetpack, crouch, C4 | `CONCEPT/04_TOOL_AND_MOVEMENT.md` |
| Finds, detector, clusters, large finds | `CONCEPT/05_DISCOVERIES.md` |
| Tracks, economy, fuel, capacity, recovery | `CONCEPT/06_PROGRESSION_AND_ECONOMY.md` |
| Surface yard, stations, display | `CONCEPT/07_SURFACE_HUB_AND_DISPLAY.md` |
| HUD, inventory UI, pause, controls, photo, saves | `CONCEPT/08_INTERFACE_AND_CONTROLS.md` |
| Visuals, palettes, dig feel, material feel, audio, FX | `CONCEPT/09_FEEL_ART_AND_AUDIO.md` |
| Motion/motor/vision/hearing/cognitive access | `CONCEPT/10_ACCESSIBILITY_AND_COMFORT.md` |
| Endgame, components, Continue Playing | `CONCEPT/11_ENDING_AND_MYSTERY.md` |
| Achievements, completion | `CONCEPT/12_ACHIEVEMENTS_AND_COMPLETION.md` |
| Open items | `CONCEPT/13_OPEN_QUESTIONS.md` |
| Prototype experiments | `CONCEPT/14_PROTOTYPE_PLAN.md` |
| Never-do list | `CONCEPT/15_ANTI_PATTERNS.md` |

## 5. Guardrails

- **The developer decides.** Research and AI output are evidence; they never overwrite a decision.
- **No numbers in design debates.** Values are tuned in the prototype (Rule 8).
- **No production/marketing questions.** Those are out of scope (Rule 5).
- **One source of truth.** If a concept file contradicts `DECISIONS.md`, the register wins.
- **No context dumping.** Never feed the whole concept set or raw question banks into a research
  session; use the context pack in §2.

## 6. Ready-to-paste prompt for the next research session

```
You are doing a research delta for a first-person digging game. Do not redesign anything.

Context:
- Decision register: [attach NEW_GAME_CONCEPT/DECISIONS.md]
- Open design items: [attach NEW_GAME_CONCEPT/CONCEPT/13_OPEN_QUESTIONS.md]
- New/updated research: [attach the updated analysis or new data summary]

Task:
For every finding relevant to a decision ID, output one row:
Finding | Affected ID(s) | CONFIRMS / CONTRADICTS / ADDS NUANCE | Confidence | New question (only if
contradicts or adds nuance).
Rules: cite evidence; no new systems; no numbers; do not treat the reference bible as this game's
spec; keep total output under N rows, ordered by importance.
```
