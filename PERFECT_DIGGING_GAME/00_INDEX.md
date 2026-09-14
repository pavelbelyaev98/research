# The Perfect Digging Game — Design Bible

A data-driven design for a first-person digging game that **keeps every strength and fixes every
recurring mistake** observed across the five Steam review corpora in this repository.

This is not a clone of any one game. It is a synthesis: every design rule in these documents traces
back to something real players wrote in reviews, with the source recorded inline.

## Sources

| Tag | Game | Reviews analyzed | Rating | Price | Typical completion |
|---|---|---|---|---|---|
| `[AGADH]` | A Game About Digging a Hole | 20,098 | 89% Very Positive | $4.99 | 1–2 h |
| `[KD]` | Keep Digging | 3,266 | 80% Mostly Positive | $6.99 | 0.5–7 h |
| `[MELT]` | Meltopia | 1,722 | 86% Very Positive | $6.99 | 5–8 h |
| `[OMT]` | One Man's Trash | 330 | 86% Very Positive | $5–7 | 2.5–6 h |
| `[SPOT]` | The Spotter: Dig or Die | 1,859 | 85% Very Positive | $12.99 | 6–12 h |

Full analyses live one level up (`*_REVIEW_ANALYSIS.md` in the repository root).

## The North Star

> **A cozy, honest, hand-crafted dig-'em-up that respects your time, your hands, your eyes and your
> hardware — and never betrays the fantasy of "I am digging a hole" for a cheap twist.**

### The seven pillars

1. **The single verb is sacred.** Digging stays satisfying, readable and physically pleasant from
   minute one to the credits. No forced genre swaps, no mid-game tool that invalidates your build,
   no un-asked-for horror. Everything else is optional. `[AGADH]` `[MELT]` `[OMT]` `[SPOT]`
2. **Every hour has a purpose.** No money dead-ends, no maxed upgrades at 40% depth, no 5-hour
   critical path sold as a 15-hour game. Content and economy stretch alongside the player.
   `[AGADH]` `[MELT]` `[OMT]`
3. **Progress, don't replace.** Upgrades visibly change your tools; new tools deepen the fantasy
   instead of resetting it. Nothing you bought becomes worthless. `[MELT]` `[OMT]` `[SPOT]`
4. **Cozy by default, danger by consent.** No death spirals, no unadvertised monsters, no forced
   stealth, no horror without an explicit opt-in. `[AGADH]` `[OMT]` `[SPOT]`
5. **Runs anywhere, saves everything.** Frame-rate-independent simulation, stable performance,
   frozen-free autosaves, terrain persisted, Steam Cloud, crash-safe writes. `[KD]` `[MELT]` `[SPOT]`
6. **Your body matters.** Hold-to-dig, full rebinding, FOV/motion controls, no RSI traps, no
   motion-sick defaults, complete accessibility. `[AGADH]` `[KD]` `[MELT]` `[OMT]` `[SPOT]`
7. **The ending pays the bill.** The finale rewards the loop, never erases it. Endgame, not a wall:
   NG+, endless, creative and challenge modes ship with 1.0. `[AGADH]` `[SPOT]`

## File map

Read in order for the full argument, or jump to a topic.

### 1. Foundation
| File | Contents |
|---|---|
| `01_GENERAL_IDEA.md` | Pitch, fantasy, audience, tone, platform, pillars, what the game is NOT |
| `02_CORE_LOOP_AND_PROGRESSION.md` | Minute-to-minute loop, session shape, campaign arc, pacing math |
| `03_WORLD_AND_LEVEL_DESIGN.md` | Map architecture, biomes, handcrafted vs procedural, why straight-down must not win |

### 2. Content & systems
| File | Contents |
|---|---|
| `04_TOOLS.md` | Every tool: dig, vacuum/terraform, traversal, light, support — full specs |
| `05_ITEMS_AND_RESOURCES.md` | Ore tiers, consumables, collectibles, placeables, artifacts, fossils |
| `06_UPGRADES_AND_ECONOMY.md` | Upgrade trees, sinks, no dead-ends, pricing math, respec, NG+ economy |
| `07_TRAVERSAL_AND_SOFT_PRESSURE.md` | Battery/heat/weight as soft pressure, fall damage policy, fast travel |
| `08_HAZARDS_ENEMIES_AND_HORROR.md` | Opt-in danger model, day/night, enemies, horror policy and content warnings |
| `09_ENDGAME_AND_POSTGAME.md` | Finale design, NG+, endless, creative, boss (optional), post-game rewards |
| `10_STORY_LORE_AND_ENDING.md` | Narrative through artifacts/notes, environmental storytelling, ending rules |

### 3. Interface & body
| File | Contents |
|---|---|
| `11_CONTROLS_AND_INPUT.md` | Hold-to-dig, full rebinding, left-handed, controller, Steam Deck |
| `12_UI_AND_UX.md` | Map/scan, quest clarity, menus, tutorial, HUD, settings persistence |
| `13_SETTINGS.md` | Every option that must exist at 1.0, with defaults |
| `14_ACCESSIBILITY.md` | Motion, motor, vision, hearing, cognitive, content toggles, one-hand play |

### 4. Technology & production
| File | Contents |
|---|---|
| `15_PERFORMANCE_SAVES_AND_TECH.md` | FPS budget, frame-rate independence, save architecture, cloud, crash safety |
| `16_MULTIPLAYER_AND_COOP.md` | Co-op design (shared progress, host parity, drop-in, sync budget) |
| `17_AUDIO_VISUALS_AND_ART.md` | Art direction rules, asset policy (no slop), readability, music/ambience |
| `18_ACHIEVEMENTS.md` | Fair achievement rules, no NG+ locks, no RNG, no false "no cheating" |
| `19_PRICE_RELEASE_AND_DEMO.md` | Price-to-content math, demo policy, EA policy, DLC policy |
| `20_LIVE_UPDATES_AND_DEV_PROCESS.md` | Patch discipline, save compatibility, communication, community |

### 5. Synthesis
| File | Contents |
|---|---|
| `21_LESSONS_MATRIX.md` | Take/avoid table for all five games, plus theme frequency data |
| `22_ANTI_PATTERNS.md` | The "never ship this" list, each with the review quote that earned it |
| `23_SCOPE_ROADMAP_AND_QA.md` | MVP scope, milestones, budget/team shape, QA gate checklist |

## How to use this document set

- **Designers**: `01`–`10` are the game. `11`–`14` are contract-level requirements, not polish.
- **Engineers**: `13` `15` `16` `23` define hard technical requirements (frame-rate independence,
  save architecture, performance budget).
- **Producers**: `19` `20` `23` define price, scope and release discipline.
- **Anyone arguing about a feature**: find the relevant file; if a proposal contradicts a pillar or
  a rule in `22_ANTI_PATTERNS.md`, it needs a written exception, not a vibe.
