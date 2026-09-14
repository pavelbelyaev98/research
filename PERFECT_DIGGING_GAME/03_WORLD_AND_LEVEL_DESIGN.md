# 03 — World and Level Design

## 1. The three scales

The underground is designed at three scales simultaneously:

1. **Macro (the layer):** 7 depth bands, each with its own palette, material set, music, hazards
   (optional), landmark family and economy. Layers prevent the "identical tunnels" problem that
   made `[MELT]`'s back half an endurance test `[MELT]` "all the corridors are identical".
2. **Meso (the route):** the player's own tunnels + checkpoints + fast travel. This is where the map
   and readability live (see `12_UI_AND_UX.md`).
3. **Micro (the voxel):** digging feedback, material splintering, ore glow, cave-ins that are
   cosmetic-only (no damage — see `07`).

## 2. Surface hub (the backyard)

A compact, warm, readable hub that grows with the player. Surface is a *save-haven*: no danger, no
timers, no fail state, ever.

| Station | Function | Lesson |
|---|---|---|
| The Hole | The entrance; physically widens/collapses as you dig | `[AGADH]`'s hole is the whole game |
| Shop (trader NPC) | Sell all, buy upgrades, unlock tools | `[MELT]` `[KD]` loop; sell-all from minute one |
| Workshop | Upgrade trees, respec (free), tool skins | `[OMT]` cosmetic-only skins complaint solved: skins are flavor, function is upgrades |
| Map table | Full map, fog-of-war, markers, notes | Direct fix for `[MELT]`/`[SPOT]` no-map complaints |
| Museum / pedestals | Artifacts, fossils, lore, passive QoL rewards | `[MELT]` artifacts did nothing — here they always give something (lore + small perk) |
| Garage | Traversal vehicles/fast travel board | `[SPOT]` car was poorly received; here a simple, polished elevator/lift |
| Job board | Optional contracts, daily-seeded bounties | Gives endgame structure `[SPOT]` lacked |
| Radio / letters | Story delivery, patch notes in-fiction | `[MELT]` "no lore, just dig" complaint |

Hub stations are all within ~20 seconds' walk (no traversal tax). The hub is upgraded visually as
milestones complete — a tangible "you are building something" feeling `[MELT]` stove/hub praise.

## 3. Layer plan (macro)

| # | Layer | Depth | Material identity | Landmark family | Gate to next layer | Optional danger (Standard+) |
|---|---|---|---|---|---|---|
| 1 | Backyard Soil | 0–150 m | Dirt, roots, clay | Old well, buried shed, mole tunnels (friendly) | — | None |
| 2 | Stone & Caves | 150–350 m | Stone, coal, iron, geodes | Natural caves, abandoned mine camp | Sealed mine door (key in cave POI) | Cave slimes (opt-in) |
| 3 | Ruins | 350–650 m | Brick, copper, silver, amber | Buried village, temple, catacombs | Glyph door (3 glyph fragments) | Guardian statues (opt-in, avoidable) |
| 4 | The Flooded Works | 650–950 m | Wet rock, gold, amethyst | Pump station, sunken rail, drowned market | Pump control (2 side valves) | Blind fish (opt-in, non-lethal) |
| 5 | Crystal Reach | 950–1,300 m | Crystal, sapphire, emerald, ruby | Crystal cathedral, prism cavern | Resonance key (found in cathedral) | Crystal crawlers (opt-in) |
| 6 | The Deep Forge | 1,300–1,650 m | Obsidian, uranium, adamant | Forge city, magma tubes | Forge sigil (quest chain) | Heat vents (environmental, fair) |
| 7 | The Hollow / Core | 1,650–2,000 m | Corestone, prism, unique | Precursor engine, the Final Descent | Finale | Opt-in boss den only |

Design rules:

- **Every 30–60 seconds of digging**: either a material change, a sound cue, a cave opening, or a
  landmark silhouette. `[SPOT]`'s underground is praised precisely for this density.
- **Every layer teaches then tests**: introduce a mechanic safely (tutorialized POI), then place a
  version that demands it.
- **Layer identity is instantly readable** by color, ambient audio, particle type and HUD accent.
  This also fixes `[KD]`'s "blurry, dark, unreadable" complaints.

## 4. Handcrafted vs. procedural

The right answer is neither pure. `[KD]`/`[OMT]` shipped fixed maps and got "no replay value" and
"every playthrough is the same" `[KD]` "no randomization of the level". `[SPOT]` shipped a fixed
hand-made map and got "best underground ever" *and* "no replay value". So:

- **Skeleton: procedural, seeded.** Layer topology, cave shapes and ore distribution are generated
  from a fixed world seed so every player's yard differs, but the *critical path and landmarks are
  deterministic*.
- **Landmarks: 100% handcrafted.** ~60–80 POIs authored by level designers, placed by rules
  (layer, spacing, gate logic). This keeps quality high and production bounded.
- **Blend rule:** proc-gen may never place a landmark in a way that is unfair, unreadable, or
  blocks a gate; hand-placed "keystones" always override.
- **Endless/Creative mode** uses a second seedable generator with all landmark families unlocked.
- **Daily seeded runs** (Endless) give replay value without roguelike FOMO.

## 5. Anti-straight-down gating (spatial rules)

Implemented via terrain, not friction (see `02_CORE_LOOP_AND_PROGRESSION.md` §4):

1. **Seal bands.** A horizontal barrier of "sealed bedrock" every layer boundary. Diggable only
   after a circuit is opened with a key/item/code from that layer's landmarks. Visually obvious and
   diegetic (mine door, glyph, valve, sigil).
2. **Vein offset.** High-value veins spawn 15–60 m laterally from the main shaft with visible
   "hint" particles on the shaft wall (glittering seam), so explorers get rich.
3. **Checkpoint economy.** Fast travel anchors are at landmarks; activating them reveals the local
   map sector. A straight-down player travels blind and slow.
4. **Structural rewards.** Tools, cosmetics, lore and museum slots are in POIs, not on the shaft.
5. **Speedrun honesty.** A "direct descent" route exists for speedrunners who want it; the game
   tracks and celebrates both "shaft-only" and "full excavation" playthroughs as separate stats.

## 6. Map and readability data model

The map is a first-class system, not a UI afterthought (the missing map is a top-2 complaint in
`[MELT]` and a top-5 in `[SPOT]`):

- **Fog of war** tuned to player vision, not global reveal.
- **Layers/legend:** ever-visited tunnel = solid line; current session's dig = bright; ore veins
  (if scanned) = colored; POIs = icons; gates = lock icons; unopened branches = dashed hints.
- **Scan tool** (unlocked early): pings resources/POIs within radius, marks them on the map for the
  session; upgraded scan radius is a money sink.
- **Personal markers:** placeable pins + labels, plus auto-notes ("better ore below").
- **"Have I checked this?" answer:** every tunnel dead-end gets a subtle map tick once physically
  visited within X meters; unvisited dead ends show as unticked.
- **Surface map** and **underground map** are one continuous view with a layer filter.

## 7. Secrets and collectibles placement

- **Rule of curiosity:** any suspicious visual (glow, crack, different brick, bird sound above
  ground) must lead to a real payoff. No fake leads, ever.
- **Secret tiers:** (1) ore caches, (2) lore notes/recordings, (3) fossils, (4) artifact set pieces,
  (5) tool/perk unlocks, (6) cosmetic vaults, (7) the unique Finale key items.
- **No missable critical items:** if a key is required for a gate, it cannot be permanently lost;
  it respawns at its POI after a reload and is marked on the map once its layer is "revealed".
- **No RNG-only collectibles:** every collectible has a deterministic location rule; the seed
  changes location, not existence. `[SPOT]`'s bugged "find every pizza" achievements are the
  cautionary tale.

## 8. Landmark spacing and budget

| Metric | Target |
|---|---|
| Handcrafted POIs at 1.0 | 70 (10 per layer) |
| Unique interior "set piece" rooms | 24 |
| Lore notes / recordings | 90 |
| Fossils + museum items | 40 |
| Vertical distance between major POIs | 120–220 m |
| Max dead-end run without payoff trigger | 30 s of digging |
| Unbreakable/decoy geometry | 0 (unfair obstacles are forbidden; `[SPOT]` "unbreakable obstacles") |

## 9. Biome rules of fairness

- Environmental tell before every hazard: heat shimmer before vents, drip audio before floods,
  crystal glow before crawlers. No blind deaths `[AGADH]` "unpredictable and inconsistent" moles.
- Environmental hazards in Cozy mode are cosmetic (warm/cool visuals, no damage) `[MELT]` freeze
  in Cozy.
- Nothing in the world can permanently destroy placed player structures or previously dug tunnels
  (no griefing caves; no "the dirt came back" bug class) `[OMT]` "all the dirt re-appeared".
