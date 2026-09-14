# 04 — Tools

> **Iron rule:** a tool you own is never taken away, disabled, or invalidated. New tools expand
> your kit; they do not replace it. `[AGADH]` disabled every tool in the finale; `[MELT]`'s Tesla gun
> made the flamethrower investment worthless; `[OMT]` tools never evolved. All three are fixed here.

## 1. Primary dig tool — 6 tiers, one continuous line

All tiers use **hold-to-dig** (a single press-and-hold is valid; click-spam is never required or
rewarded). Every tier changes the model, sound pitch, particles and head-bob response, so the
upgrade is felt in the body in under a second. `[OMT]` "invisible +5%" upgrades are forbidden.

| Tier | Name | Dig shape | Radius | Speed | Feel | Unlock |
|---|---|---|---|---|---|---|
| 1 | Rusty Shovel | 1 voxel, chunky | 0.4 m | Slow but weighty | "Honest work" | Start |
| 2 | Steel Shovel | 1–2 voxels | 0.6 m | +40% | Crisp thunk | Layer 1 shop |
| 3 | Powered Spade | 2-voxel scoop | 0.9 m | +35%, auto-sweeps | Vibration, dust | Layer 2 |
| 4 | Scoop Drill | 3-voxel bite + **vacuum pickup** | 1.2 m | +30% | Roar, auto-collect | Layer 3 |
| 5 | Auger | Cone, 5 voxels | 1.9 m | +25% | Continuous spin | Layer 5 |
| 6 | Core Drill | Sphere bite, 9 voxels | 2.8 m | +20% | Satisfying erase | Layer 6 |

Design notes:

- **Vacuum pickup arrives at tier 4, not as a separate replacement.** Reviewers loved `[OMT]`'s
  vacuum mainly because it ends **floating dirt specks** and enables **spitting dirt back out**.
  Both properties are in this design from tier 4 (and the forklift-like scoop of tiers 1–3 leaves
  no un-minable 1-voxel leftovers — see §5).
- **Radius beats raw speed at high tiers** so late-game digging feels like *sculpting* `[AGADH]`
  drill praise, without making early game pointless.
- **Every tier can break every material of its intended layer**; campaign gates are keys/doors, never
  "your drill is too small" walls that force grinding to the next tier. `[SPOT]`'s "top drill still
  has a criminally small radius" and its expensive mandatory tier purchase before the finale are
  explicitly avoided.

## 2. Utility tools (parallel upgrade lines, each 4–5 tiers)

| Tool | Purpose | Tiers | Notes |
|---|---|---|---|
| **Collector field** | Auto-vacuum ore/junk at range | 1–5 (1.5–6 m) | Comes online with Scoop Drill; ends specks forever |
| **Terraformer** | Re-place dirt/stone blocks; build stairs, ramps, patios | 1–4 | `[OMT]` dirt-spitting is a beloved idea — made a proper tool with ghost preview |
| **Anchor line** | Rope/winch: descend fast, ascend safely, tow carts | 1–4 | One of several ways up — never the only way `[OMT]` rope-only complaint |
| **Jet suit** | Hover/jump; the late-game traversal toy | 1–4 | `[AGADH]` `[SPOT]` jetpack praise; activates gently, no fall-damage anxiety |
| **Lamp kit** | Placeable colored lights; smart glow follows tunnels | 1–4 | `[OMT]` placed lamps praised; fixes `[KD]` darkness/readability |
| **Charges (dynamite)** | Shaped blasts, dig radius, ore-safe mode | 1–5 | Must never bounce/clip `[AGADH]`, must be worth using `[KD]` "trap upgrade": blast radius scales hard, tier V clears rooms |
| **Scanner / radar** | Ping ore, caves, POIs; writes to map | 1–4 | Direct fix for `[MELT]`/`[SPOT]` missing map |
| **Suit** | Heat/cold/water/flood protection | 1–4 | Layer access, not a survival stat; in Cozy, visual only |
| **Beacon / recall** | Place a return beacon; recall to last checkpoint | 1–3 | Two-way fast travel is a 1.0 requirement, not a stretch goal |

## 3. Tool module system (depth without replacement)

Instead of replacing tools, each tool accepts **modules** found in the world:

- **Shovel/Drill modules:** "Vein Sense" (highlights ore behind walls), "Silent Mesh" (no noise in
  danger zones), "Wide Bite" (+shape), "Kinetic Return" (digging recharges battery slightly).
- **Charge modules:** "Nutrient Charge" (reveals fossils), "Gentle Charge" (no ore destroyed),
  "Chain Charge" (secondary blast on a delay).
- **Suit modules:** filters, insulation layers, dive tanks.
- **Terraformer modules:** preset stair/ramp templates, blueprint stamps ("build 4×4 platform").

Modules are deterministic world content (POIs, contracts, museum milestones), never random lootbox
drops `[KD]` 2.0 RNG blueprints are a cautionary tale. Modules can be swapped freely at the hub.

## 4. The tool feel budget (non-negotiable)

| Property | Requirement |
|---|---|
| Input | Hold-to-dig always valid; tap also works; controller trigger analog where possible |
| Audio | Unique, layered loops per tier; the dominant ambient sound while digging; mute-able |
| Feedback | Damage numbers off by default; ore "pop" and material crumble on |
| Camera | No involuntary roll; shake scalar slider; head-bob slider; first-person FOV slider |
| Hands | No QTE mashing, no per-click requirements, no "hold three keys" stance |
| Crosshair | Dig reticle shows material and predicted shape; accesscolor modes |

## 5. The floating-dirt guarantee

`[AGADH]`'s single most-cited technical flaw: 1-voxel specks left floating, which snag movement,
block the jetpack, cause fall damage and ruin speedruns `[AGADH]` "1x1-pixel particles that will
break your legs", `[OMT]` "those tiny pebbles left flying in the air that can kill you".

Engineering requirements:

1. **No unsupported voxels.** After a dig, any voxel not connected (face-adjacent, carrying a
   connectivity flag) to the terrain or a placed structure converts into a collectible pickup and
   flies to the player. This runs on a bounded flood-fill (budgeted per frame) — see §15.
2. **No collision with collectible pickups.** Pickups have triggers, never colliders.
3. **Cave-in cosmetics only.** Dust and pebbles are particles; particles never have collision and
   never deal damage.
4. **Destructible props drop props**, not voxel debris.
5. **A "Clean Cut" assist option** (on by default) snaps the dig shape to remove partial voxels.

## 6. Progression guardrails

- **No tool is ever disabled by the story.** `[AGADH]` finale rule, absolute.
- **No ammunition economy on the primary tool.** Digging never costs consumables. Charges are a
  bonus, not a baseline requirement.
- **No durability.** Tools never break. `[SPOT]`'s "broken shovel" early feel is achieved with
  speed, not fragility.
- **Respec is free and instant** at the workshop; modules are never consumed by removal.
- **Tool count budget:** 9 tools + modules. Every tool must be useful in at least two layers and
  have a skin/museum identity.
