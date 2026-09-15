# 15 — Anti-Patterns (never ship these)

Each entry is a specific failure observed in the reviewed digging-game corpora, and the rule that
forbids it here. If a proposal matches an entry, it is rejected unless the developer explicitly
overrides it in `../DECISIONS.md`.

## Progression and economy

| # | Never | Evidence | Rule here |
|---|---|---|---|
| 1 | Let players max everything halfway and make money pointless | "completely max out everything before the hole is even 15% of the way down" / "ended with 100k and nowhere to spend" | Tracks + late sinks + final purchase near the end (`06`) |
| 2 | Introduce a new tool that invalidates old upgrades | The Tesla gun: "completely invalidates your progress… like starting from the beginning" | One machine, shared upgrade track (`04`) |
| 3 | Sell invisible stat upgrades | "+5% range, +5% power… you don't feel the effect"; Ore Factory Squad's reviewers finished it feeling upgrades never increased their output | Every purchase visible/audible (`06`) |
| 4 | Gate progress behind RNG, blueprints, licenses or rare drops | "2.0 introduces blueprints… RNG… can no longer purchase tools past Copper"; Ore Factory Squad locked upgrades behind player levels and drew "upgrades locked behind levels are stupid" and "progression is broken" | Money-only, sequential, deterministic (`06`) |
| 5 | Make rare finds buy half the tree | Jackpots destroy pacing | Rare = several expeditions, never half the tree (`05`) |
| 6 | Force repeat trips or grinds for the finale | "40 to 60 more trips to the bottom" | Finale readiness is natural; no grind wall (`02`, `06`) |
| 7 | Irreversible build choices | "to try new turret I have to start completely over" | No permanent branches; all purchases additive (`06`) |
| 44 | Gate progression behind a minigame or non-digging activity | Hydroneer's King's quest demanded token crops, a 1.5-weight lobster and 600-crop soup deliveries — "quest grind fest" | The only gates are money and tool power; the dig is always the answer (`06` §1) |
| 47 | Ship an upgrade that is bigger but slower in the ground it replaces | Ore Factory Squad's jackhammer was faster per hit but had a smaller bite than the upgraded shovel — players called it "really useless", and its tool tiers read as "more or less the same" | Every new head/tier is measured in time-to-clear and never regresses; new behavior adds speed, access or control (`04`, `06`) |
| 48 | Add gambling, casino or betting mechanics | Developer playthrough: "Gambling in the game is a hard NO… cheap and bad"; One Man's Trash reviewers split — a funny diversion to some, "do not bet, kids" to others (75.7% return, a ~$3,000 loss over 16,000 spins) | No gambling; money sinks are explicit purchases with visible value (`06`, `07`) |
| 49 | Wall off depth to force in-area grinding | Developer playthrough: a hard blocker at roughly 20 m forced re-digging the same area; One Man's Trash reviewers also resented the ~$20,000 license gate | The only gates are money and tool power; depth is never artificially walled, and any capability gate is telegraphed before commitment (`06` §1, `03` §5) |

## Pressure and failure

| # | Never | Evidence | Rule here |
|---|---|---|---|
| 8 | Delete carried loot on failure | "want to do bad things to the creators"; freeze-loss | Recovery keeps everything; fee + debt only (`06`) |
| 9 | Add stamina/commute mechanics that interrupt digging | "remove the beer drinking crap… I want to dig"; Hydroneer's no-inventory hauling loop is its biggest complaint | Battery is the only pressure; no commuting design (`03`) |
| 10 | Punish falls with health/chip damage | "fall damage is not gracious"; 1-voxel specks break legs | Battery knock + stagger; never health (`04`, `10`) |
| 11 | Add hunger, oxygen, warmth, food, overheating or other upkeep meters | "absolutely unnecessary to have dmg in a game like this"; developer playthrough: "the overheating mechanic is really annoying" | None; NOT-list (`03`) |
| 12 | Make darkness pitch black | "extreme darkness" complaints | Dim ambient floor everywhere (`03`) |
| 13 | Drain battery for looking, reading or standing still | Battery as a nag | Drain only on powered actions (`06`) |
| 46 | Add a day/night cycle, forced rest or time-gated content | Players recommend Ore Factory Squad as a chill solo game, then cite its short day, night dig penalty and sleep blackouts as the top reason solo play stops being fun | The battery and the player's greed are the only pressure; the clock never gates digging or content (`06`, `10`) |

## Discovery and content

| # | Never | Evidence | Rule here |
|---|---|---|---|
| 14 | Turn the detector into a value radar | Ordinary finds become waste | No value/rarity hints, ever (`05`) |
| 15 | Leave floating specks that snag movement | "1x1-pixel particles that will break your legs"; Ore Factory Squad's reviewers specifically praised that its digging left no floating bits — clean cleanup is a selling point | Disconnected voxels auto-collect; no collidable debris (`03`) |
| 16 | Require archaeology chores (brushing, 100% cleaning, analysis timers) | Identification fatigue | Recognition without bureaucracy (`05`) |
| 17 | Ship a game where the trailer is the whole game | "what you see in the trailer is what you get" | Four zones, escalating silhouettes, density rules (`02`, `05`) |
| 18 | Clump all novelty early / empty late game | "the game ends the second it should open up" | Validated pacing, late silhouettes (`02`) |
| 19 | Depth-only value with nothing sideways | Straight-down trivialization; Ore Factory Squad tied worth strictly to depth and ended with top-tier floods while its basic inputs went scarce | Clusters, off-shaft components, category-not-value (`03`) |
| 20 | Unbreakable decoy obstacles, or solutions the player cannot discover | "unbreakable obstacles"; One Man's Trash's worm/TNT counterplay existed but was invisible — "there is no way to fight back at all" | Every boundary looks different; every pocket has solutions, and at least one is visibly telegraphed (`03`) |

## Tone and honesty

| # | Never | Evidence | Rule here |
|---|---|---|---|
| 21 | Unadvertised horror or scary content | "not labelled as a horror type game" | None exists; no horror tag (`01`, `10`) |
| 22 | Bait-and-switch ending or genre shift | stealth-horror finale; "it was a game show" | Normal systems at the finale; honest ending (`11`) |
| 23 | Disable the player's tools for drama | mole finale strips everything | Tools always work (`11`) |
| 24 | Toilet/body-sound humor or joke spam | toilet humor backlash | Deadpan object humor, rare, no sound gags (`01`) |
| 25 | NPCs, dialogue trees, or quest-givers | not wanted; story via objects | Machines and finds only (`07`, `11`) |
| 26 | Fake difficulty through controls getting worse | — | Jetpack only improves; control quality never degrades (`04`) |
| 40 | Real-world politics, partisan slogans, or living controversies | "Politics and gaming don't mix"; Trump coin review backlash | Fictional setting; original deadpan parody only (`01`, `05`) |

## Interface and body

| # | Never | Evidence | Rule here |
|---|---|---|---|
| 27 | Click-per-dig, no hold-to-dig | RSI warnings; "not gonna mash m1 over hours" | Hold-to-dig from minute one (`04`) |
| 28 | Fixed keybinds or no rebinding | left-handed/fixed-key complaints | Full rebinding everywhere (`08`) |
| 29 | FOV/shake/bob without controls | motion sickness refunds | Comfort suite with safe defaults (`10`) |
| 30 | Complete toggle that doesn't remove the content | "I'm forced to enable it" | Every toggle fully removes its content (`10`) |
| 31 | Settings that don't persist; ESC that doesn't close menus | recurring complaints | Immediate persistence; correct back behavior (`08`) |
| 32 | Color-only information | colorblind lockout | Shape + label redundancy (`10`) |
| 33 | Audio-only clues in a music-less game | playable-muted requirement | Visual counterparts for every cue (`09`) |
| 34 | A permanent tutorial or popup spam | tutorial complaints; Ore Factory Squad's forced, unskippable tutorial that could not be saved through caused restarts before play began | No tutorial; diegetic labels (`07`) |
| 45 | Land an interaction anywhere but where the player aims | Hydroneer's offset drop cursor — a second cursor below the right hand — is one of its most-criticized mechanics; players learn to bracket-drop instead of using it | Results land at the aim point or at a clearly previewed valid surface (`08` §4, `10` §2) |
| 50 | Surface achievements as in-game checklists or task lists | Developer playthrough: "collect X bags, sell X items" checkbox tasks were an annoyance; achievements should be a record, not a to-do list | Achievements live on Steam, never as HUD chores (`12`) |

## Saves and trust

| # | Never | Evidence | Rule here |
|---|---|---|---|
| 35 | Lose the hole, inventory or display on load | "saving only saves your upgrades, not the hole" | Full state persistence (`08`) |
| 36 | Delete or corrupt saves; no backups | "Saves disappeared?!" | Autosave + manual slots + independent rolling backup generations with validated fallback (`08` §7) |
| 37 | Make balance patches reroll an existing world | "rebalanced… now I can't reach the end of a tunnel" | Population persists; no forced rerolls (`03`) |
| 38 | Lock achievements behind NG+, RNG or bugs | "INCREDIBLY scummy"; 45/46 forever | Fair one-run achievements derived from visible state (`12`) |
| 39 | Delete or invalidate the display / collection | progress loss | Display is permanent in the save (`07`) |
| 41 | Trigger the finale purely via depth or void boundary volumes | Falling into void/collision seams triggering credits | Finale requires intentional physical insertion of components (`11`) |
| 42 | Block the main thread during save serialization or freeze the game on save | Digger: Galactic Treasures PC freezes for 15–60s on every save due to synchronous whole-world voxel serialization | Asynchronous non-blocking background serialization (<100ms budget) (`08`, `14`) |

## The one-line version

> Keep the hole, keep the loot, keep the tool, keep the wonder. Never take anything away that the
> player earned, and never surprise them with a different game.
