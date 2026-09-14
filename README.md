# Research Workspace — Map and Update Guide

This repository holds two things: **evidence** from digging-game reviews, and **the game** being
designed from it.

**Current status:** decision phase complete for v1; the concept set is written; the next step is a
research iteration (improve analyses → delta against decisions → new questions).

## The game

Start here: **`NEW_GAME_CONCEPT/CONCEPT/00_README.md`**

| Path | What it is |
|---|---|
| `NEW_GAME_CONCEPT/CONCEPT/` | The game design (16 files, from pitch to prototype plan) |
| `NEW_GAME_CONCEPT/DECISIONS.md` | The decision register — **single source of truth** for every confirmed choice |
| `NEW_GAME_CONCEPT/ITERATION_GUIDE.md` | How new research is turned into decision deltas safely |
| `NEW_GAME_CONCEPT/ARCHIVE/` | Historical process documents — never use as design context |

## The evidence

| Path | What it is |
|---|---|
| `RESEARCH/README.md` | Evidence-layer index and iteration instructions |
| `RESEARCH/A_GAME_ABOUT_DIGGING_A_HOLE_REVIEW_ANALYSIS.md` | Steam review analysis (20,098 reviews) |
| `RESEARCH/KEEP_DIGGING_REVIEW_ANALYSIS.md` | Steam review analysis (3,266 reviews) |
| `RESEARCH/MELTOPIA_REVIEW_ANALYSIS.md` | Steam review analysis (1,722 reviews) |
| `RESEARCH/ONE_MANS_TRASH_REVIEW_ANALYSIS.md` | Steam review analysis (330 reviews) |
| `RESEARCH/THE_SPOTTER_DIG_OR_DIE_REVIEW_ANALYSIS.md` | Steam review analysis (1,859 reviews) |
| `RESEARCH/research_data/` | Raw scraped review JSON for the five analyses |
| `PERFECT_DIGGING_GAME/` | Evidence-based synthesis + anti-pattern bible. **Reference only — not this game's design** |

## Workflow (short version)

1. **Research iteration:** improve the `RESEARCH/*_REVIEW_ANALYSIS.md` files from
   `RESEARCH/research_data/` (and any new data). Evidence layer only; do not touch the design here.
2. **Delta iteration:** compare the updated research against `DECISIONS.md` +
   `CONCEPT/13_OPEN_QUESTIONS.md` using the protocol in `ITERATION_GUIDE.md`. Output findings mapped
   to decision IDs, not redesigns.
3. **Design iteration:** changed decisions are logged in `DECISIONS.md`; affected `CONCEPT/`
   files are updated; new questions go to the developer.

**Golden rule:** if a concept file and the decision register disagree, the register wins.

---

## How to update as we go

### Change an existing decision

1. Find its ID in `NEW_GAME_CONCEPT/DECISIONS.md`.
2. Update the status (`REVISED`, `REJECTED`, …) and the decision text.
3. Add a dated row to the decision log: date, ID, change, reason, by.
4. Update the concept file(s) that mention it — mapping in `ITERATION_GUIDE.md` §4.
5. If it was listed as open, adjust or remove its row in `CONCEPT/13_OPEN_QUESTIONS.md`.

### Answer an open question

1. Move it into `DECISIONS.md` under the matching round with the developer's answer and a status.
   If it has no ID, allocate one (below).
2. Remove or update its row in `13_OPEN_QUESTIONS.md`.
3. Update the affected concept file(s) and log the change.

### Add a brand-new decision or question

- Continue the ID sequence; never reuse or renumber IDs:
  `Q31+` vision/scope · `W13+` world · `S13+` systems · `D14+` discoveries · `I17+` interface ·
  `F13+` art/feel · `P07+` design-relevant production outcomes · `A02+` policy.
- If it needs research, add a row to `13_OPEN_QUESTIONS.md` with options + a recommendation.

### Add research data or update an analysis

1. Drop raw data into `RESEARCH/research_data/`.
2. Update the matching `RESEARCH/*_REVIEW_ANALYSIS.md`, keeping its format.
3. Run the delta prompt from `NEW_GAME_CONCEPT/ITERATION_GUIDE.md` §6 and bring the mapped findings
   back for logging.

### Housekeeping rules

- **Never delete a decision.** Strike it through in the table and add a log entry.
- **Archive, don't delete,** process documents; only `CONCEPT/`, `DECISIONS.md` and
  `13_OPEN_QUESTIONS.md` are "live".
- **Commit in git after each decision round** so every change is revertable.
- If a file's purpose changes, update this README's map in the same commit.
- Keep numbers out of decisions (Rule 8) and production/marketing questions out of the process
  (Rule 5).
