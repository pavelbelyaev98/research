# 02 — Core Loop and Progression

## 1. The minute-to-minute loop

```
LOOK (1–3 s)  →  DIG / VACUUM (10–30 s)  →  FEEL RICH (loot pop, sound)
      ↑                                              ↓
UPGRADE (10–30 s)  ←  SELL (5–15 s)  ←  RETURN when full / tired / curious
```

Every step must be satisfying **in isolation**, because reviewers described each separately:

- The **dig** must feel good with the starting tool, not only after upgrades `[AGADH]` "early
  clicking is painful" complaints. The starting shovel is satisfying-but-slow; every tier is
  faster, wider, or richer.
- The **loot pop** is core: ore vacuum-in, sparkle, a small sound, a rarity color. "Oddly
  satisfying" is the genre's top praise word `[OMT]` `[MELT]`.
- The **return** must never feel like a punishment. Traversal up equals traversal down (see
  `07_TRAVERSAL_AND_SOFT_PRESSURE.md`). "More time commuting than digging" is the #1 `[SPOT]`
  complaint and must be structurally impossible.

## 2. The session loop (30–90 minutes)

| Beat | Target | Rule |
|---|---|---|
| Plan | 1–2 min at surface: sell, bank, pick a goal ("reach 620 m", "find the third gear") | The map and quest log answer "what now?" in under 5 seconds |
| Descend | 2–5 min depending on fast travel | Fast travel never skips discovery: checkpoints unlock one-way until activated |
| Dig / explore | 20–50 min | At least one landmark or event every 60 s `[SPOT]` |
| Tension (optional) | 0–10 min | Only in Standard/Challenge, never mandatory |
| Return | 1–5 min | Soft pressure (heat/battery/weight) ends the trip *before* it becomes annoying; if the player ignores it, the soft penalty is losing nothing `[AGADH]` ore-loss is forbidden |
| Cash in | 2–5 min | Selling is instant and satisfying; "sell all" available from the start `[AGADH]` missing QoL |
| Upgrade | 1–3 min | Shop always has exactly one tempting purchase; visible tool change `[MELT]` |
| Optionally repeat | — | "One more run" comes from the player `[KD]` `[OMT]` `[SPOT]` |

## 3. Campaign arc

- **Depth scale:** 0–2,000 m across 7 layers (see `03_WORLD_AND_LEVEL_DESIGN.md`).
- **Tool tiers:** 6 tiers of the primary tool, each visually distinct, plus side tools.
- **Critical path:** 10–14 h. **100%:** 20–25 h. **Endgame:** 30+ h (see `09_ENDGAME_AND_POSTGAME.md`).
- **No dead zones:** from first sale to credits, the project manager's rule is *"at any moment the
  player is within 20–45 minutes of their next meaningful purchase."* This directly fixes
  `[AGADH]` (everything maxed by ~15% depth) and `[MELT]` ("ended with 100k and nowhere to spend").

### Pacing table (target; tune in playtests)

| Hour | Depth band | Primary tool | Purchases available | New thing introduced |
|---|---|---|---|---|
| 0.0–0.5 | 0–40 m | Rusty shovel | Backpack 2 | Hub, shop, map, basic ores |
| 0.5–1.5 | 40–120 m | Steel shovel | Shovel 2, battery 2 | First landmark (old well), first artifact |
| 1.5–3 | 120–260 m | Powered spade | Traversal (rope/kite), backpack 3 | Cave biome, first side tunnel gate |
| 3–5 | 260–480 m | Scoop drill | Drill radius 2, lamp, dynamite | Ruins biome, key/gear side quests |
| 5–7 | 480–760 m | Drill | Heat/cold gear 1, drill 3 | Flooded layer, first optional creature pool |
| 7–9.5 | 760–1,100 m | Auger | Traversal 3 (jetpack), drill 4 | Crystal layer, faction-1 story arc finale |
| 9.5–12 | 1,100–1,550 m | Core drill | Final tool tier, suit | Deep ruins, main story revelations |
| 12–14 | 1,550–2,000 m | Core drill+ | Post-max sinks (see `06`) | Finale, then post-game unlocks |

**Rule:** the final *power* upgrade is purchasable at ~85% depth, and post-max **sink** upgrades
(cosmetic, utility, museum, challenge keys) remain forever. The player must never sit on money with
nothing to buy `[AGADH]` `[MELT]` `[OMT]`.

## 4. Anti-straight-down design

`[KD]` died by this: the optimal strategy was to ignore the game and dig straight down in under an
hour; the developers literally patched notes admitting it. `[SPOT]` suffered a milder version.

Structural rules:

1. **Depth gates are lateral.** Every 150–250 m there is a "seal" (bedrock shelf, glyph door,
   collapsed vault) that cannot be passed by digging. Opening it requires an item, key or coded
   toggle found in side branches or landmarks of the current layer.
2. **Ore bands reward breadth.** Valuable ores spawn in horizontal veins offset from the main
   shaft; pure vertical digging yields ~40% of the income of a thorough player.
3. **Pressure is radial.** Fast travel checkpoints are off-shaft; the map reveals the layer when a
   checkpoint is activated, so explorers literally see more.
4. **Some things only exist sideways.** 100% completion, lore, fossils, cosmetics and side tools
   are all off-shaft. Straight-down can rush the critical path (it should still be *possible* for
   speedrunners) but misses 70% of the game — and the game says so honestly.
5. **Never nerf the dig.** Do not solve straight-down with friction (stamina drains, cooldowns,
   enemies). Solve it with content placement. Friction solutions generated the worst reviews in the
   set `[SPOT]` stamina/beer.

## 5. Difficulty and mastery

- Mastery comes from **efficiency and discovery**, not death: route planning, drill placement,
  vein recognition, checkpoint use, landmark hunts, speedrun tech.
- Optional challenge content: timed digs, "excavate 100% of a room" contracts, deep boss dens
  (opt-in, see `08`), daily seeded runs in Endless mode.
- No power is ever lost. No upgrade is ever refunded by the story. `[AGADH]` final sequence deleted
  all tools; `[MELT]` Tesla gun invalidated the flamethrower; `[OMT]` upgrades were invisible. All
  three are forbidden by pillar 2.

## 6. Progression systems (parallel, not serial)

| System | Feeds | Unlocks via | Never does |
|---|---|---|---|
| Tool tiers | Dig speed/radius | Money + layer materials | Replace a tool you own |
| Utility upgrades | Backpack, light, traversal, suit | Money + side quests | Reset |
| Museum/collection | Cosmetics, lore, passive QoL | Collectibles | Gate the story |
| Relationships (hub NPCs) | Discounts, side quests, flavor | Returning with gifts | Expire or punish |
| Knowledge (bestiary/lore) | Map annotations, danger warnings | Discovery | Require grind |

Everything in the "Unlocks via" column is achievable in any order the player wants, so builds never
dead-end, and respec is free (see `06_UPGRADES_AND_ECONOMY.md`).

## 7. What we deliberately do *not* put in the loop

- **No unskippable cutscenes mid-run.** Story beats are triggered at the hub or are short, quiet,
  skippable, and replayable.
- **No forced combat segments.** `[SPOT]` parkour/laser rooms and `[AGADH]` mole stealth are
  cautionary tales.
- **No randomly lost inventory.** `[AGADH]` battery-blackout ore loss and `[MELT]` freeze-loss are
  the loudest "unfair" complaints in the set.
- **No daily/login mechanics, no FOMO, no battle pass.**

## 8. Tuning targets (from review data)

| Metric | Target | Comparative evidence |
|---|---|---|
| First purchase | ≤ 5 min | `[AGADH]` hook lands immediately |
| Time to first "wow" landmark | ≤ 45 min | `[SPOT]` secrets are its best-loved feature |
| Upgrade felt-per-purchase | 100% (audible/visible) | `[OMT]` "+5% invisible" upgrade complaints |
| Max power reachable at | ~85% depth | `[AGADH]` maxed at ~15% |
| Money sinks available at credits | ≥ 8 meaningful | `[MELT]` "nothing to spend on" |
| Return trip frequency | ≤ every 25 min | `[SPOT]` "stop digging every 30 secs" |
| Session-enders chosen by player | > 90% | `[AGADH]` ending forced the stop |
