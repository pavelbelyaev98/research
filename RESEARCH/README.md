# Research — Evidence Layer

The five Steam review corpora behind the game's design. **Evidence only: never edit the game design
from here.**

| Game | Analysis | Raw data | Reviews |
|---|---|---|---|
| A Game About Digging a Hole | `A_GAME_ABOUT_DIGGING_A_HOLE_REVIEW_ANALYSIS.md` | `research_data/a_game_about_digging_a_hole_reviews_raw.json` (6.7 MB) | 20,098 |
| Keep Digging | `KEEP_DIGGING_REVIEW_ANALYSIS.md` | `research_data/keep_digging_reviews_raw.json` (1.2 MB) | 3,266 |
| Meltopia | `MELTOPIA_REVIEW_ANALYSIS.md` | `research_data/meltopia_reviews_raw.json` (1 MB) | 1,722 |
| One Man's Trash | `ONE_MANS_TRASH_REVIEW_ANALYSIS.md` | `research_data/one_mans_trash_reviews_raw.json` (0.2 MB) | 330 |
| The Spotter: Dig or Die | `THE_SPOTTER_DIG_OR_DIE_REVIEW_ANALYSIS.md` | `research_data/the_spotter_dig_or_die_reviews_raw.json` (1 MB) | 1,859 |

## How to iterate (Stage 1)

1. Open the raw JSON for a game in `research_data/`.
2. Update its `*_REVIEW_ANALYSIS.md`, keeping the existing format: summary, numbers, quantified theme
   tables, praise/criticism sections, verbatim quotes with language/playtime/votes, caveats.
3. Do not touch `../NEW_GAME_CONCEPT/` in this stage.
4. When the analyses are updated, run the delta protocol (Stage 2) in
   `../NEW_GAME_CONCEPT/ITERATION_GUIDE.md`.

## Notes

- Review records carry only review-relevant fields, one review per line: `language`, `voted_up`, `votes_up`, `timestamp_created`, `playtime_at_review`, `received_for_free`, `primarily_steam_deck`, `review`, plus `developer_response` when the developer replied. All other scrape fields (IDs, profile/avatar, `app_release_date`, `hardware`, `reactions`, vote scores, purchase/refund/early-access flags) were dropped.
- Paths written inside the analyses (e.g. `research_data/...`) are relative to this folder.
- The game itself is in `../NEW_GAME_CONCEPT/CONCEPT/`; decisions in
  `../NEW_GAME_CONCEPT/DECISIONS.md`.

## Prompt: update one analysis from its raw data (Stage 1)

Paste this into a fresh chat, replacing `<JSON>` and `<ANALYSIS>`:

```
You are updating one research document in this repository. Evidence layer only - do not touch the
game design.

Files:
- Raw data: RESEARCH/research_data/<JSON>
- Target document: RESEARCH/<ANALYSIS>.md
- Rules/context: RESEARCH/README.md (read it first)

Goal: bring the target markdown up to date with the raw JSON - correct anything inaccurate, add
important themes that are missing, add minor details and quotes worth keeping, and improve clarity
and organization. Do not rewrite from scratch; do not remove content unless it is wrong, redundant
or superseded.

Process:
1. Read RESEARCH/README.md for the rules.
2. Inventory the JSON: total reviews, positive/negative counts, languages, date range, fields and
   data quirks. Report the numbers.
3. Read the current markdown fully and list every checkable factual claim (counts, percentages,
   medians, totals, quotes, language distributions, dated statements).
4. Verify each claim against the JSON. For every mismatch state: existing claim -> actual value ->
   how it was computed.
5. Find gaps: themes, quotes or player behaviors in the data the document misses. Rank them
   important / minor / skip.
6. Present a change plan as a list and wait for my approval before editing.
7. After approval, update the file in place, preserving its structure: header table, method/corpus
   verification, TL;DR, numbers, praise, criticism, divergent opinions, who should buy, caveats,
   spoiler sections.
8. Add a short "Revision notes (date)" section at the end listing what changed and why.

Hard rules:
- Never invent quotes, numbers or themes. Quotes are verbatim from the JSON; translations are marked
  "(translated)".
- Preserve attribution: language, playtime at review, sentiment, upvote count.
- Keep theme/keyword counts labeled approximate, as the existing docs do.
- Do not touch NEW_GAME_CONCEPT/.
- If the JSON is too large for one pass, compute aggregates with small scripts; never sample silently
  - if you sample, state exactly how and why.
- If a change is uncertain, list it as an open question instead of applying it.

Deliverable: the updated markdown file plus a concise change report (max 30 lines) for review.
```
