# 03 — World and Site

## 1. The site

A drained river-fed reservoir. The working floor sits inside visible former banks, concrete
retaining walls, and leftover waterworks. It is finite, believable and clearly bounded.

- **Dimensions:** depth at least 100 m; exact depth and footprint are set by feel in playtest (W01).
  Depth is the progression axis; the footprint stays contained.
- **Surface:** authored, not procedurally generated into ugliness. A small worksite yard
 (see `07_SURFACE_HUB_AND_DISPLAY.md`).
- **Underground:** fully diggable voxel ground except permanent boundaries.
- **No pre-existing caves or tunnels:** every opening in the ground is one the player made.

## 2. Boundaries (why you cannot dig forever)

Permanent boundaries must look categorically different from any diggable material (W02):

- **Sides:** concrete retaining walls, dam infrastructure, steel pilings — industrial, cracked,
 obviously not soil.
- **Bottom:** solid bedrock shelf.
- **One edge:** natural bedrock shelf (W10). No water, no swimming, no flooding — the drained
  reservoir's edge reads as ground meeting stone, with no fake-water interaction problems.

Rule: never use the same material look for "tough but diggable" and "eternal wall". Players must
know at a glance what will eventually yield.

## 3. The four zones

Each zone changes ground, palette, typical finds and mood. Transitions are gradual; there are no
loading screens or separate levels (W07, F02).

| # | Zone | Ground | Finds typical | Mood |
|---|---|---|---|---|
| 1 | **Recent fill** | Loose soil, gravel, roots, modern rubbish | Bottles, scrap, household junk, common ore | Bright, familiar, hopeful |
| 2 | **Old sediment** | Compacted river sediment, clay lenses | Old tools, machinery parts, first fossils, better ore | Nostalgic, slightly odd |
| 3 | **Deep clay / stone** | Hard clay, rock, occasional concrete | Larger machines, rare ore, deliberate objects | Heavy, dim, purposeful |
| 4 | **Ancient constructed** | Unknown compacted material, ancient fabrication | Impossibilities, final components, the final object | Cold, quiet, wrong in a good way |

Zone names are placeholders; final naming is content work.

## 4. Materials

Working set (7 families; exact list TBD, W04): soil, clay, gravel, compact sediment, rock, dry sand,
hard rock — plus concrete near structures. Each family differs in **behavior**, not just color
(F12):

- sand pours and collapses quickly;
- clay sticks and clumps;
- gravel trickles;
- compact sediment resists evenly;
- rock chips and cracks;
- concrete sparks and barely yields until the right power level.

The tool adapts automatically to the material (see `04_TOOL_AND_MOVEMENT.md`); materials reward the
right behavior but never lock it out.

## 5. Tough ground: hard pockets

A small number of memorable, optional obstacles (5–8 target) — never walls across the main descent
(W05b):

| Example | Feel | Behind it |
|---|---|---|
| Concrete plug | Barely scratched by early tools | A waterworks alcove with a rare part |
| River-rock lens | Dense boulder cluster | A complete fossil |
| Compacted gravel shelf | Slows digging for a while | An older, richer pocket of finds |

Every pocket has **multiple solutions**: sufficient tool power, C4, or patience/routing. Discovering
one early and demolishing it later is a designed moment of power.

## 6. Terrain technology and cleanup

- **Full voxel**: every diggable cube can be removed; tunnels, overhangs and trenches are legal
 (W06). Chunk size prototype-tuned (W11).
- **No floating specks**: after a dig, disconnected valuable voxels convert to pickups and fly to the
  player, while plain dirt crumbs simply vanish; nothing collidable is ever left suspended.
- **Debris is visual only**: particles never collide and never deal damage.
- **Collision always matches the visible mesh.**
- **Substantial structures survive**: ledges, tunnels and overhangs the player built are preserved;
 only unsupported crumbs are cleaned.
- **Progress never resets**: the terrain edit history is saved; loading restores exactly the hole
.

## 7. Lighting and darkness

- **Sky light reaches down open shafts** and fades with depth (F09).
- **A dim ambient floor** exists everywhere — the game is never pitch black; you can always barely
 navigate (W03g).
- **Placeable lamps** provide real visibility, let players mark routes, and light finds for photos.
- **No personal light.** The tool does not act as a headlamp; darkness in covered areas is a reason
 to place lamps.
- **Zone lighting moods:** warm daylight near the surface → cool dim mid-depths → near-black deep
 where lamps are effectively required.

## 8. Randomization rules

- Authored: zone layout, depth ranges, boundary placement, general difficulty curve.
- Randomized per save: find positions, depths within bands, rotations, cluster layouts, some
 surrounding junk (W09).
- The generator produces a candidate layout and validates pacing (Section 4 of
 `02_CORE_LOOP.md`) before accepting it.
- The accepted population is finite and persisted; patches never reroll an existing save.

## 9. No hazards

No lava, gas, oxygen, hunger, earthquakes, temperature damage, or monsters (Q13). The only pressure
is the shared battery, the bag's capacity, and the player's own greed — all soft, all fair, all
recoverable (see `06_PROGRESSION_AND_ECONOMY.md`).
