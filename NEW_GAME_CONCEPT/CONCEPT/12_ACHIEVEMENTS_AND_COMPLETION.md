# 12 — Achievements and Completion

## 1. Philosophy

Achievements are a fair record of play, not a second job (I15, P06). The reference set's failures:
achievements locked behind New Game+, buggy counters, RNG speedruns, host-only unlocks, grindy
collectathons and false "no cheating" detectors. None of that exists here.

## 2. The rules

1. **5–10 achievements total.**
2. All obtainable in a **single playthrough**; no NG+ requirement.
3. **Deterministic:** no RNG, no seeds, no luck-based unlocks.
4. **Mode/assist independent:** auto-dig, toggle dig, muted audio and colorblind palettes never block
 an achievement.
5. **Retroactive and durable:** discovery and progression records persist; loading an old save
 re-grants anything already earned.
6. **No false detectors:** the game never accuses the player of cheating.
7. **No grinds:** nothing requires clearing every voxel or repeating unfun loops.
8. **No host-only or online-required achievements** (the game is single-player).
9. **Visible-state eligibility only.** No hidden cheat/mod flag can silently lock achievements. If a
   save becomes ineligible (e.g., debug), the game says so in plain language and points to a clean-save
   path; saves that never cheated are never punished.
10. **No in-game task lists:** achievements are never surfaced as HUD checkboxes or to-do chores; they
    live on Steam and read as a record of play, not assignments (developer playthrough).

## 3. Candidate set (to be finalized with content)

| # | Type | Example |
|---|---|---|
| 1 | Story | Reach and expose the final impossible object |
| 2 | Depth | Reach the deepest zone for the first time |
| 3 | Tool | Fully upgrade the machine's Tool track |
| 4 | Discovery | Fill the first display row / collect the first unique |
| 5 | Discovery | Find a complete fossil or micro-scene set |
| 6 | Collection | Fill a meaningful fraction of the display outlines |
| 7 | Fun | Perform a natural absurd action (e.g., extract a car, or something equally silly) |
| 8 | Completion | All tracks maxed |
| 9 | Completion | All display outlines filled |
| 10 | Mystery | Discover all three mystery-escalation finds |

Final list should stay in the 5–10 range and prefer "things players naturally want to do anyway".

## 4. Completion definition (P05)

| State | Requirement |
|---|---|
| **Beaten** | Final object found and components assembled; credits shown |
| **100%** | Display outlines complete + all upgrade tracks maxed + all zones explored (stat view) + achievement set complete |
| **Never required** | 100% terrain removal, perfectly straight shafts, retaining every temporary item |

Achievements must remain attainable after the ending on the same save (S12): missed finds are still
findable, remaining upgrades purchasable, the display completable.

## 5. Tracked stats (for the completion screen)

- Depth records, time played, purchases, finds by tier, uniques collected, clusters discovered,
 fossils recovered, large objects extracted, mystery finds found, recoveries used, seeds played.
- Stats are informational; only the 100% definition uses a subset.

## 6. Implementation requirements

- Profile-level stat store written with the save; achievements derived from stats and re-granted on
 load when conditions are met.
- Offline earning queues locally and syncs to Steam when available.
- A clean-save 100% verification run must pass before release, including with assists enabled
 (`14_PROTOTYPE_PLAN.md` lists this as a release gate).
