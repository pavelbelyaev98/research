# 07 — Traversal and Soft Pressure

> The pressure systems in the comparative set are its most hated mechanics:
> `[SPOT]` stamina/beer ("anti-fun… exists only to disrupt the core gameplay loop", "will you let me
> dig or not?!"), `[AGADH]` battery blackout and fall damage ("want to do bad things to the
> creators"), `[MELT]` post-patch heat ("patched in stress"). This file defines pressure that
> **sets a trip's rhythm** without ever taking anything from the player.

## 1. The ascent guarantee

Getting back up must always be as easy as getting down. `[OMT]`'s single central rope was its
biggest traversal criticism ("no jetpack or anything… a pain to rebuild walkways") and `[OMT]`'s
potential rope softlock is a named anti-pattern.

Four independent ways up, always available:

1. **Chute / lift** at every activated checkpoint (unlocked Layer 1 tutorial): a fast, free ride to
   the surface, usable from any checkpoint.
2. **Anchor line** (tool): placeable winch line; fast ascent with a smooth camera.
3. **Jet suit**: the late-game traversal toy; enough fuel for comfortable climbs.
4. **Terraformer stairs**: shape your own route; snap-to-stair ghosts prevent tedious block-placing.

Additional rules:

- **Recall button** ("Return to Surface") unlocks at the first checkpoint and is always one input
  away. It costs nothing; it is never disabled by story or danger.
- **Deaths or rescues never teleport you to the surface with lost cargo** (see §3).
- Digging can never create an unreachable home location: bedrock under the hub is indestructible
  and the shaft walls are climbable at checkpoints (built-in ladders).

## 2. Fall damage policy

| Mode | Rule |
|---|---|
| Cozy | No damage. Landing hard causes a stagger + dust, never harm. `[MELT]` "you don't die, you freeze" praise |
| Standard | Forgiving: damage starts above 8 m, capped at 35% max HP per fall, never lethal from a full-health fall, no damage when landing on player-placed structures/soft material |
| Challenge | Classic fall damage, clearly labelled; jet suit/anchors trivialize it by design |

Additional guarantees:

- **No 1-voxel kills.** Floating specks are removed by the Clean Cut/flood-fill system
  (`04_TOOLS.md` §5), so "1x1-pixel particles that will break your legs" `[AGADH]` cannot happen.
- **Terminal-velocity feedback:** wind audio, screen tilt, a landing reticle; the player always
  knows when a fall is dangerous.
- **Cave-ins cosmetic only.**

## 3. Trip pressure: battery / heat / weight as soft limits

These systems exist to create the classic "should I grab one more vein?" decision — the praised core
of `[SPOT]`'s day/night loop — not to punish.

### Design contract (all modes)

| Event | Result |
|---|---|
| Battery reaches 0 | **No explosion.** Drill speed drops to 40%; light dims to a personal glow; a "weak" audio cue plays. You can keep digging slowly or walk out |
| Suit heat/cold reaches 0 | Speed slows, screen edges tint; no damage spirals. A **rescue drone** arrives after a grace period and *carries you* (not your loot) to the last checkpoint |
| Weight over capacity | Move up to 120% capacity at −25% speed; cannot exceed 150%; excess pickups auto-send to hub storage. **No drops, no deletion** |
| Freeze/blackout during carry | Loot is *kept*; only time is lost. `[MELT]` freeze-loss and `[AGADH]` blackout-loss are forbidden |

### Tuning targets

- A full battery at base tier should allow **≥ 20 minutes** of active digging or a 300 m descent.
- Upgraded battery/suit should allow **≥ 45 minutes** or a full layer round trip.
- Layers 6–7 tighten these numbers by ~20%, never more; the suit tier matching the layer restores
  full comfort.
- **Post-launch rebalances must never make an existing save's comfort tier worse.** `[MELT]`'s
  August heat nerf ("devs rebalanced something, now I can't reach the end of a tunnel") is a named
  anti-pattern: balance changes ship behind a **beta branch first**, with in-game compensation for
  altered saves (`20_LIVE_UPDATES_AND_DEV_PROCESS.md`).

## 4. Fast travel

| Type | Unlock | Cost | Notes |
|---|---|---|---|
| Hub lift | Start | Free | Surface ↔ Layer 1 checkpoint |
| Checkpoint network | Activating a checkpoint | Free | Any activated checkpoint ↔ any other |
| Beacon (consumable/placeable) | Tool tier 2 | Small coin | Personal return point |
| Recall to surface | First checkpoint | Free | Always available, never disabled |
| Cart/rail shortcuts | Layer-specific | One-time build | Scenic rides; showcase the tunnels |

Rules:

- **Checkpoints every 150–250 m**, at landmarks, visually distinct (warm light, flag, music sting).
- **First visit is one-way** (you must walk/dig to it) so exploration is preserved; after
  activation it is a full network.
- Fast travel never costs progress or items; it exists to eliminate the "30-minute commute" that
  dominated `[SPOT]`'s complaints and the "hours of tedious back-and-forth" of `[MELT]`.

## 5. Encumbrance-free reading: the Trip Meter

A single HUD widget ("Trip Meter") shows the four soft pressures in one glance: battery, suit
comfort, weight, and time since last checkpoint. Its design rules:

- **No numbers that require interpretation** — arcs and color, tooltips for numbers.
- **Predictive warnings**: "≈ 6 min of dig time left", "next checkpoint 120 m".
- **Never a countdown to a loss** (no "explodes in 10 seconds"). Pacing, not panic.
- Cozy mode hides the meter by default (the player only sees ore sparkle and map).

## 6. Health and rescues

- Base HP in Standard/Challenge; heal via buyable rations and checkpoint rest (free, instant).
- **No AFK healing.** Rest at checkpoints/at hub regenerates fully; rations are cheap and
  craftable — `[OMT]`'s "wait 5 minutes for a sandwich to spawn" is banned.
- Rescues (freeze/blackout/fall-to-0 HP) put you at the last checkpoint with all inventory except a
  teleport-rescued "heavy" load if over capacity — which is delivered to hub storage, not lost.
- Cozy has no HP at all; Standard caps damage sources to fair, telegraphed ones; Challenge respects
  the same tell rules (no "unpredictable and inconsistent" enemies `[AGADH]`).

## 7. Testable requirements

| Requirement | Verification |
|---|---|
| A player can always return to surface from any point ≤ 3 min after unlocking checkpoint 1 | Automated playtest bot + human test |
| No fall ≤ 8 m is lethal at full HP in Standard | Automated matrix test |
| No system ever deletes carried items | Fuzz test of failure states (0 battery, 0 HP, freeze, quit mid-trip, cloud conflict) |
| Fast travel round trip ≤ 20 s from any checkpoint | Timed test |
| Trip pressure adds ≥ 5 min of average session length but ≤ 1 "annoyed" survey score | Playtest telemetry + survey |
