# Research — Evidence Layer

The Steam review corpora behind the game's design. **Evidence only: never edit the game design
from here.**

| Game | Analysis | Raw data | Reviews |
|---|---|---|---|
| A Game About Digging a Hole | `A_GAME_ABOUT_DIGGING_A_HOLE_REVIEW_ANALYSIS.md` | `research_data/a_game_about_digging_a_hole_reviews_raw.json` (6.7 MB) | 20,098 |
| Keep Digging | `KEEP_DIGGING_REVIEW_ANALYSIS.md` | `research_data/keep_digging_reviews_raw.json` (1.2 MB) | 3,266 |
| Meltopia | `MELTOPIA_REVIEW_ANALYSIS.md` | `research_data/meltopia_reviews_raw.json` (1 MB) | 1,722 |
| One Man's Trash | `ONE_MANS_TRASH_REVIEW_ANALYSIS.md` | `research_data/one_mans_trash_reviews_raw.json` (0.2 MB) | 330 |
| The Spotter: Dig or Die | `THE_SPOTTER_DIG_OR_DIE_REVIEW_ANALYSIS.md` | `research_data/the_spotter_dig_or_die_reviews_raw.json` (1 MB) | 1,859 |
| Digger: Galactic Treasures | `DIGGER_GALACTIC_TREASURES_REVIEW_ANALYSIS.md` | `research_data/digger_galactic_treasures_reviews_raw.json` (0.4 MB) | 729 |
| Hydroneer | `HYDRONEER_REVIEW_ANALYSIS.md` | `research_data/hydroneer_reviews_raw.json` (11 MB) | 28,474 |
| Ore Factory Squad | `ORE_FACTORY_SQUAD_REVIEW_ANALYSIS.md` | `research_data/ore_factory_squad_reviews_raw.json` (834 KB) | 1,791 |
| iDigging | `IDIGGING_REVIEW_ANALYSIS.md` | `research_data/idigging_reviews_raw.json` (414 KB) | 862 |

## Notes

- Review records carry only review-relevant fields, one review per line: `language`, `voted_up`, `votes_up`, `timestamp_created`, `playtime_at_review`, `received_for_free`, `primarily_steam_deck`, `review`, plus `developer_response` when the developer replied. All other scrape fields (IDs, profile/avatar, `app_release_date`, `hardware`, `reactions`, vote scores, purchase/refund/early-access flags) were dropped.
- Paths written inside the analyses (e.g. `research_data/...`) are relative to this folder.
- The game itself is in `../NEW_GAME_CONCEPT/CONCEPT/`; decisions in
  `../NEW_GAME_CONCEPT/DECISIONS.md`.
