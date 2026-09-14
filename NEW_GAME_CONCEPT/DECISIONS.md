# Decision Register

**Single source of truth for the game's design.** If any file in `CONCEPT/` disagrees with this
register, the register wins. Open items live in `CONCEPT/13_OPEN_QUESTIONS.md`. How research updates
this file: `ITERATION_GUIDE.md`.

**Statuses:** `PENDING` · `OPEN` · `DISCUSSING` · `CONFIRMED` · `REVISED` · `REJECTED` · `DELEGATED` · `DEFERRED`

**Rules**

1. I never mark anything `CONFIRMED` on the developer's behalf.
2. Bulk answers are allowed at group level, but every row still gets its own status line.
3. Changing a decision requires a new dated entry in the log; old entries are struck through, never
   deleted.
4. A decision later contradicted by review evidence is flagged, not silently overridden.
5. No business, marketing, production, resourcing, team, budget, timeline or implementation
   questions.
6. Questions stay on the game itself.
7. No silent assumptions: even settled ideas can be re-questioned.
8. Numbers are prototype-tuned; decisions stay at rules/variations level.
9. New IDs continue the sequence (Q31+, W13+, S13+, D14+, I17+, F13+, P07+, A02+); IDs are never
   reused or renumbered. Maintenance steps: see the root `README.md` §"How to update as we go".

---

## Round 1 — Vision, identity, scope

| ID | Decision | Status |
|---|---|---|
| Q01 | Decision authority: bulk-confirm audit keepers; contested items reviewed individually | `CONFIRMED` |
| Q02 | Keep the core fantasy (detector loop, recognition reveals, free-form hole, one evolving tool, Continue Playing); revisions: loot-safe recovery, 3–5 h, no return aids, no separate guns | `CONFIRMED (C01)` |
| Q03 | Title: **Something Down There** | `CONFIRMED` |
| Q04 | Drained river-fed reservoir; Danube-style news of exposed valuables as motivation | `CONFIRMED (C02)` |
| Q05 | Fictional country; Eastern-European-coded humor and objects | `CONFIRMED` |
| Q06 | Silent first-person nobody; no face, no voice | `CONFIRMED` |
| Q07 | Discovery and upgrade carry equal weight | `CONFIRMED` |
| Q08 | Fun/absurdity/curiosity first; relaxation secondary; honest marketing | `CONFIRMED` |
| Q09 | Humor object/deadpan based, rare, never a main pillar; no toilet/body-sound gags | `REVISED` |
| Q10 | Light slow-build mystery | `CONFIRMED` |
| Q11 | No NPCs; story told by objects, machines, display and environment | `REVISED` |
| Q12 | Final discovery: a modern object built in impossibly ancient materials | `REVISED` |
| Q13 | Full NOT-list confirmed (no archaeology/survival/crafting/puzzle/management/hazards/meters) | `CONFIRMED` |
| Q14 | Genre fans primary; streamers/meme audience secondary; must be a real game | `CONFIRMED` |
| Q15 | E10+ / PEGI 7 | `CONFIRMED` |
| Q16 | 30–60 minute sessions | `CONFIRMED` |
| Q17 | 3–5 h first completion @ $6.99–9.99 | `CONFIRMED` |
| Q18 | Per-save randomized world; display per-save; no meta progression | `CONFIRMED` |
| Q19 | PC primary; full controller support mandatory; Deck optional; no consoles | `REVISED` |
| Q20 | Complete 1.0, no Early Access; short pre-release demo/playtest window | `CONFIRMED (C03)` |
| Q21 | No permanent demo | `REVISED` |
| Q22 | Post-launch: free bugfixes and small QoL only | `REVISED` |
| Q22b | Ambience and action feedback only; no music; no voice acting (evidence flag 2026-09-14: AGADAH music praised; decision reaffirmed) | `CONFIRMED` |
| Q23 | Localization: parked | `DEFERRED` |
| Q24 | No co-op; save format stays future-proof | `CONFIRMED` |
| Q25 | One single difficulty | `REVISED` |
| Q26 | Recovery keeps all loot; depth-scaled fee + interest-free auto-debt; auto-trigger at 0 fuel | `CONFIRMED` |
| Q27 | No return aids; vertical return only; keep the return-power warning | `REVISED` |
| Q28 | No health bar; falls stagger + knock battery; extreme falls trigger recovery | `CONFIRMED` |
| Q29 | Shared dig + jetpack battery | `CONFIRMED` |
| Q30 | C4 IN as a late-game tool | `CONFIRMED` |
| Q30b | One machine + attachments; final form is the absurd shovel-cannon; no separate gun | `CONFIRMED` |
| Q30c | Crouch IN; lights IN (dark areas exist); item condition OUT | `CONFIRMED` / `REVISED` / `REJECTED` |
| Q31 | Ending fame shown diegetically: a media wall (news clippings, radio, TV) accumulates in the yard after the discovery; no characters, no dialogue | `CONFIRMED` |

## Round 2 — World and terrain

| ID | Decision | Status |
|---|---|---|
| W01 | Site depth at least 100 m (exact depth and footprint set by feel in playtest) | `CONFIRMED (depth floor) / OPEN (size)` |
| W02 | Boundaries: reservoir infrastructure (concrete/dam) + bedrock, visually distinct from diggable ground | `CONFIRMED` |
| W03 | No personal light; open-shaft sky light + dim ambient floor; placeable lamps for real visibility; never pitch black | `CONFIRMED` |
| W04 | Four depth zones with changing ground, minerals and mood; exact material list TBD | `DEFERRED` |
| W05 | Rare optional hard pockets (concrete plug, river-rock lens, gravel shelf); multiple solutions; no specific-upgrade gating | `CONFIRMED` |
| W06 | Full voxel free-form terrain; tunnels/overhangs; disconnected valuable voxels auto-collect, plain dirt vanishes; debris visual-only | `CONFIRMED` |
| W07 | Four distinct zones: recent fill → old river sediment → deep clay/stone → ancient constructed | `CONFIRMED` |
| W08 | Compact yard; stations within ~10 s; uniques physically displayed | `CONFIRMED` |
| W08b | Display: predefined outlines; empty frames visible, shapes hidden; player places finds into waiting spots | `CONFIRMED` |
| W09 | Validated random placement; authored depth ranges; population persists per save | `CONFIRMED` |
| W10 | Open edge is bedrock; no swimming or flooding | `CONFIRMED` |
| W11 | Voxel/chunk size: prototype-tuned | `DEFERRED` |
| W12 | No map; depth readout, display and detector direction handle memory | `CONFIRMED` |

## Round 3 — Systems and progression

| ID | Decision | Status |
|---|---|---|
| S01 | Tracks: Tool, Battery, Jetpack, Inventory, Detector + small C4 track | `CONFIRMED` |
| S02 | Levels: many small increments with a major capability change roughly every third level (the 30–45 min purchase cadence measures these milestones, not every level); count flexible; visuals escalate | `CONFIRMED` |
| S03 | Money-only progression; late sinks exist | `CONFIRMED` |
| S03b | Late sinks: extra charges, lamps, display upgrades, cosmetics, conveniences | `CONFIRMED` |
| S04 | Shared battery; paid surface refill (full/partial); drain only on powered actions; safe/risky/critical warning; bigger tank keeps current fuel | `CONFIRMED` |
| S05 | Generous starting capacity; strong growth steps | `CONFIRMED` |
| S05b | Hard stop when full; finds stay in the world; uniques/key items never blocked; nothing deleted | `CONFIRMED` |
| S06 | Detector: range/clarity/direction upgrades; never value or rarity; visual cues; one target; quiet intervals | `CONFIRMED` |
| S07 | Jetpack: stable from the start; upgrades only improve (speed, efficiency, altitude, assists); control never degrades | `CONFIRMED` |
| S08 | C4: thrown in multiples, stick where they land, remote detonation; powerful; costs money; optional accelerator | `CONFIRMED` |
| S09 | Tool: automatic material adaptation; no manual switching; converges late; exact late behavior validated in playtest | `CONFIRMED (provisional)` |
| S10 | Passive upgrades: deprioritized until playfeel review; find-or-buy still the leading option; passive/unique effects must preserve challenge (no sudden power spikes) | `DEFERRED` |
| S11 | Shop: fully transparent (current→next, cost, benefit); sequential purchase; locked tiers visible | `CONFIRMED` |
| S12 | Post-ending: full Continue Playing; economy live; achievements on the same save | `CONFIRMED` |

## Round 4 — Discoveries and content

| ID | Decision | Status |
|---|---|---|
| D01 | Common finds: 20–30 types; detector-silent; reliable income | `CONFIRMED` |
| D02 | Distinctive finds: 30–50 types; produced in batches (5-object slice first) | `CONFIRMED` |
| D03 | Find purpose: no keep/sell choice; each type has one fixed purpose; distinctive purpose TBD after research | `DEFERRED` |
| D04 | Detector targets: distinctive + unique only; some distinctives silent by design; size/metal/price never decide | `CONFIRMED` |
| D05 | Value: 4 bands — common income, distinctive value, rare (several expeditions), unique (effect) | `CONFIRMED` |
| D06 | Clusters: 5 authored micro-scene templates, rotated/placed procedurally | `CONFIRMED` |
| D07 | First-slice objects: washing machine, hand drill, gearbox, mammoth bone, gramophone | `CONFIRMED` |
| D08 | Mystery: 3-step escalation (anachronistic junk → too-correct objects → constructed impossibilities) | `CONFIRMED` |
| D09 | Ending components: 3–4, never lost, no slots, no puzzle, obvious insertion | `CONFIRMED` |
| D10 | Large discoveries: a few per run; excavated then cable-yanked; some may stay | `CONFIRMED` |
| D11 | Display form: growing wall/shelf with predefined outlines; no player choice of placement | `CONFIRMED` |
| D11b | Empty display frames visible; item shapes hidden until discovered | `CONFIRMED` |
| D12 | Pacing: guaranteed early find; bounded dry spells; one major-scale find per zone; new silhouettes to the end | `CONFIRMED` |
| D13 | References: original parody only; no real brands or games | `CONFIRMED` |
| D14 | Uniques carry a one-sentence story; delivery trigger (pickup vs inspection) still open | `CONFIRMED (trigger OPEN)` |

## Round 5 — Interface and accessibility

| ID | Decision | Status |
|---|---|---|
| I01 | HUD minimal: depth, bag count/capacity, battery, return warning; detector feedback diegetic | `CONFIRMED` |
| I02 | No tutorial | `REVISED` |
| I02b | Learning via diegetic labels/signs on machines; pause reference lists controls | `CONFIRMED` |
| I03 | Pause menu: direction Resume / New Game / Settings / Exit; exact tabs later | `DEFERRED` |
| I04 | Inventory: inspect-only grid; no stats/equipping/sorting; selling only at the machine | `CONFIRMED` |
| I05 | Selling: one-button Sell All with physical animation; individual selling available there | `CONFIRMED` |
| I06 | Purchase order: strict sequence; no skipping; future levels visible | `CONFIRMED` |
| I07 | Controls: hold-to-dig + toggle; full rebinding; controller parity; left-handed preset; sensitivity; optional gyro | `CONFIRMED` |
| I08 | Motion comfort: FOV slider, shake 0–100% (low default), head bob toggle, comfort preset, no forced roll; settings persist | `CONFIRMED` |
| I09 | Readability: colorblind palettes, shape+label redundancy, contrast option, subtitles for all significant sounds | `CONFIRMED` |
| I10 | Motor access: auto-dig assist, toggle holds, one-hand presets, no mashing/QTEs, generous buffering | `CONFIRMED` |
| I11 | Cognitive comfort: pause anywhere, no timed content, no missables, no FOMO | `CONFIRMED` |
| I12 | Text scale / screen reader: optional later | `DEFERRED` |
| I13 | Photo mode: pause-only; hide HUD, FOV, filters, watermark; no free camera | `REVISED` |
| I14 | Saves: autosave + 3 manual slots; Steam Cloud later | `REVISED` |
| I15 | Achievements: a few fair Steam achievements | `REVISED` |
| I16 | Content disclosure: marketing; not decided | `DEFERRED` |

## Round 6 — Art, audio and feel

| ID | Decision | Status |
|---|---|---|
| F01 | Visual style: stylized painted low-poly; strong silhouettes; cohesive custom art | `CONFIRMED` |
| F02 | Strong distinct palettes per zone with gradual transitions | `CONFIRMED` |
| F03 | Controlled absurdity: insane homemade tool + object identity + physical comedy; deadpan | `CONFIRMED` |
| F04 | Tool only visible; no hands | `REVISED` |
| F05 | Dig feel: chunky, weighted, per-material debris/audio, steady camera, no shake | `CONFIRMED` |
| F06 | Audio: layered zone ambience + per-material dig loops + station feedback; no music/VO | `CONFIRMED` |
| F07 | Detector presentation: deferred; options documented (hybrid / edge indicator / tool reaction) | `DEFERRED` |
| F08 | FX: comfort-safe (dust/crumbs/sparkles/C4 smoke); no shake/gore/flashes; adjustable | `CONFIRMED` |
| F09 | Lighting moods per zone: warm daylight → cool dim → near-black deep; lamps make readable pools | `CONFIRMED` |
| F10 | UI art style: clear, not retro; exact style later | `DEFERRED` |
| F11 | Tool visuals: bolt-on escalation; one continuous absurd machine | `CONFIRMED` |
| F12 | Material feel: distinct per-family shape/audio/particles/resistance | `CONFIRMED` |

## Round 7 — Design-relevant production outcomes

| ID | Decision | Status |
|---|---|---|
| P02 | Engine: Unity | `CONFIRMED` |
| P05 | Completion: credits + display outlines + all upgrades + zone stats; never 100% terrain | `CONFIRMED` |
| P06 | Achievements: 5–10 fair ones; no grind/RNG/NG+ locks | `CONFIRMED` |
| P01 / P03 | Team and performance questions: out of scope (Rule 5) | `REJECTED (question)` |

## Policy and confirmed proposals

| ID | Decision | Status |
|---|---|---|
| A01 | Assets: custom Blender models (AI-assisted workflow acceptable, real references); no AI-generated images/textures; licensed audio only if needed; parody references only | `CONFIRMED (REVISED)` |
| C01 | Keep core fantasy; revisions per Q02 | `CONFIRMED` |
| C02 | Setting and motivation per Q04 | `CONFIRMED` |
| C03 | Release approach per Q20 | `CONFIRMED` |

---

## Decision log (dated, append-only)

| Date | ID | Change | Reason | By |
|---|---|---|---|---|
| 2026-09-14 | — | Process started; Rounds 1–6 and delegated proposals answered; concept set written | Process | process |
| 2026-09-14 | C01–C03, A01 | Delegated proposals and asset policy confirmed | Developer answers | user |
| 2026-09-14 | W10 | Water vs bedrock boundary remains open | Developer undecided | user |
| 2026-09-14 | — | Process docs archived; L-register retired; concept files cleaned of legacy citations | Organization | process |
| 2026-09-14 | — | Decision register rewritten as the full, standalone source of truth; iteration guide created | Organization | process |
| 2026-09-14 | W01 | Depth floor fixed at ≥100 m; exact depth/footprint decided by feel in playtest | Developer answer | user |
| 2026-09-14 | W10 | Open edge decided: bedrock (water ruled out) | Developer answer | user |
| 2026-09-14 | W06 | Cleanup rule: only valuable disconnected voxels auto-collect; plain dirt vanishes | Developer answer | user |
| 2026-09-14 | Q31 | Ending fame delivered via diegetic accumulating media wall | Developer answer | user |
| 2026-09-14 | S02 | Cadence clarified: small levels frequent; 30–45 min target = milestone purchases | Developer answer | user |
| 2026-09-14 | Q22b | Evidence flag from AGADAH review refresh; no-music decision reaffirmed | Developer answer | user |
| 2026-09-14 | S10 | Passive upgrades deprioritized until playfeel review | Developer answer | user |
| 2026-09-14 | D03, S10, — | Decisions deferred; constraint recorded: unique/passive effects must preserve challenge, no sudden power spikes; endless mode gated on a feasibility spike | Developer answers | user |
| 2026-09-14 | D14 | Uniques carry a one-sentence story; delivery trigger (pickup vs inspection) deferred | Developer answer | user |
