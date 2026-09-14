# 09 — Endgame and Post-Game

> The ending is where the comparative set repeatedly shoots itself:
> `[AGADH]` — forced stealth, all tools disabled, **empty chest**, player killed, endless "should be
> optional" threads; `[SPOT]` — "All that time digging? Pointless", no NG+, no boss, a post-game
> tool with nothing to use it on; `[MELT]` — an ending some found nonsensical; `[OMT]` — abrupt payoff;
> `[KD]` — a button-and-cutscene ending that many found baffling.
> This game's rule: **the ending must make the player richer, not poorer.**

## 1. Finale design rules

1. **Tools stay online.** No sequence disables equipment. The finale is *the most powerful you ever
   feel*, not a powerless stealth segment. `[AGADH]` rule, absolute.
2. **The reward is real.** The final vault contains something the player actually wants: a unique
   tool module, the final tool skin, museum centerpiece, a story resolution, and access to all
   post-game modes. "Empty chest" is banned.
3. **No genre shift.** The final challenge uses digging, route planning, charges, traversal and
   reading the world — the verbs the player has mastered for 12 hours.
4. **No trolling retcon.** The story may have twists, but they add meaning, not negation. "It was a
   game show / you were a sucker / all digging was pointless" endings are forbidden unless written
   as an *optional* bonus scene, not the main resolution.
5. **Player agency:** the finale can be paused, left and returned to; no timed lock-in; no
   checkpoint starvation.
6. **Multiple ending expressions (3 variants), one canonical truth:** based on collection %, lore
   completeness and optional choices. All variants are satisfying; none punishes an unlucky player.
   (See `10_STORY_LORE_AND_ENDING.md`.)
7. **Ending sequence:** skippable, replayable from the menu, visible in a "memories" gallery.

## 2. What happens after the credits

Everything here ships at 1.0. `[SPOT]`'s empty post-game ("no New Game+, no boss, nothing to use
the reward on") is the anti-pattern.

| Mode | Unlock | Description |
|---|---|---|
| **Free Dig (surface reopened)** | After credits | The whole yard/layers regenerate with all tools; no story gates, full freedom |
| **New Game+** | After credits | New seed, gear carried, ascended variants, prestige cosmetics, in-game timer |
| **Endless** | After credits (demo: sample) | Seeded infinite descent with escalating ore values and contract generation |
| **Creative** | After credits | Unlimited money, flight, instant dig options, all placeables; build and share yard codes |
| **Challenge Dens** | 40% story + opt-in | Timed digs, no-suit runs, horror dens, "The Burrow" mole den; cosmetic rewards only |
| **Boss: The Hollow Warden** | Optional, endgame | A real, telegraphed, multi-phase optional boss for players who want a climax fight; fully avoidable, never gates the story; rewards a unique module + trophy |
| **Excavation Contracts** | Continuous | The endgame loop: bounded "clear this volume" and bounty jobs (`06` §6) |
| **Daily Seed** | Continuous | Fixed-seed shared runs with optional leaderboards; no FOMO rewards |

## 3. NG+ rules (built from `[KD]`'s praised reset)

- Keep: tools, modules, upgrades, cosmetics, museum, lore, currency at a reduced conversion rate.
- Reset: terrain and story triggers (with an option to turn quests off entirely in NG+).
- Add: "ascended" layer variants (remixed landmarks), a prestige cosmetic track, deeper contracts.
- Never: remove access to any mode, lock achievements (`[AGADH]` solved: achievements all work in
  run 1), or wipe the museum.
- The yard keeps a visual history: trophy room / before-after terrain scans per cycle.

## 4. Post-game collectibles and purpose

- **Trophy room:** displays finale variants, boss trophy, boss den souvenirs, daily-run medals.
- **Master Museum wing:** completion % track with tangible rewards (skill-free perks, hub guests).
- **Season-free content cadence:** post-launch updates add *new landmark families* and contracts,
  not power creep; old saves remain valid and complete-able (`20_LIVE_UPDATES_AND_DEV_PROCESS.md`).

## 5. The "use your reward" law

Every major reward must have at least one obvious use within 10 minutes of receiving it:

- Final drill module → the Free Dig / NG+ content opens immediately.
- Boss trophy → placed in the hub, visible forever.
- Museum completion → a new wing + a QoL perk + a cosmetic.
- `[SPOT]`'s "reward you can't actually use" is a named anti-pattern; every reward has a consumer
  designed at the same time as the reward.

## 6. Endgame pacing targets

| Metric | Target |
|---|---|
| Time from final story gate to credits | 20–40 min (one focused session) |
| Credits → first post-game activity | < 2 min (mode select is immediate) |
| Post-credits content available at 1.0 | ≥ 25 h of contracts/dailies/NG+/endless |
| Alt ending variants | 3 (collection 40%/75%/100% + optional choice) |
| Speedrun: story% and 100% | Both tracked in-game; dev-verified routes documented |

## 7. Ending test checklist

- [ ] Tools are never forcibly disabled in the finale (automated test: assert all tools usable).
- [ ] The finale's reward is validated by playtesters as "worth it" (survey ≥ 4/5).
- [ ] All three ending variants are reachable and distinct.
- [ ] Credits can be skipped and replayed.
- [ ] No post-credit mode invalidates achievements or deletes progress.
- [ ] A player can return to Free Dig from every post-game mode without losing anything.
