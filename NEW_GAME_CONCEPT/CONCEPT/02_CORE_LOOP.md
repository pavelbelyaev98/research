# 02 — Core Loop

## 1. The minute loop

```
DIG  →  SIGNAL  →  INVESTIGATE  →  REVEAL  →  RECOGNIZE  →  COLLECT
 ↑                                                              ↓
UPGRADE  ←  SELL  ←  SURFACE  ←  (bag full / battery low / curiosity satisfied)
```

Rules for each beat:

| Beat | What happens | Rule |
|---|---|---|
| **Dig** | Hold-to-dig bites chunks of voxel ground; dust and material fall; the tool adapts automatically to what it's biting | Always satisfying from the starting shovel, never requires clicking speed |
| **Signal** | The detector reacts silently — the tool glows/shivers, a subtle edge-of-screen hint grows with proximity and general direction (exact presentation TBD, F07) | One target at a time; quiet intervals; never reveals value; can be ignored |
| **Investigate** | The player chooses to follow the hunch, dig sideways, or keep going down | Signals suggest, never prescribe; ignoring one is never wasted work |
| **Reveal** | Digging around an interesting object exposes it little by little; shape becomes readable before identity | Objects do not vanish when touched; the player decides when enough is exposed |
| **Recognize** | "Wait… is that a—" The object's silhouette resolves into identity | This moment is the game's core reward; objects must read at partial exposure |
| **Collect** | Quick pickups fly into the abstract bag; large finds get extracted later by cable | Small = instant, interesting = earned, large = event |
| **Return** | Climb your own hole; battery is the trip clock; return-power warning shows safe/risky/critical | No teleport; vertical return only; no return aids |
| **Sell** | Sell All machine gobbles everything ordinary; money is banked only here | One button; physical comedy; no deposit chore |
| **Upgrade** | Buy the next level of a track; visible change on the tool; practical benefit shown | Sequential, transparent, always something worth buying |

## 2. The session loop (30–60 min)

1. **Plan (1 min):** check the display outlines, the fat wallet, the next upgrade. Pick an intention:
   "reach the next zone", "chase that signal", "afford the drill".
2. **Dig (20–45 min):** descend, chase signals, explore sideways, discover, get greedy.
3. **Tension (optional):** the bag fills, the battery drops, the return warning turns orange.
4. **Decide:** keep going for one more thing, or leave with everything. This decision is the game's
   entire risk.
5. **Return and cash in (5–10 min):** climb, sell, recharge, upgrade, glance at the display wall.
6. **Repeat** because there is always exactly one thing to buy and one signal uninvestigated.

## 3. Campaign arc (3–5 hours, four zones)

| Phase | Zone | Experience |
|---|---|---|
| Hour 1 | **Recent fill** | Slow shovel, believable finds, first purchases, first hard pocket |
| Hours 2–3 | **Old sediment** | Real capability jumps, clusters, first "too modern for this depth" oddity |
| Hours 3–4 | **Deep clay/stone** | Tough ground, richer finds, lamps matter, deliberate impossibilities begin |
| Hours 4–5 | **Ancient constructed** | The final components, the impossible object, the ending; Continue Playing opens |

The last meaningful purchase should land near the end of the run so its power gets used (timing
prototype-tuned, L19).

## 4. Pacing rules (generation enforces these)

- A noteworthy discovery is guaranteed early (first ten minutes).
- Dry spells between noteworthy discoveries are bounded.
- Related objects cluster; unrelated major finds never clump.
- At most one major-scale discovery per zone.
- New object silhouettes keep appearing until the end; the late game is never "more dirt".
- Novelty is never dumped early: strong finds are distributed across all four zones.
- These rules validate a candidate layout before it is accepted; an accepted population persists and
  is never rerolled by a patch (W09, D12).

## 5. Anti-straight-down design

The reviewed failure: the optimal strategy becomes "ignore the game, dig straight down". This game
answers structurally, not with friction:

1. **Clusters and signals pull sideways** — the best discoveries are rarely on the main shaft.
2. **Depth influences category, never value** (L05): deep does not automatically mean richer, so a
   straight shaft skips content but does not out-earn an explorer.
3. **Hard pockets are optional and sideways** (W05b); the main descent is never hard-blocked.
4. **Components and uniques live off-shaft**, so the ending and the display reward exploration.
5. **No friction mechanics are used to stop rushing** — no stamina, no drains, no cooldowns, no
   enemies. The game respects the speedrunner and simply hides its best moments to the side.

## 6. The core test (if the prototype works, this happens repeatedly)

> "I should probably go back…"
> *a quiet cue suggests something nearby*
> "…fuck it, one more thing."
> Sideways. A weird shape. More exposure. Recognition. Collected.
> Bag almost full. Battery uncomfortable. Barely make it home.
> **SELL ALL.** Finally afford the ridiculous upgrade.
> *remember the hard wall at 14 m*
> …and immediately go back down.

## 7. Never in the loop

- No unskippable cutscenes mid-run (story is object-based; the ending is the only sequence).
- No forced combat, stealth, parkour or puzzles.
- No random inventory loss, no loot deletion from failure.
- No timed pressure, no daily systems, no FOMO.
- No walking through buildings or menus between digging and upgrading.
