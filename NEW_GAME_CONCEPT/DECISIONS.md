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
9. Keep concept questions about the game's identity and experience; routine settings and bug fixes
   are implementation work. Interview answers 35–36 adopted no new requirements.
10. New IDs continue the sequence (Q31+, W13+, S13+, D14+, I17+, F13+, P07+, A02+); IDs are never
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
| Q08 | Fun/absurdity/curiosity first; relaxation secondary; honest marketing (evidence: relaxing/chill is the most positively-rated theme in Hydroneer's reviews — the calm payoff stays a first-class result of the loop, never an afterthought; Ore Factory Squad's reviewers recommend it for exactly that calm while its day timer and sleep penalty are their sharpest solo complaint, so time pressure never enters the loop) | `CONFIRMED` |
| Q09 | Humor object/deadpan based, rare, never a main pillar; no toilet/body-sound gags | `REVISED` |
| Q10 | Light, object-led mystery: related discoveries reveal one enormous construction; following it is optional until choosing to finish the story (D18) | `REVISED` |
| Q11 | No NPCs; story told by objects, machines, display and environment | `REVISED` |
| Q12 | Final discovery: a recognizable modern function in impossibly ancient materials, explaining the larger construction; exact object chosen after the loop works | `REVISED (identity DEFERRED)` |
| Q13 | Full NOT-list confirmed (no archaeology/survival/crafting/puzzle/management/hazards/meters) (evidence: unadvertised horror is One Man's Trash's standout complaint and AGADAH's creepy finale divided its audience — the impossible must read as awe, never threat; concept `11` §1, `09` §6) | `CONFIRMED` |
| Q14 | Genre fans primary; streamers/meme audience secondary; must be a real game | `CONFIRMED` |
| Q15 | E10+ / PEGI 7 | `CONFIRMED` |
| Q16 | 30–60 minute sessions | `CONFIRMED` |
| Q17 | 3–5 h first completion @ $6.99–9.99 (evidence: perceived value tracks density, polish and replayability more than hours — One Man's Trash at ~3 h drew "not enough content" complaints while AGADAH at a similar size keeps a strongly positive rating; Ore Factory Squad's 15–20 h still drew "not enough content" because progression hit a hard cap before the player was done — the ending lands after the loop is fully expressed and post-credits goals stay visible; price unchanged) | `CONFIRMED` |
| Q18 | Fresh progression and a personal display per save; randomized arrangements of a complete required content set; no equipment, collection or completion carryover | `REVISED` |
| Q19 | PC primary; full controller support mandatory; Deck optional; no consoles | `REVISED` |
| Q20 | Complete 1.0, no Early Access; short pre-release demo/playtest window | `CONFIRMED (C03)` |
| Q21 | No permanent demo | `REVISED` |
| Q22 | Post-launch: free bugfixes and small QoL only | `REVISED` |
| Q22b | Ambience and action feedback only; no music; no voice acting (evidence: AGADAH's music is specifically praised in its reviews; no-music decision reaffirmed) | `CONFIRMED` |
| Q23 | Localization: parked | `DEFERRED` |
| Q24 | Solo; no co-op or shared economy. Separate sharing features are rejected under Q32 | `REVISED` |
| Q25 | One single difficulty | `REVISED` |
| Q26 | At zero charge underground, keep all finds and recover with full charge for one disclosed depth-scaled rescue/refill fee; interest-free debt protects the next basic refill. At the yard use the fuel point, with basic restart credit if broke, never another rescue | `REVISED` |
| Q27 | Return through the player-made excavation using the stable jetpack and existing reusable lamps; no added transport, normal surface teleport or map; retain the broad return warning | `REVISED` |
| Q28 | No health bar. Ordinary falls give harmless landing feedback without battery loss, forced input lock or surface recovery | `REVISED` |
| Q29 | One battery for powered digging and jetpack thrust; an action budget, never a clock. Looking, reading, standing and pausing do not drain it | `REVISED` |
| Q30 | C4 IN as a late-game tool | `CONFIRMED` |
| Q30b | One machine + attachments; final form is the absurd shovel-cannon; no separate gun | `CONFIRMED` |
| Q30c | Crouch IN; lights IN (dark areas exist); item condition OUT | `CONFIRMED` / `REVISED` / `REJECTED` |
| Q31 | One short, pausable/skippable ending: fame through printed/captioned media about this save's actual finds and depth; no faces, voices or music; same hole and equipment afterward | `REVISED` |

## Round 2 — World and terrain

| ID | Decision | Status |
|---|---|---|
| W01 | Compact vertical site at least 100 m deep, with worthwhile lateral room; exact depth and footprint decided in play | `REVISED (dimensions OPEN)` |
| W02 | Boundaries: reservoir infrastructure (concrete/dam) + bedrock, visually distinct from diggable ground | `CONFIRMED` |
| W03 | No personal light. Sky light in open shafts plus ambient light that always preserves ground and object shapes; reusable lamps improve detail/color, do not expire or drain charge, and remain recoverable/repositionable | `REVISED` |
| W04 | Four depth zones remain fixed; prototype five response groups first: loose earth, clay/sediment, gravel, rock, diggable concrete. Exact material roster stays open | `DEFERRED` |
| W05 | Optional hard pockets always show visible progress with the early tool; upgrades, C4 and routing save effort. No specific-upgrade or mandatory depth gate; distinguish tough ground from boundaries | `REVISED` |
| W06 | Free-form voxel terrain preserves substantial player-made forms. Plain crumbs vanish; valuables become visible pickups subject to capacity; overflow persists nonblocking. Cleanup never deletes or auto-collects interesting discoveries | `REVISED` |
| W07 | Four distinct zones: recent fill → old river sediment → deep clay/stone → ancient constructed | `CONFIRMED` |
| W08 | Compact yard; stations within ~10 s; uniques physically displayed | `CONFIRMED` |
| W08b | Display spaces are available and visible without spoiling undiscovered shapes; the player chooses any compatible shelf/stand. No assigned per-object outline or frame-purchase gate | `REVISED` |
| W09 | Validate each complete finite population before play; vary placements within authored depth bands and relationships. Connected construction parts keep coherent geometry. Save the result; patches never reroll it | `REVISED` |
| W10 | Open edge is bedrock; no swimming or flooding | `CONFIRMED` |
| W11 | Voxel/chunk size: prototype-tuned | `DEFERRED` |
| W12 | Never add a map. A compact vertical excavation, stable jetpack and reusable lamps support easy returns; depth is information, not a hidden horizontal-position display | `REVISED` |

## Round 3 — Systems and progression

| ID | Decision | Status |
|---|---|---|
| S01 | Six tracks: Tool, Battery, Jetpack, Bag capacity, Detector and a small optional C4 track | `REVISED` |
| S02 | Fewer stronger upgrades within existing tracks; every purchase noticeably improves the next outing and applies immediately. Count and cadence are prototype-tuned | `REVISED` |
| S03 | One currency; fixed sale price per type at every depth. Deeper zones can contain more valuable types. Value may sum but never grow through duplication/combining; no display-completion cash reward | `REVISED` |
| S03b | Optional C4, reusable lamps and cosmetics support remaining play. Basic display capacity is available without buying frames. No forced upkeep; money may stop mattering after finite completion | `REVISED` |
| S04 | Paid full/partial surface refills; bigger tanks keep current charge and do not raise the price of the same energy quantity. Broad safe/risky/critical warning treats unknown routes conservatively; recovery follows Q26 | `REVISED` |
| S05 | Generous starting capacity; strong growth steps | `CONFIRMED` |
| S05b | A full bag stops ordinary pickup, not digging/travel; finds and nonblocking overflow persist. No discarding. Special exhibits and keys never use ordinary capacity or get lost | `REVISED` |
| S06 | Passive silent detector; range/clarity/direction upgrades, no identity/value/rarity. One nearby target stays until collection or moving away; quiet intervals and broad visual cues | `REVISED` |
| S07 | Stable jetpack from the start; upgrades improve speed, efficiency and assists. No upgrade-locked altitude ceiling; returns through familiar ground become easy | `REVISED` |
| S08 | Paid optional C4: multiple sticky charges, remote detonation, predictable powerful excavation. Interesting finds stay for deliberate collection; valuables and lamps survive, overflow persists | `REVISED` |
| S09 | One tool with automatic material adaptation through the final tier; no manual mode choice or uniform late vacuum convergence. Feedback shows the selected response; one Tool track improves all responses | `REVISED` |
| S10 | All permanent mechanical power comes from the existing shop tracks; no found passive upgrades or mechanical perks from unique exhibits | `REVISED` |
| S11 | Shop: fully transparent (current→next, cost, benefit); sequential purchase; locked tiers visible | `CONFIRMED` |
| S12 | Continue Playing preserves the same finite hole, equipment, economy and collection; missed content and achievements remain available. Completion can be a satisfying stopping point | `REVISED` |

## Round 4 — Discoveries and content

| ID | Decision | Status |
|---|---|---|
| D01 | Common finds: 20–30 types; detector-silent; reliable income | `CONFIRMED` |
| D02 | Distinctive finds: 30–50 types; produced in batches (5-object slice first) | `CONFIRMED` |
| D03 | Ordinary and repeatable distinctive finds sell through Sell All. A small set of special exhibits and keys is unsellable; one purpose per type, no first-copy/duplicate routing or keep/sell sorting | `REVISED` |
| D04 | Commons are detector-silent; noteworthy distinctives and uniques signal, with some optional distinctives silent. Eligibility is authored, never price/size/metal; required parts have discoverable trails via the existing detector and related objects | `REVISED` |
| D05 | Sale values and collection roles are separate: ordinary, distinctive and rare payouts; rare sales help a major purchase without buying half the tree. Uniques reward permanent display/story only, with no money or power effect | `REVISED` |
| D06 | Five starting related-object scene templates: bones, vehicle parts, household remains, machinery and deliberate oddities. Build coherent buried places; random placement preserves relationships | `REVISED` |
| D07 | First-slice objects: washing machine, hand drill, gearbox, mammoth bone, gramophone | `CONFIRMED` |
| D08 | Anachronistic junk → too-correct objects → constructed impossibilities. Shared joints, seams and fittings connect major discoveries to the larger construction without a code or puzzle | `REVISED` |
| D09 | 3–4 ending parts, unsellable, loss-proof and outside bag capacity. Ownership makes them automatically available; one interaction inserts any collected parts, leaving missing sockets visible. Complete intentional insertion is required for the finale | `REVISED` |
| D10 | Extractable large finds deliver the whole object after enough exposure: short local extraction then automatic surface transfer, without a car-wide route or camera takeover. Structural landmarks may remain and receive discovery credit; animation tested in play | `REVISED` |
| D11 | Safely store special exhibits on pickup; handle and place them individually at the yard in any compatible shelf/stand. No underground carrying task. Name, depth and story inspection; no price/condition/rarity labels | `REVISED` |
| D11b | Show empty display capacity without undiscovered silhouettes; completion follows collected/placed exhibits, not prescribed slot identities or arrangement | `REVISED` |
| D12 | Early recognizable discovery, first sale sufficient for a purchase, one guaranteed major find per zone and new silhouettes through the end. Validate gaps along representative routes and preserve accepted populations | `REVISED` |
| D13 | References: original parody only; no real brands or games (evidence: iDigging's real-world political cameo drew dedicated negative review backlash across languages — original parody only; anti-pattern 40) | `CONFIRMED` |
| D14 | Uniques have a one-sentence story. First delivery is playtest-deferred, leaning before placement; placed objects always allow inspection/rereading. No inventory delivery or compulsory reading | `REVISED (trigger DEFERRED)` |
| D15 | Uniques exist exactly once per save. Commons are visible before automatic collection with no inspection chores; repeatable distinctives remain deliberately collectible. Developer reports common visibility already implemented in the demo | `REVISED` |

## Round 5 — Interface and accessibility

| ID | Decision | Status |
|---|---|---|
| I01 | Minimal HUD: depth, bag capacity, battery and broad return warning; silent detector feedback on tool plus subtle screen-edge direction | `REVISED` |
| I02 | No compulsory tutorial or popup chain. Teach through world labels, contextual action prompts and optional controls reference; the first find-sell-upgrade loop must work unaided | `REVISED` |
| I02b | Learning via diegetic labels/signs on machines; pause reference lists controls | `CONFIRMED` |
| I03 | Menu direction: Resume / Save & Load / Settings / Exit to Title; New Game on title screen, clear world-overwrite warning; final layout is implementation work | `REVISED` |
| I04 | No inventory screen. Abstract bag and HUD capacity; inspect discoveries in-world and on displays, sell at the machine, use owned keys automatically | `REVISED` |
| I05 | One-button Sell All banks money immediately; physical haul animation is nonblocking and may react to the haul. No depositing/sorting; individual selling remains optional at the machine | `REVISED` |
| I06 | Purchase order: strict sequence; no skipping; future levels visible | `CONFIRMED` |
| I07 | Controls: hold-to-dig + toggle; full rebinding; controller parity; left-handed preset; sensitivity; optional gyro | `CONFIRMED` |
| I08 | FOV/bob controls and optional comfort preview/preset; zero camera shake, no digging/C4 shake or forced roll. Existing useful settings persist; no mandatory first-launch questionnaire | `REVISED` |
| I09 | Readability: colorblind palettes, shape+label redundancy, contrast option, subtitles for all significant sounds | `CONFIRMED` |
| I10 | Hold/toggle digging, one-hand presets, no mashing/QTEs, generous buffering and forgiving placement. Any additional auto-dig assist needs a distinct purpose beyond normal hold/toggle | `REVISED` |
| I11 | Cognitive comfort: pause anywhere, no timed content, no missables, no FOMO (evidence: Ore Factory Squad's day/night deadlines, closed contract counters and sleep penalty turned a game its players recommend as chill into a solo rush — the clock never gates digging or content) | `CONFIRMED` |
| I12 | Text scale / screen reader: optional later | `DEFERRED` |
| I13 | Photo mode: pause-only; hide HUD, FOV, filters, watermark; no free camera | `REVISED` |
| I14 | Saves: autosave + 3 manual slots + independent rolling backup generations; Steam Cloud later (evidence: save integrity is the biggest trust issue in the genre's reviews — async non-blocking writes plus independent rolling backups are mandated; concept `08` §7, anti-pattern 42) | `REVISED` |
| I15 | Achievements: a few fair Steam achievements; eligibility derives from visible state only, never a hidden lockout flag (concept `12` rule 9) | `REVISED` |
| I16 | Content disclosure: marketing; not decided | `DEFERRED` |

## Round 6 — Art, audio and feel

| ID | Decision | Status |
|---|---|---|
| F01 | Visual style: stylized painted low-poly; strong silhouettes; cohesive custom art | `CONFIRMED` |
| F02 | Strong distinct palettes per zone with gradual transitions | `CONFIRMED` |
| F03 | Controlled absurdity: insane homemade tool + object identity + physical comedy; deadpan | `CONFIRMED` |
| F04 | Tool only visible; no hands | `REVISED` |
| F05 | Dig feel: chunky, weighted, per-material debris/audio, steady camera, no shake (evidence: dig feel is the strongest positive theme in Ore Factory Squad's reviews — reviewers single out smooth digging and the absence of floating debris as its best quality) | `CONFIRMED` |
| F06 | Audio: layered zone ambience + per-material dig loops + station feedback; no music/VO | `CONFIRMED` |
| F07 | Silent tool reaction plus a subtle broad screen-edge direction cue; readable beyond color, with no object identity, value, rarity or hidden outline | `REVISED` |
| F08 | FX: comfort-safe (dust/crumbs/sparkles/C4 smoke); no shake/gore/flashes; adjustable | `CONFIRMED` |
| F09 | Warm daylight → cool dim → quiet deep-zone light; ground and object shapes always remain readable. Lamps improve detail and color; darkness never defeats recognition | `REVISED` |
| F10 | Clear industrial-worksite UI: clean type, simple shapes and high contrast; final art treatment later | `REVISED` |
| F11 | Tool visuals: bolt-on escalation; one continuous absurd machine | `CONFIRMED` |
| F12 | Material feel: distinct per-family shape/audio/particles/resistance | `CONFIRMED` |

## Round 7 — Design-relevant production outcomes

| ID | Decision | Status |
|---|---|---|
| P02 | Engine: Unity | `CONFIRMED` |
| P05 | 100% in this save: ending, all special exhibits collected and placed, all upgrade tracks maxed, every zone reached. No terrain-clearing requirement; Steam achievements are a separate record | `REVISED` |
| P06 | Achievements: 5–10 fair ones; no grind/RNG/NG+ locks | `CONFIRMED` |
| P01 / P03 | Team and performance questions: out of scope (Rule 5) | `REJECTED (question)` |

## Policy and confirmed proposals

| ID | Decision | Status |
|---|---|---|
| A01 | Assets: custom Blender models (AI-assisted workflow acceptable, real references); no AI-generated images/textures; licensed audio only if needed; parody references only (evidence: Ore Factory Squad's most-upvoted negative review accuses it of being vibe-coded end to end while its positive reviews defend it as "not AI slop" — cohesive custom art is a trust feature) | `CONFIRMED (REVISED)` |
| C01 | Keep core fantasy; revisions per Q02 | `CONFIRMED` |
| C02 | Setting and motivation per Q04 | `CONFIRMED` |
| C03 | Release approach per Q20 | `CONFIRMED` |

---

## Interview additions — 2026-09-15

| ID | Decision | Status |
|---|---|---|
| Q32 | No postcard export or separate sharing system; retain the existing simple photo mode | `REJECTED (extra feature)` |
| Q33 | Finite Continue Playing only. No endless strata or additional post-game campaign in this concept; completed play need not sustain useful spending forever | `REVISED` |
| W13 | Return through the player-made route using the jetpack and reusable lamps; preserve readable ground and conservative route warnings. No map or additional return system | `REVISED` |
| W14 | Authored buried/filled structures are allowed; the player excavates their interiors. No pre-dug rooms, caves or passage networks | `REVISED` |
| W15 | Uncover a believable buried place with history: related workshop, household and waterworks finds. Deeper impossibilities contrast with that established context | `REVISED` |
| S13 | A new run starts fresh with reshuffled arrangements of the complete required content set; no equipment, collection or completion carryover | `REVISED` |
| S14 | Ordinary falls give harmless landing feedback only; no battery cost, input lock or forced surface recovery. Geometry fault repairs remain implementation work | `REVISED` |
| S15 | Preserve value: fix duplication, duplicate credit, purchase bypasses and premature finale activation. Harmless physics comedy and free relocation of owned devices may remain | `REVISED` |
| S16 | No temporary power-ups, including timed or limited-use boosts; permanent shop upgrades and optional C4 provide power moments | `REVISED` |
| S17 | Machine power growth outpaces tougher ground: deliberate early shovel work becomes large, fast late excavation, while material responses and interesting-object recognition remain | `REVISED` |
| D16 | Expose before collecting. Interesting objects survive terrain removal/C4 and await deliberate collection after generous exposure; full-bag overflow persists and revealed uncollected targets remain detectable | `REVISED` |
| D17 | Every seed independently contains all required exhibits, ending parts and achievement-relevant finds, reachable and discoverable with baseline equipment. Sale, extraction and reload preserve discovery credit | `REVISED` |
| D18 | Major discoveries gradually reveal parts of one enormous construction. Matching visible details connect them; the final impossible object explains what they belong to. Free-form routes and flexible discovery order remain | `REVISED` |
| I17 | Resume at the saved position with the same charge, loot, terrain, displays and discovery state; no reload travel or refill | `REVISED` |
| F13 | Excavation, reveals, movement and saves preserve responsive input and visual rhythm over long altered-world sessions. Budgets are prototype measurements; optimization preserves earned state | `REVISED` |

## Revisited notes — 2026-09-15

| ID | Decision | Status |
|---|---|---|
| D19 | Consider a small fixed sale price on hover once a sellable find is exposed enough to collect. No hidden-item/detector prices, unsellable-item prices or delayed common pickups | `OPEN` |
| Q34 | Consider a short, skippable ending timelapse of this save's excavation, from untouched ground to the final hole. Before-and-after views are the simpler fallback; final staging remains open under Q31 | `DEFERRED` |
| D20 | Occasional authored containers hold a second discovery. Expose and open them in the world with the existing tool; visible contents follow normal collection and sale/display rules. No lockpicking, extra keys or inventory search; contents persist as part of the finite population | `REVISED` |
| W16 | Optional seam digging: follow visible cracks or material boundaries with the normal tool to remove a larger local section more efficiently. Broad cuts, no precision puzzle; straight-through digging always works. Upgrades increase the payoff; finds and unrelated terrain survive | `REVISED` |
| D21 | Retain physical object responses as surrounding ground is removed. Developer reports moving discoveries already implemented; this is existing reveal feedback | `REVISED` |

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
| 2026-09-14 | W05 | Legibility rule added: hard-pocket solutions must be telegraphed before commitment | One Man's Trash: invisible TNT/worm-head counterplay; concept `03` §5, anti-pattern 20 | process (user-approved) |
| 2026-09-14 | Q13 | Awe-not-dread rule added for impossible content and the deep-zone audio mix | One Man's Trash unadvertised-horror backlash; AGADAH creepy-finale split; concept `11`, `09` | process (user-approved) |
| 2026-09-14 | W13 / F13 | Prototype and release gates added for return navigation and performance feel | Meltopia lostness; Keep Digging / Meltopia / One Man's Trash performance complaints; concept `14` | process (user-approved) |
| 2026-09-14 | Q17 | Value-perception nuance flagged; price unchanged | Cross-corpus price themes (One Man's Trash, AGADAH, Meltopia) | process (user-approved) |
| 2026-09-14 | D13 | Strict prohibition of real-world political references confirmed | iDigging: buried Trump Bitcoin sparked review backlash; anti-pattern 40 | process (user-approved) |
| 2026-09-14 | D09 | Finale activation strictly gated behind component insertion, never depth/boundary triggers | iDigging: falling into void triggered ending cutscene; anti-pattern 41 | process (user-approved) |
| 2026-09-15 | I14 / F13 | Non-blocking asynchronous save serialization mandated (<100ms budget) | Digger: Galactic Treasures 15–60s system chugs on voxel saves + lack of autosave wiped hours on crash; concept 08 §7, 14 §4/§7, anti-pattern 42 | user |
| 2026-09-15 | — | Post-ending endless dig mode open question updated with positive sandbox evidence | Digger: Galactic Treasures Grandpa's Farm bonus level & 100+ layer Infinity Tunnel praised by players; concept 13 | user |
| 2026-09-15 | Q08, Q24 | Evidence flags only: calm payoff is the corpus's strongest positive theme; feature-tag honesty reinforced | Hydroneer 28,474-review analysis: relaxing/chill 94% positive; Co-op tag drove years of negative multiplayer reviews | assistant (user-requested delta) |
| 2026-09-15 | I02 / I02b | Evidence flag + new gate: first-session full loop must be completed unaided; diegetic learning validated in the prototype | Hydroneer refund-window wall: sub-2 h reviews 41.1% positive vs 86–91% after; only ~39% had sold an item in 2024 | assistant (user-requested delta) |
| 2026-09-15 | I14 | Independent rolling backup generations added; load falls back to the newest valid backup, never a silent reset | Hydroneer 2024–2026 whole-save corruption also destroyed the in-game backup (310-upvote report; community save-swap channel) | assistant (user-requested delta) |
| 2026-09-15 | I15 | Achievement eligibility from visible state only; no silent lockout flags | Hydroneer Workshop/creative lockout plus a save-flag bug that blocked honest saves (81-upvote complaint) | assistant (user-requested delta) |
| 2026-09-15 | W12, S03b, D12 | Evidence flags only: navigation legibility, late sinks, immediate novelty density | Hydroneer: carried-map annoyance, money-trivial-after-automation complaint, praise concentrated in the first hours | assistant (user-requested delta) |
| 2026-09-15 | — | Anti-patterns 43–45 added; 9/15/36/38 evidence extended; concepts 07/08/12/14/15 and open questions updated; register flags added for I04/W06; new question S15 (exploit policy) | Hydroneer delta review | assistant (user-requested delta) |
| 2026-09-15 | I05, I08, Q31, S03 | Direct additions from the follow-up idea list: haul-drop at the Sell All machine; first-launch comfort calibration; epilogue cites displayed finds; value never grows by combining; first find staged at the shaft mouth and first purchase affordable from the first sale | User-requested direct adds (Hydroneer delta follow-up) | assistant (user-requested) |
| 2026-09-15 | — | Open questions updated with seed signature sets (S13), postcard sharing (Q32), final-object candidate, exploit invariant (S15) | User-requested idea logging | assistant (user-requested) |
| 2026-09-15 | — | Pruned other-game bug/marketing citations from the register and concept set per developer preference; removed anti-pattern 43 (feature-tag honesty) and the bug-only flags on Q24/I14/W06; game-relevant rules retained (backups, achievement eligibility, exploit invariant, onboarding gate) | Developer feedback | assistant (user-requested) |
| 2026-09-15 | Q24 | No-co-op decision re-opened for decisioning (status `DISCUSSING`) | Persistent co-op praise and requests across the review corpora (Keep Digging's #1 praised feature; AGADAH, The Spotter, Hydroneer couch co-op) | assistant (user-requested) |
| 2026-09-15 | — | Inline evidence flags reworded to game/player-feedback style; dates removed from flags | Developer preference | assistant (user-requested) |
| 2026-09-15 | — | Ore Factory Squad delta: anti-patterns 46–47 added; evidence extended on 3/4/15/19/34; flags added on Q08/Q17/Q24/S03b/S08/S09/I02/I05/I11/A01/F05; open questions W01/F07/D03/S15 updated; prototype checks added for tool-tier regressions and C4 payback | `RESEARCH/ORE_FACTORY_SQUAD_REVIEW_ANALYSIS.md` | assistant (user-requested) |
| 2026-09-15 | D15 | Added: uniques exist exactly once — no duplicates; commons get no presentation effort; distinctives stay the special repeatable tier | Developer playthrough: duplicate uniques and item-inspection fatigue in One Man's Trash | user (playthrough) |
| 2026-09-15 | D10, W03, D14 | Nuances logged: large finds must deliver the whole object; darkness ramps gradually and never outpaces readability; unique stories never require inspecting commons | Developer playthrough: partial-collectible car letdown; "got dark too quickly"; item-popup and inspection annoyance | user (playthrough) |
| 2026-09-15 | S16, W14 | New open questions: timed/temporary power-ups; non-cave underground structures | Developer playthrough: liked timed boosts but unsure whether the boring game flattered them; unsure whether generated non-cave passages fit the direction; corpus silent on both | user (playthrough) |
| 2026-09-15 | — | Anti-patterns 48–50 added (no gambling; no hard depth walls forcing in-area grinding; no in-game task checklists); anti-pattern 11 evidence extended with upkeep/overheating | Developer playthrough (One Man's Trash): gambling hard no; early depth blocker; checkbox achievements; overheating annoyance | user (playthrough) |
| 2026-09-15 | Q06, Q11, Q22b, Q25, Q28, S06, S07, S11, I04, I05, I11, D11, F05, F06, A01 | Confirmed only — no rule change: no characters/faces, ambience-only audio and custom cohesive art, one difficulty, detector never targets commons, jetpack core, legible upgrades, no fall damage, quick sell-then-upgrade flow, no clocks, display collecting, satisfying dig feel | Developer playthrough aligns with existing register and corpus | user (playthrough) |
| 2026-09-15 | Q28, S14 | Answer 1: Harmless ordinary falls; no battery cost or forced return | Experimenting in the player-made hole should not cost progress | user |
| 2026-09-15 | Q26, S04 | Answer 2: Keep loot-safe recovery fee and interest-free debt; protect basic refill income | Recovery has a consequence without trapping a broke player | user |
| 2026-09-15 | Q27, W12, W13 | Answer 3: Jetpack and reusable lamps; never a map | The developer expects a compact vertical hole to be easy to leave | user |
| 2026-09-15 | W03, F09 | Answer 4: Ground/object shapes always readable; lamps add detail/color | Darkness supports atmosphere while preserving recognition | user |
| 2026-09-15 | S09, F12 | Answer 5: Automatic material-specific behavior through the final tier | Preserve distinct digging feel as the same machine grows | user |
| 2026-09-15 | S02 | Answer 6: Fewer stronger upgrades; each affects the next outing | Tiny invisible gains weaken the purchase reward | user |
| 2026-09-15 | D03 | Answer 7: After research: ordinary/repeatable finds sell; special exhibits and keys are unsellable; no first-copy routing | Effortless Sell All with a clear purpose for each type | user |
| 2026-09-15 | D11, W08b | Answer 8: After research: individual placement for a few special exhibits, not routine rocks; no rarity-display system selected | Visible collections matter; repeated handling can become a chore | user |
| 2026-09-15 | D14 | Answer 9: Story through the object before pickup/placement or at display; no inventory reading; timing remained open | The developer expects players to stay in the world | user |
| 2026-09-15 | D15 | Answer 10: Commons visible before auto-pickup; developer reports this already works in the demo | Keep the implemented recognition feedback; no inspection chore | user |
| 2026-09-15 | S05b, I04 | Answer 11: No discarding; full-bag finds stay in the world | Avoid inventory management and lost finds | user |
| 2026-09-15 | D05, S10 | Answer 12: Uniques reward display/story only, no mechanical perks | Discovery and collection are their reward | user |
| 2026-09-15 | F07, I01 | Answer 13: Tool reaction plus subtle edge direction cue | Connect feedback to the machine while keeping direction readable | user |
| 2026-09-15 | S06 | Answer 14: Keep a nearby detector target until collection or moving away | Stable feedback supports finishing a reveal | user |
| 2026-09-15 | W05 | Answer 15: Early tool always makes visible progress; upgrades/C4 accelerate hard pockets | Preserve dig-anywhere freedom without mandatory grind walls | user |
| 2026-09-15 | W14 | Answer 16: Buried walls, machinery and filled structures; player excavates the interiors | Larger discoveries preserve the player-made hole | user |
| 2026-09-15 | S08, D16 | Answer 17: C4 clears ground; interesting finds remain for deliberate collection | Powerful blasts must not erase recognition | user |
| 2026-09-15 | D10 | Answer 18: Short local large-object extraction then whole-object surface transfer | A major find should not demand a car-wide shaft to the sky | user |
| 2026-09-15 | S03 | Answer 19: Fixed price per type; deeper zones contain richer types/mixes | A gold bar is the same price at every depth | user |
| 2026-09-15 | S10 | Answer 20: All permanent power from existing shop tracks; no found passives | Keep progression clear and independent of lucky upgrade drops | user |
| 2026-09-15 | S16 | Answer 21: No temporary boosts | Use satisfying base digging, permanent upgrades and C4 | user |
| 2026-09-15 | S12, Q33 | Answer 22: Finite Continue Playing; spending can end after completion | A 3–5 h game can have a satisfying stopping point | user |
| 2026-09-15 | Q18, S13 | Answer 23: Fresh progression per seed, complete content set in each | Replay changes the hole without requiring repeat runs | user |
| 2026-09-15 | Q32, I13 | Answer 24: Drop the extra postcard/sharing proposal; existing photo mode not removed | The developer sees no need for another sharing feature | user |
| 2026-09-15 | D11 | Answer 25: Store special finds safely; handle them physically at the display | Keep the placement moment without underground carrying | user |
| 2026-09-15 | D11, D11b | Answer 26: Choose any compatible display space; snap placement | A small choice makes the collection personal | user |
| 2026-09-15 | D14 | Answer 27: First story trigger deferred to play; lean before placement; display inspection/rereading required | Judge timing in context and preserve later access to the story | user |
| 2026-09-15 | I04 | Answer 28: Remove the inventory screen | Chosen selling, collection and inspection already work in-world | user |
| 2026-09-15 | D04, D09, D17 | Answer 29: Authored related-object trails and existing detector lead to required finds | Avoid a blind hunt for the last missing part | user |
| 2026-09-15 | D09 | Answer 30: Insert any owned parts in one interaction; missing sockets remain visible | Show partial progress without requiring separate return trips | user |
| 2026-09-15 | P05 | Answer 31: 100% = ending, special exhibits placed, upgrades maxed, zones reached; Steam separate | Completion belongs to this save, never terrain coverage | user |
| 2026-09-15 | Q31 | Answer 32: One ending personalized by actual discoveries | The excavation matters without alternate-outcome hunting | user |
| 2026-09-15 | Q12 | Answer 33: Keep exact final object open until the digging loop works | The payoff needs visual and play validation | user |
| 2026-09-15 | I17 | Answer 34: Reload at saved position with unchanged charge and loot | Continue the interrupted expedition without a free return | user |
| 2026-09-15 | — | Answer 35: Skipped: no Unstuck feature adopted into the concept | Developer rejects implementation-detail questions in concept discussion | user |
| 2026-09-15 | I12 | Answer 36: Skipped: no new text-scaling requirement; I12 stays deferred | Settings scope is not a concept-level decision | user |
| 2026-09-15 | W15 | Answer 37: Uncover a coherent buried place and history | Related finds motivate lateral digging and establish believable context | user |
| 2026-09-15 | S17 | Answer 38: Power growth outpaces tougher ground | The machine changes the scale of play, not only its appearance | user |
| 2026-09-15 | D18 | Answer 39: Major discoveries connect into one enormous construction | The final object gives earlier discoveries meaning and resolves growing curiosity | user |
| 2026-09-15 | Q26, Q29, S04, S07, W03, W06, S05b, D16 | Apply recovery, refill, reusable-light and overflow clarifications | One charge per recovery, a viable next outing, honest route feedback and preserved finds | assistant (delegated by user) |
| 2026-09-15 | S01, S02, S03, S03b, S15, I05 | Apply meaningful purchase, nonblocking sale/upgrade and value-preservation clarifications | Keep money tied to useful play and distinguish convenience from duplicated value | assistant (delegated by user) |
| 2026-09-15 | W01, W04, W09, D04, D06, D08, D12, D17 | Apply coherent generation, complete-seed guarantees and five-group material prototype direction | Validate relationships, partial recognition and novelty instead of multiplying similar content | assistant (delegated by user) |
| 2026-09-15 | I02, I03, I08, I10, F10, F13 | Apply bounded onboarding/menu/style clarifications and resolve existing comfort/feel contradictions | Minor review improvements delegated by the developer; no new settings questionnaire or Unstuck feature | assistant (delegated by user) |
| 2026-09-15 | Q31, W15, S17, D18 | Add recurring construction detail, familiar-ground upgrade payoff, intact object, lamp appearances, haul reaction, seed arrangements and personal clipping | Small suggestions reinforce the selected world, power and mystery arc | assistant (delegated by user) |
| 2026-09-15 | — | Process the complete review; retain intentional deferrals and skip superseded proposals; remove CONCEPT_REVIEW.md after verification | Developer authorizes minor/medium changes without more questions; no unresolved major concept change found | assistant (delegated by user) |
| 2026-09-15 | D19 | Record the developer's price-on-hover note as an open candidate; recommend a small price after exposure | Anticipation of a good sale may reinforce discovery without an inventory or inspection chore | user idea; assistant recommendation |
| 2026-09-15 | Q26, S04 | Reaffirm: zero fuel in the yard leaves the player at zero; no rescue or automatic refill | The player is already safe and can walk to sell or refuel; this clarifies the existing rule | user note; assistant clarification |
| 2026-09-15 | Q34, Q31 | Record the developer's world-change timelapse as a deferred candidate for the existing ending montage | Show the player's own work and the scale of change; before-and-after views can provide a simpler payoff | user idea; assistant recommendation |
| 2026-09-15 | D20 | Adopt finds inside finds: selected containers reveal visible, persistent contents using the existing tool | One discovery creates another moment of curiosity and reinforces the buried scene | user |
| 2026-09-15 | W16 | Adopt optional seam digging with broad, efficient local cuts and normal straight-through digging preserved | Choosing where to cut adds satisfying agency without another tool or a required technique | user |
| 2026-09-15 | D21 | Record the developer's report that moving discoveries are already implemented | Preserve existing physical reveal feedback rather than treating it as new work | user (implementation report) |

<details>
<summary>Superseded wording — 2026-09-15</summary>

Prior rows are retained for history. The unstruck rows above are current.

| ID | Previous decision | Previous status |
|---|---|---|
| ~~Q10~~ | ~~Light slow-build mystery (evidence: hidden finds and unsolved oddities are among the most-praised elements in digging-game reviews, while forced story chores are among the most resented — the trail stays discovery-driven, optional and rewarded by the finds themselves; concept `11` §1)~~ | ~~`CONFIRMED`~~ |
| ~~Q12~~ | ~~Final discovery: a modern object built in impossibly ancient materials~~ | ~~`REVISED`~~ |
| ~~Q18~~ | ~~Per-save randomized world; display per-save; no meta progression (evidence: Keep Digging players widely praised the gear-carrying reset; second-run identity logged as S13)~~ | ~~`CONFIRMED`~~ |
| ~~Q24~~ | ~~No co-op; save format stays future-proof (evidence: co-op is Keep Digging's most-praised feature, one of the most-requested additions in AGADAH and The Spotter, and a genuine couch highlight for Hydroneer players; Ore Factory Squad's co-op is its most-praised mode while its top negative reviews are solo players fighting timers and workloads built for groups — demand is persistent across games, so this is **re-opened for decisioning**; any outcome keeps the solo loop complete on its own; social hook tracked as Q32)~~ | ~~`DISCUSSING`~~ |
| ~~Q26~~ | ~~Recovery keeps all loot; depth-scaled fee + interest-free auto-debt; auto-trigger at 0 fuel (evidence: losing collected loot or progress is the most trust-destroying theme in digging-game reviews — failure costing only time and a fee is strongly supported)~~ | ~~`CONFIRMED`~~ |
| ~~Q27~~ | ~~No return aids; vertical return only; keep the return-power warning (evidence: getting lost is one of Meltopia's top complaints; Keep Digging players climbed badly enough to use save-exit as an elevator; One Man's Trash players praised terrain repack; see W13)~~ | ~~`REVISED`~~ |
| ~~Q28~~ | ~~No health bar; falls stagger + knock battery; extreme falls trigger recovery (evidence: Keep Digging players praised no fall damage and disliked the patch that added fall death; severity re-opened as S14)~~ | ~~`CONFIRMED`~~ |
| ~~Q29~~ | ~~Shared dig + jetpack battery~~ | ~~`CONFIRMED`~~ |
| ~~Q31~~ | ~~Ending fame shown diegetically: a media wall (news clippings, radio, TV) accumulates in the yard after the discovery; no characters, no dialogue (evidence: Hydroneer players found its ending disconnected from their run — the reports cite the player's actual displayed finds and depths so the epilogue pays off this hole; concept `11` §5)~~ | ~~`CONFIRMED`~~ |
| ~~W01~~ | ~~Site depth at least 100 m (exact depth and footprint set by feel in playtest)~~ | ~~`CONFIRMED (depth floor) / OPEN (size)`~~ |
| ~~W03~~ | ~~No personal light; open-shaft sky light + dim ambient floor; placeable lamps for real visibility; never pitch black (evidence: developer playthrough — darkness must ramp gradually and never outpace readability or lamp access)~~ | ~~`CONFIRMED`~~ |
| ~~W04~~ | ~~Four depth zones with changing ground, minerals and mood; exact material list TBD~~ | ~~`DEFERRED`~~ |
| ~~W05~~ | ~~Rare optional hard pockets (concrete plug, river-rock lens, gravel shelf); multiple solutions; no specific-upgrade gating (evidence: One Man's Trash's TNT/worm counterplay existed but was invisible to players — reviewers concluded there was no counterplay; pocket solutions must be legible before commitment; concept `03` §5)~~ | ~~`CONFIRMED`~~ |
| ~~W06~~ | ~~Full voxel free-form terrain; tunnels/overhangs; disconnected valuable voxels auto-collect, plain dirt vanishes; debris visual-only~~ | ~~`CONFIRMED`~~ |
| ~~W08b~~ | ~~Display: predefined outlines; empty frames visible, shapes hidden; player places finds into waiting spots~~ | ~~`CONFIRMED`~~ |
| ~~W09~~ | ~~Validated random placement; authored depth ranges; population persists per save~~ | ~~`CONFIRMED`~~ |
| ~~W12~~ | ~~No map; depth readout, display and detector direction handle memory (evidence: Hydroneer players repeatedly complained that the map was a physical object they had to carry; the requirement is legible navigation, not a map widget; see W13)~~ | ~~`CONFIRMED`~~ |
| ~~S01~~ | ~~Tracks: Tool, Battery, Jetpack, Inventory, Detector + small C4 track~~ | ~~`CONFIRMED`~~ |
| ~~S02~~ | ~~Levels: many small increments with a major capability change roughly every third level (the 30–45 min purchase cadence measures these milestones, not every level); count flexible; visuals escalate~~ | ~~`CONFIRMED`~~ |
| ~~S03~~ | ~~Money-only progression; late sinks exist; value never grows by combining (concept `06` §8)~~ | ~~`CONFIRMED`~~ |
| ~~S03b~~ | ~~Late sinks: extra charges, lamps, display upgrades, cosmetics, conveniences (evidence: "the game is over once the setup runs itself" / money becomes pointless is Hydroneer's most repeated long-term complaint — late sinks plus final-purchase timing are the answer inside a 3–5 h run; Ore Factory Squad's level cap with nothing left to buy or chase is its most common endgame complaint — visible post-max goals are the direct answer)~~ | ~~`CONFIRMED`~~ |
| ~~S04~~ | ~~Shared battery; paid surface refill (full/partial); drain only on powered actions; safe/risky/critical warning; bigger tank keeps current fuel (evidence: upkeep mechanics that interrupt digging — stamina, commutes, maintenance — are among the most-resisted features in digging-game reviews; drain only on powered actions is the right line)~~ | ~~`CONFIRMED`~~ |
| ~~S05b~~ | ~~Hard stop when full; finds stay in the world; uniques/key items never blocked; nothing deleted~~ | ~~`CONFIRMED`~~ |
| ~~S06~~ | ~~Detector: range/clarity/direction upgrades; never value or rarity; visual cues; one target; quiet intervals~~ | ~~`CONFIRMED`~~ |
| ~~S07~~ | ~~Jetpack: stable from the start; upgrades only improve (speed, efficiency, altitude, assists); control never degrades~~ | ~~`CONFIRMED`~~ |
| ~~S08~~ | ~~C4: thrown in multiples, stick where they land, remote detonation; powerful; costs money; optional accelerator (evidence: Ore Factory Squad's paid explosives were ignored because the blast did not justify the price — a charge must clearly beat digging time for its cost; "properly powerful" is a prototype gate)~~ | ~~`CONFIRMED`~~ |
| ~~S09~~ | ~~Tool: automatic material adaptation; no manual switching; converges late; exact late behavior validated in playtest (evidence: Ore Factory Squad's tool tiers read as "more or less the same" and its upgraded jackhammer was worse in ground the shovel already cleared — adaptation must show distinct, felt behavior per material)~~ | ~~`CONFIRMED (provisional)`~~ |
| ~~S10~~ | ~~Passive upgrades: deprioritized until playfeel review; find-or-buy still the leading option; passive/unique effects must preserve challenge (no sudden power spikes)~~ | ~~`DEFERRED`~~ |
| ~~S12~~ | ~~Post-ending: full Continue Playing; economy live; achievements on the same save~~ | ~~`CONFIRMED`~~ |
| ~~D03~~ | ~~Find purpose: no keep/sell choice; each type has one fixed purpose; distinctive purpose TBD after research~~ | ~~`DEFERRED`~~ |
| ~~D04~~ | ~~Detector targets: distinctive + unique only; some distinctives silent by design; size/metal/price never decide~~ | ~~`CONFIRMED`~~ |
| ~~D05~~ | ~~Value: 4 bands — common income, distinctive value, rare (several expeditions), unique (effect)~~ | ~~`CONFIRMED`~~ |
| ~~D06~~ | ~~Clusters: 5 authored micro-scene templates, rotated/placed procedurally~~ | ~~`CONFIRMED`~~ |
| ~~D08~~ | ~~Mystery: 3-step escalation (anachronistic junk → too-correct objects → constructed impossibilities)~~ | ~~`CONFIRMED`~~ |
| ~~D09~~ | ~~Ending components: 3–4, never lost, no slots, no puzzle, obvious insertion (evidence: iDigging players reached the credits in 8–20 min by falling through collision into the ending trigger — the finale stays behind intentional component insertion; anti-pattern 41)~~ | ~~`CONFIRMED`~~ |
| ~~D10~~ | ~~Large discoveries: a few per run; excavated then cable-yanked; some may stay (evidence: developer playthrough — extraction must deliver the whole object; a token part of a large find reads as a letdown)~~ | ~~`CONFIRMED`~~ |
| ~~D11~~ | ~~Display form: growing wall/shelf with predefined outlines; no player choice of placement~~ | ~~`CONFIRMED`~~ |
| ~~D11b~~ | ~~Empty display frames visible; item shapes hidden until discovered~~ | ~~`CONFIRMED`~~ |
| ~~D12~~ | ~~Pacing: guaranteed early find; bounded dry spells; one major-scale find per zone; new silhouettes to the end (evidence: Hydroneer's praise concentrates in its early hours while its negatives concentrate in the first two — novelty density starts immediately; first find ≤10 min is a prototype gate, `14` §4)~~ | ~~`CONFIRMED`~~ |
| ~~D14~~ | ~~Uniques carry a one-sentence story; delivery trigger (pickup vs inspection) still open (evidence: developer playthrough — inspection must never be required for commons; pickup delivery with optional inspection fits)~~ | ~~`CONFIRMED (trigger OPEN)`~~ |
| ~~D15~~ | ~~Uniques exist exactly once in the world — never in multiples; common finds get no presentation effort; distinctives are the special, repeatable middle tier~~ | ~~`CONFIRMED`~~ |
| ~~I01~~ | ~~HUD minimal: depth, bag count/capacity, battery, return warning; detector feedback diegetic~~ | ~~`CONFIRMED`~~ |
| ~~I02~~ | ~~No tutorial (evidence: Hydroneer's hands-off onboarding is a "refund-window wall" — short-session reviews reject it while later ones turn positive, and many players never find the first sale; Ore Factory Squad's forced tutorial could not be skipped or saved through and drew restarts, while its unexplained systems sent players searching for guides — no tutorial, but every system must teach itself in-world; diegetic learning carries a first-session full-loop gate; concept `07` §2 / `14` §4)~~ | ~~`REVISED`~~ |
| ~~I03~~ | ~~Pause menu: direction Resume / New Game / Settings / Exit; exact tabs later~~ | ~~`DEFERRED`~~ |
| ~~I04~~ | ~~Inventory: inspect-only grid; no stats/equipping/sorting; selling only at the machine (evidence: physical one-item-at-a-time handling is Hydroneer's biggest complaint — the abstract bag avoids it; concept `05` §9)~~ | ~~`CONFIRMED`~~ |
| ~~I05~~ | ~~Selling: one-button Sell All with physical animation; individual selling available there (evidence: players love hands-on physicality but hate carrying — the tactile payoff belongs at the machine, once; Ore Factory Squad's praised forklift/pallet physicality was bypassed by players the moment it became manual labor; the haul leaves the bag as one animated pile at the machine; concept `07` §3)~~ | ~~`CONFIRMED`~~ |
| ~~I08~~ | ~~Motion comfort: FOV slider, shake 0–100% (low default), head bob toggle, comfort preset, no forced roll; settings persist (evidence: motion-sickness complaints recur across digging-game reviews — a first-launch comfort calibration preview is added; concept `10` §1)~~ | ~~`CONFIRMED`~~ |
| ~~I10~~ | ~~Motor access: auto-dig assist, toggle holds, one-hand presets, no mashing/QTEs, generous buffering~~ | ~~`CONFIRMED`~~ |
| ~~F07~~ | ~~Detector presentation: deferred; options documented (hybrid / edge indicator / tool reaction)~~ | ~~`DEFERRED`~~ |
| ~~F09~~ | ~~Lighting moods per zone: warm daylight → cool dim → near-black deep; lamps make readable pools~~ | ~~`CONFIRMED`~~ |
| ~~F10~~ | ~~UI art style: clear, not retro; exact style later~~ | ~~`DEFERRED`~~ |
| ~~P05~~ | ~~Completion: credits + display outlines + all upgrades + zone stats; never 100% terrain~~ | ~~`CONFIRMED`~~ |

</details>


<details>
<summary>Complete review disposition — 2026-09-15</summary>

All sections of the former `CONCEPT_REVIEW.md` were processed before deletion. C/M numbers below
are that review's finding labels, not decision IDs. Developer answers override its recommendations.

| Review items | Disposition |
|---|---|
| Critiques C01–C04 | Recovery/refill fairness, return wording, open descent and fixed item prices aligned in Q26–Q29, W05, W12–W13 and S03–S04. No reopening maps |
| Critiques C05–C08 | Adaptive final tool, meaningful upgrades, safe overflow and visible-before-pickup rules aligned in S02, S09, S17, W06, D15–D16 |
| Critiques C09–C10 | Replaced first-copy routing, inventory stories and unique effects with the chosen sell/display roles; no passives or display paydays |
| Critiques C11–C12 | Complete seeds and required-find trails adopted; local whole-object extraction replaces a required transport shaft |
| Critiques C13–C16 | Reusable light, finite economy, automatic component ownership and visual mystery continuity adopted; exact final object remains deferred |
| Critiques C17–C20 | Action-only battery, consistent existing comfort rules, current-save completion and staged prototype validation applied; no new settings/Unstuck requirements |
| Critiques C21–C24 | Repaired certainty and IDs; one guaranteed major per zone; no unsupported OFS popup claim, universal boost verdict, value/refund inference or reopened co-op question |
| Improvements M01–M08 | Applied; M03's Unstuck button omitted as outside concept scope. Ordinary fall and state-preservation rules remain |
| Improvement M09 | Superseded: all repeatable valuables sell; special exhibits place individually in compatible spots. No first-copy reservation or batch placement |
| Improvement M10 | Superseded: no inventory screen or unique perks; first story timing remains for playtesting, with display rereading required |
| Improvements M11–M16 | Applied with current choices: complete seeds, extraction, reusable lamps, finite completion, convenient finale and current-save credit |
| Improvement M17 | Existing comfort/onboarding contradictions resolved. Text-scaling/screen-reader scope stays deferred after skipped question 36 |
| Improvement M18 | Applied; common visibility is attributed to the developer's demo report. Save implementation is not represented as verified |
| Suggestion 1: recurring construction detail | Added to the connected major discoveries and finale (D08, D18) |
| Suggestion 2: new attachment on familiar ground | Added as a natural upgrade payoff, not a mandatory demo (S02, S17) |
| Suggestion 3: intact object in extraordinary sediment | Added as a visual mystery example, not a roster commitment |
| Suggestion 4: lamp-lit memories | Reusable/repositionable lamps and a few equal-utility cosmetic appearances fit the existing yard |
| Suggestion 5: haul-specific sale reaction | Added to the existing nonblocking sale animation (I05) |
| Suggestion 6: seed personality through arrangement | Added within complete-content and construction-relationship constraints (W09, S13) |
| Suggestion 7: personal clipping | Added to the chosen one-ending media wall (Q31) |
| Suggestion 8: local postcard | Rejected by answer 24 (Q32); ordinary photo mode remains |

### All 28 original open-question rows

| Original row | Outcome |
|---|---|
| 01 — distinctive purpose | Sell repeatables; a small separate unsellable exhibit set; D03 |
| 02 — story trigger | Still deferred in play, leaning before placement; display rereading required; D14 |
| 03 — passive upgrades | No found passives; power comes from existing shop tracks; S10 |
| 04 — late tool | Keep automatic adaptation; S09 |
| 05 — social hooks | No extra sharing feature; Q32 |
| 06 — second run | Fresh equipment and collection, complete content per seed; S13 |
| 07 — falls | Harmless ordinary landing; Q28, S14 |
| 08 — exploits | Preserve value, allow harmless comedy and owned-device relocation; S15 |
| 09 — temporary boosts | None, including limited-use boosts; S16 |
| 10 — rosters | Counts retained; exact lists follow the five-object slice; deferred |
| 11 — final purchase timing | Worthwhile play must remain; percentage/cadence still prototype hypotheses |
| 12 — zone names | Descriptive placeholders retained; final names deferred |
| 13 — endless post-game | Finite Continue Playing only; Q33 |
| 14 — footprint | Compact and vertical with lateral room; at least 100 m; exact dimensions deferred |
| 15 — materials | Five response groups for initial tests; final roster deferred; W04 |
| 16 — voxel/chunk size | Deferred to recognition/feel/travel tests; separate cut scale from streamed-region size |
| 17 — detector presentation | Silent tool reaction plus broad edge cue; F07 |
| 18 — UI art | Industrial-worksite direction adopted; final treatment later; F10 |
| 19 — return navigation | Jetpack and reusable lamps, never a map or added return system; W13 |
| 20 — buried structures | Filled authored structures; player creates all openings; W14 |
| 21 — performance feel | Preserve input/reveal rhythm; budgets remain prototype work; F13 |
| 22 — pause menu | Bounded menu direction applied under delegated minor cleanup; I03 |
| 23 — text scale/screen reader | Question 36 skipped; I12 remains deferred, no new concept requirement |
| 24 — reload position | Saved position and state; I17 |
| 25 — ending staging | One personal, pausable/skippable ending; Q31 |
| 26 — final object | Direction retained; exact identity deliberately deferred; Q12 |
| 27 — achievements | Candidate themes retained; final 5–10 follow validated content |
| 28 — exact values | Deferred to combined loop testing, not decided from review counts |

### All decision proposals and repairs

- All 35 existing-row flags processed. Applied or clarified except where superseded: Q27 cannot
  reopen maps; D03/D11/I04 first-copy, assigned-slot, batch-placement and inventory proposals are
  replaced by the user's choices; D05 has no unique perks; D14 timing remains open; I12 stays deferred.
  I09's existing captions remain required without a new feature decision.
- All 13 proposed rows processed: Q32 rejected; Q33, S13–S16, W13–W14, F13, I17, D16–D17 adopted
  with the user's corrections. I18 (Unstuck) omitted as an implementation question, not silently accepted.
- All six repair bullets processed: obsolete IDs repaired; major-find guarantee aligned; working
  options labeled; evidence attribution corrected; demo/save claims qualified; locked content counts
  retained. User decisions settle several formerly open options instead of perpetually labeling them provisional.
- Parked business/production topics remain parked. No unresolved major proposal required another question.

### Research behind the display choice

The follow-up used qualitative examples, not a representative preference survey:
[One Man's Trash raw reviews](../RESEARCH/research_data/one_mans_trash_reviews_raw.json)
(entries 169 and 221) praise visible collections;
[Meltopia raw reviews](../RESEARCH/research_data/meltopia_reviews_raw.json)
(766 and 910) request meaning at placement and criticize prescribed pedestal placement respectively.
A [Treasure Hunter Simulator review](https://steamcommunity.com/id/kschang77/recommended/748300)
criticizes individual minor-item sales and repeated identification; a
[player discussion](https://steamcommunity.com/app/748300/discussions/0/1639788130288374561/)
shows uncertainty over what is safe to sell.
[Fossil Corner reviews](https://steamcommunity.com/app/1587710/reviews/?browsefilter=toprated)
provide adjacent support for arranging special displays.
The developer adopted effortless ordinary sales and a few personally placed exhibits; this is a
design choice informed by those examples, not a claim that every player wants manual placement.

</details>
