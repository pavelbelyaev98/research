# Research — Evidence Layer

The five Steam review corpora behind the game's design. **Evidence only: never edit the game design
from here.**

| Game | Analysis | Raw data | Reviews |
|---|---|---|---|
| A Game About Digging a Hole | `A_GAME_ABOUT_DIGGING_A_HOLE_REVIEW_ANALYSIS.md` | `research_data/a_game_about_digging_a_hole_reviews_raw.json` (29 MB) | 20,098 |
| Keep Digging | `KEEP_DIGGING_REVIEW_ANALYSIS.md` | `research_data/keep_digging_reviews_raw.json` (4.9 MB) | 3,266 |
| Meltopia | `MELTOPIA_REVIEW_ANALYSIS.md` | `research_data/meltopia_reviews_raw.json` (3 MB) | 1,722 |
| One Man's Trash | `ONE_MANS_TRASH_REVIEW_ANALYSIS.md` | `research_data/one_mans_trash_reviews_raw.json` (0.5 MB) | 330 |
| The Spotter: Dig or Die | `THE_SPOTTER_DIG_OR_DIE_REVIEW_ANALYSIS.md` | `research_data/the_spotter_dig_or_die_reviews_raw.json` (3.1 MB) | 1,859 |

## How to iterate (Stage 1)

1. Open the raw JSON for a game in `research_data/`.
2. Update its `*_REVIEW_ANALYSIS.md`, keeping the existing format: summary, numbers, quantified theme
   tables, praise/criticism sections, verbatim quotes with language/playtime/votes, caveats.
3. Do not touch `../NEW_GAME_CONCEPT/` in this stage.
4. When the analyses are updated, run the delta protocol (Stage 2) in
   `../NEW_GAME_CONCEPT/ITERATION_GUIDE.md`.

## Notes

- Paths written inside the analyses (e.g. `research_data/...`) are relative to this folder.
- The evidence-based synthesis (a different, hypothetical game) lives in
  `../PERFECT_DIGGING_GAME/` — reference only, not this game's design.
- The game itself is in `../NEW_GAME_CONCEPT/CONCEPT/`; decisions in
  `../NEW_GAME_CONCEPT/DECISIONS.md`.
