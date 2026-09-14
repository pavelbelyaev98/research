# 04 — Questions, Round 2: World and Terrain

**How this works:** answer by ID in chat. I record answers in `02_DECISIONS.md`. Unanswered questions
stay `OPEN`. Recommendations cite the five review analyses; if you disagree, your answer wins and the
registers note the change.

This round defines the physical game: the site, its limits, its materials, its light, and how the
player's hole is generated and persisted. Systems/progression (upgrades, economy, fuel, detector
levels) is Round 3 (`05_QUESTIONS_SYSTEMS_AND_PROGRESSION.md`).

---

### W01 — Site dimensions
**Context:** The site is currently 24×24×32 m. Target completion is 3–5 h and the user wants a
mostly vertical game. Depth is the progression axis, so height matters more than footprint.
**Options:**
- **A)** Keep 24×24×32 m — dense, cheapest, but 32 m is shallow for 3–5 h of content.
- **B)** 24×24×48 m — same footprint, +50% depth for vertical progression, contained lateral area. *(Recommended)*
- **C)** 32×32×64 m — more lateral discovery and more depth; roughly doubles content/QA cost.
- **D)** 16×16×48 m — tight shaft, most focused, risks claustrophobia and less cluster room.
**Recommendation:** B. `[KD]` showed straight-down trivialization when depth alone wins; the fix is
lateral clusters and layers, not a huge map. `[MELT]` showed how large identical spaces become a
navigation endurance test. Keep the footprint contained, deepen the shaft.
> **ANSWER:**

### W02 — Boundary language (why you can't dig sideways forever)
**Context:** The site must feel finite and believable. Permanent limits must look categorically
different from diggable ground, so players never confuse "tough" with "impossible".
**Options:**
- **A)** Reservoir infrastructure: concrete retaining walls and dam structures at the sides; bedrock shelf below; deep water or steep rock at the far edge. *(Recommended)*
- **B)** Natural only: solid bedrock cliff walls and an underground rock floor.
- **C)** Water boundary: the dig floor sits between vertical water walls; you're digging inside the drained basin.
- **D)** Mixed with authored "unbreakable" geology in the corners.
**Recommendation:** A + C flavor. The reservoir story supplies believable, readable walls (concrete
vs soil vs rock) and a water wall explains one edge. `[AGADH]` reviews specifically complained that
the same grey rock meant both "tough now" and "eternal wall" — never reuse a diggable material look
for a boundary.
> **ANSWER:**

### W03 — Darkness and light
**Context:** You want dark areas and mentioned carried and/or placeable lights. `[KD]` was criticized
for extreme darkness; `[OMT]`'s placeable colored lamps were praised; `[AGADH]`'s dark+battery combo
created stress.
**Options:**
- **A)** Personal light always on and free (short range, battery-independent) + placeable lamps for reach, routes and beauty. *(Recommended)*
- **B)** Personal light drains the battery; darkness is a real resource pressure.
- **C)** No personal light; only placed lamps; bring your own lighting.
- **D)** Fully lit site; no darkness at all.
**Recommendation:** A. Darkness becomes atmosphere and a reason to place lamps, never a punishment.
Charging light from the shared battery would recreate the hated `[AGADH]` death-spiral (dark +
low battery + deep hole). Lamp placement should be optional but rewarding (marking routes,
illuminating finds for photos).
> **ANSWER:**

### W04 — Material progression
**Context:** The underground needs readable change without "special texture = treasure" signaling.
Materials also carry hardness and depth identity.
**Options:**
- **A)** 5 materials: soil, clay, gravel, compact sediment, rock (+ local concrete).
- **B)** 7 materials: adds dry sand and hard rock variants, with color/palette shifts by depth. *(Recommended)*
- **C)** 9+ materials: rich geology, more art/production and memory burden.
**Recommendation:** B. Enough variety to make every zone feel new (the `[MELT]` "all corridors
identical" failure), few enough that a player learns them without a tutorial. Concrete/constructed
material only near structures and boundaries.
> **ANSWER:**

### W05 — Hard formations
**Context:** "Remember that wall I couldn't break" is a strong return motivation, but gating the main
path with hard walls was criticized when the top tool stayed weak (`[SPOT]` drill radius).
**Options:**
- **A)** A small number of memorable hard pockets (5–8) that are optional and contain something good; never block the main descent. *(Recommended)*
- **B)** Frequent hard layers that pace progression, some blocking the critical path.
- **C)** No hardness at all; all ground digs at the same speed.
**Recommendation:** A. They become personal landmarks ("I'll come back with the new drill"), not
walls. The main descent stays open, so a straight-down player is never hard-locked, but the best
finds sit behind old obstacles.
> **ANSWER:**

### W06 — Terrain technology and cleanup
**Context:** Digging must feel free-form (tunnels, overhangs, trenches) while never leaving
collidable specks (`[AGADH]`'s most-cited technical flaw) and never producing physics debris that
snags movement.
**Options:**
- **A)** Full voxel destructible terrain; auto-removal of disconnected fragments; debris is purely
  visual; collision always matches the visible mesh. *(Recommended)*
- **B)** Heightmap-based digging (no overhangs/tunnels; simpler and cheaper).
- **C)** Voxel terrain with a limited depth of destruction.
**Recommendation:** A. It matches the core fantasy (the player shapes the hole) and the cleanup rule
already confirmed. B would forbid the trenches and overhangs that make the hole personal.
> **ANSWER:**

### W07 — Depth bands and identity
**Context:** Players should feel the world changing as they descend, without separate "levels".
**Options:**
- **A)** 4 bands: recent fill/rubbish → old river sediment → deep clay/stone → ancient constructed layer. *(Recommended)*
- **B)** 3 broad bands.
- **C)** 6 narrow bands with stronger visual shifts.
**Recommendation:** A. Four identities match the 3–5 h arc (roughly one per hour), support the
mystery pacing (believable → suspicious → impossible), and keep texture/production scope sane.
> **ANSWER:**

### W08 — Surface layout
**Context:** Returning must be short and satisfying: sell, recharge, upgrade, back down. Walking and
menu friction are top complaints in `[MELT]` and `[SPOT]`.
**Options:**
- **A)** Compact yard: shaft mouth, Sell All machine and upgrade bench within ~10 seconds of each other; discovery fridge on a wall nearby. *(Recommended)*
- **B)** Slightly spread-out worksite: separate trailer for selling and a shed for upgrades (~30 s walk).
- **C)** A small building with interior interactions (walking through doors/menus).
**Recommendation:** A. Keep the physical comedy of the Sell All machine but zero commuting. The
fridge should be visible from the shaft so first finds are naturally displayed.
> **ANSWER:**

### W09 — What is randomized per save
**Context:** Replay value comes from not knowing where things are, but pacing must stay reliable.
**Options:**
- **A)** Positions, depths (within bands), rotations and cluster layouts are randomized; the material
  layout and general depth ranges are authored. Generation validates pacing (early guaranteed notable
  find, no long dry stretches, no novelty dumping). *(Recommended)*
- **B)** Fully randomized terrain and finds, no validation.
- **C)** Fixed authored layout for everyone.
**Recommendation:** A. It is the only model that delivers both "genuinely not know where a favourite
discovery is" and "every run has a good first ten minutes".
> **ANSWER:**

### W10 — Water
**Context:** The site is a drained reservoir with visible water. No swimming is wanted.
**Options:**
- **A)** Water exists as scenery and boundary: pools in low corners, a waterline on the walls, damp
  zones near the edges; digging never floods; no swimming. *(Recommended)*
- **B)** Small flooded pockets you must drain or avoid.
- **C)** No visible water; entirely dry.
**Recommendation:** A. It sells the setting, gives the boundary its meaning, and stays out of the
digging verb. B smuggles in an oxygen/hazard system the NOT-list forbids.
> **ANSWER:**

### W11 — Dig chunk size and feel
**Context:** The size of one removed piece defines the game's tactile feel, performance and how fast
the hole takes shape.
**Options:**
- **A)** 0.5 m voxels — chunky, satisfying, readable silhouettes, good performance. *(Recommended)*
- **B)** 0.25 m voxels — finer detail, slower progress per stroke, more objects per pixel, heavier.
- **C)** 1.0 m voxels — very chunky, fast digging, blocky/crude object reveals.
**Recommendation:** A. It matches the "shovel bites chunks" satisfaction (`[AGADH]`'s praised crunch)
and keeps the site (24×24×48 m = 48×48×96 voxels) workable.
> **ANSWER:**

### W12 — Sky, light gradient and the map question
**Context:** An open-air dig means you can always see the sky from above, but depth creates darkness.
Separately, the game has no minimap; with a vertical hole, orientation is easy, but "where was that
hard wall / that signal?" still matters.
**Options:**
- **A)** Natural light fades with depth into colored ambient per band; personal light + placed lamps
  handle the rest. No map or compass; the fridge records depths and the detector cues direction. *(Recommended)*
- **B)** Add a simple depth meter + remembered marker list (no visual map).
- **C)** Add a minimal top-down map of the hole.
**Recommendation:** A for now, with B as a cheap fallback if playtests show disorientation. A full
map (C) fights the "your hole is the map" fantasy and adds UI weight to a short game.
> **ANSWER:**

---

## Answer sheet
> W01: | W02: | W03: | W04: | W05: | W06:
> W07: | W08: | W09: | W10: | W11: | W12:
