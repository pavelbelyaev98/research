# 22 — Anti-Patterns (the "never ship this" list)

Each entry: the pattern, the evidence quote that earned it, and the rule that replaces it. If a
proposal matches an entry here, it is rejected unless a written exception is approved by the design
lead **and** the producer, with a mitigation plan.

## A. Tone and consent

| # | Anti-pattern | Evidence | Rule |
|---|---|---|---|
| A1 | Unadvertised horror in a cozy game | `[OMT]` "I was unaware that there would be jumpscare worms, as the game is not labelled as a horror type game" | Horror only via explicit opt-in; store page discloses (`08`) |
| A2 | Forced stealth / chase with tools disabled | `[AGADH]` "suddenly shifts genres to stealth horror… unpredictable and inconsistent" | No sequence ever disables tools or forces stealth (`09`) |
| A3 | Unskippable parkour/instadeath set pieces in a dig game | `[SPOT]` "mandatory parkour with clanky controls and instadeath pits" | Optional challenge dens only; tells and counters always (`08`) |
| A4 | Horror/parkour on the critical path | `[SPOT]` "You cant evade those parts, since they are built into the main quests" | Quest graph audit: zero horror nodes on critical path (`08`) |
| A5 | Content toggle that doesn't actually remove content | `[SPOT]` "I'm forced to enable it for the soil-softening function"; opening scene remains | Toggles cover 100% of the content, verified by content audit (`13` `14`) |
| A6 | Ending that negates the player's effort | `[SPOT]` "All that time digging? Pointless"; `[AGADH]` "one in a long line of suckers" | Twists re-contextualize, never negate; three warm endings (`10`) |

## B. Gameplay and progression

| # | Anti-pattern | Evidence | Rule |
|---|---|---|---|
| B1 | Tool that invalidates prior investment | `[MELT]` "a new tool which completely invalidates your progress… like starting from the beginning" | Parallel tools; nothing replaced (`04`) |
| B2 | Invisible stat-only upgrades | `[OMT]` "upgrades that have invisible effects (+5% range)" | Every upgrade visible/audible within 1 s (`04` `06`) |
| B3 | Economy dead-end: maxed everything early | `[AGADH]` "max out everything before the hole is even 15% of the way"; `[MELT]` "100k nowhere to spend" | Max power at 85% depth; eternal sinks (`06`) |
| B4 | Arbirary irreversible build choices | `[SPOT]` "to try new turret I have to start completely over" | Free instant respec; no permanent branches (`06`) |
| B5 | Straight-down trivializes the game | `[KD]` "It's too easy to clear by digging straight down" (devs' own patch notes) | Lateral gates, offset veins, landmark rewards (`03`) |
| B6 | Grind wall before the finale | `[SPOT]` "told me I need to buy the expensive tier upgrade two times over" | Finale readiness check; requirements visible early (`06`) |
| B7 | Time-friction mechanics that stop digging | `[SPOT]` "remove the beer drinking crap… I want to dig, not stop every 30 secs"; `[AGADH]` battery blackout | Soft pressure sets rhythm, never blocks; loot never lost (`07`) |
| B8 | Rope-only / one-way traversal | `[OMT]` "single rope in the center, no jetpack… pain to rebuild walkways" | Four independent ways up; recall always (`07`) |
| B9 | RNG replacing deterministic progression | `[KD]` "2.0 introduces blueprints… RNG involved… can no longer purchase tools past Copper" | Shops and deterministic rewards; RNG is cosmetic only (`04` `05`) |
| B10 | Inventory that destroys items | `[OMT]` rare slots; `[AGADH]` blackout loss; `[MELT]` freeze-drop | Overflow ships to storage; nothing is ever deleted (`05`) |
| B11 | Health/ammo scarcity forcing AFK or shopping friction | `[OMT]` "going AFK for 5 minutes to let my health slowly refill" | Buyable/craftable rations; checkpoint rest (`07`) |
| B12 | Unminable/decoy obstacles | `[SPOT]` "unbreakable obstacles" | Every wall has a tool, route or clear tell (`03` §8) |

## C. Technical

| # | Anti-pattern | Evidence | Rule |
|---|---|---|---|
| C1 | Single-digit FPS / heavy optimization debt | `[KD]` "Solid 11fps on a 3070", `[MELT]` "heats my PC to 90 degrees" | Hard perf budget + nightly soak (`15`) |
| C2 | Shader compilation on every launch | `[KD]` "shaders compiling… every game load" | Warm-up once + async precache (`15`) |
| C3 | Save freeze / lost saves / no cloud / one slot | `[MELT]` "autosave freezes the ENTIRE game for 5 seconds"; `[SPOT]` "Saves disappeared?!" | Atomic async saves, backups, cloud, 5+ slots (`15`) |
| C4 | Terrain not saved | `[AGADH]` "saving only saves your tool upgrades not the hole you've dug" | Full world delta persistence (`15`) |
| C5 | Crash on core actions | `[AGADH]` "'Fatal Error' on selling ore, recharging, buying" | P0 test sweep; crash-free operations (`15`) |
| C6 | Frame-rate-dependent simulation | `[SPOT]` "Drill speed changes with fps" | Fixed timestep; automated regression test (`15`) |
| C7 | FPS decay over a session | `[KD]` "the longer I played, the more my frames dropped"; `[OMT]` "FPS drops over time" | 3-hour soak, < 5% drift (`15`) |
| C8 | No autosave | `[OMT]` "No autosave; if the game crashes, the save is lost" | Autosave default with crash recovery (`15`) |
| C9 | Settings that don't persist | `[KD]`; `[SPOT]` "doesn't remember my setting… every restart" | Immediate persist + cloud (`13`) |
| C10 | Floating voxel debris | `[AGADH]` "1x1-pixel particles that will break your legs" | Flood-fill cleanup; no collidable particles (`04` §5) |

## D. Interface and body

| # | Anti-pattern | Evidence | Rule |
|---|---|---|---|
| D1 | Click-per-dig / no hold-to-dig | `[AGADH]` "I'm not gonna mash m1 over hours"; `[MELT]` "might give yourself RSI" | Hold-to-dig + auto-dig assist (`11`) |
| D2 | No key rebinding / fixed keys / layout lockout | `[SPOT]` "left-handed player on fixed keybinds"; `[AGADH]` AZERTY | 100% rebinding, left-handed mode (`11`) |
| D3 | No FOV / no motion-comfort settings | `[AGADH]` vertigo; `[MELT]` "no settings to reduce motion sickness… unplayable" | Full motion suite defaults safe (`13` `14`) |
| D4 | Forced blur/bloom/darkness | `[KD]` "extremely blurry… unplayable"; `[KD]` "extreme darkness" | Post-processing off by default; player light sufficient (`17`) |
| D5 | Missing map / identical corridors | `[MELT]` "no map… all corridors identical"; `[SPOT]` "not very clear… feel lost" | Map system at 1.0; distinct layer palettes (`03` `12`) |
| D6 | ESC doesn't close menus | `[KD]` "ESC button should close the menu" | Menu UX hard rules (`12`) |
| D7 | Repeated nag popups | `[SPOT]` toilet-humor prompt every launch | Ask once, store answer (`12`) |
| D8 | Color-only information | genre-wide; colorblind audits rare | Shape + icon + label redundancy (`14`) |

## E. Business, content and community

| # | Anti-pattern | Evidence | Rule |
|---|---|---|---|
| E1 | Paid demo / critical path under the refund window | `[AGADH]` "feels like a paid demo"; `[OMT]` "barely longer than the demo" | 10–14 h critical path minimum; demo carries over (`19`) |
| E2 | Early Access vibes at full price | `[SPOT]` "major Early Access vibes, while it is not"; `[MELT]` "should've been released as Early Access" | Ship complete or be honest in EA (`19`) |
| E3 | DLC before the base is finished | `[MELT]` DLC/Soundtrack while empty rooms remained | Cosmetic/supporter only; free content updates (`19`) |
| E4 | Asset flip / AI slop | `[KD]` "blatant ripoff"; `[MELT]` "I suspect AI textures, music, and/or writing" | Original art, no AI assets, cohesion gate (`17`) |
| E5 | NG+-locked or broken achievements | `[AGADH]` "locking achievements behind finishing the game… INCREDIBLY scummy"; `[MELT]` "45/46 forever" | One-run deterministic achievements; retroactive grants (`18`) |
| E6 | Hostile achievements | `[SPOT]` false "no cheating", bugged collectathons, "clear all dirt" | Fairness rules (`18`) |
| E7 | Host-only co-op content | `[KD]` "only the host can pick up dinosaur bones"; achievements | Parity rules (`16`) |
| E8 | Stealth balance changes that hurt existing saves | `[MELT]` "devs rebalanced something… cant even reach the end of a tunnel" | No-stealth-change rule; opt-in balance (`20`) |
| E9 | Updates that invalidate saves | `[SPOT]` 1.1 "developers strongly recommend starting a new game" | No save-breaking updates, ever (`20`) |
| E10 | Post-launch abandonment | `[AGADH]` "It's been over a year and still nothing has come" | 12-month roadmap with free updates (`20`) |
| E11 | Bought/fake review culture | `[KD]` "the Very Positive rating is fake and bought" accusations | Real demo, no review manipulation, transparent comms (`19` `20`) |

## F. One-line summary card

> No unadvertised scares. No disabled tools. No invisible upgrades. No dead economy. No lost saves.
> No lost loot. No unmapped mazes. No mashing. No fixed keys. No forced blur. No stolen choices.
> No empty endings. No abandonware. **Just a very good hole.**
