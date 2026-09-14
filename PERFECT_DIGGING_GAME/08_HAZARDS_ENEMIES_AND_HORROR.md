# 08 — Hazards, Enemies and Horror

> Across the corpora, unadvertised danger is the fastest way to destroy goodwill:
> `[OMT]` worms — "I was unaware that there would be jumpscare worms, as the game is not labelled
> as a horror type game"; `[AGADH]` mole stealth finale — "I didn't sign up for a fnaf-level
> jumpscare by a 20 foot rodent"; `[SPOT]` unlabelled horror/parkour — "colour me shocked when I
> find that this game is a horror game in disguise". This game treats danger as a **consent
> setting**, not a surprise.

## 1. The consent model

Three explicit axes, chosen in a first-launch screen (with clear previews) and changeable any time:

| Axis | Options | Default |
|---|---|---|
| **Creatures** | Off / Ambient (no combat, no damage) / Light (avoidable, no lethal) / Active (Standard) | **Ambient** (Cozy) |
| **Horror intensity** | Off / Spooky ambience (no shock) / Full (opt-in horror content) | **Off** |
| **Environmental hazards** | Cosmetic / Soft (slow, tint) / Damaging (Standard) / Deadly (Challenge) | **Soft** in Cozy, **Damaging** in Standard |

Additionally:

- The **store page and trailer** state exactly what exists: "optional horror elements can be
  enabled in settings" (or similar). No bait-and-switch. `[OMT]` "Please label it as a horror game"
  and `[SPOT]` "there's no mention or tag that this has a horror aspect" are prevented by design.
- `[AGADH]` "advertised as cozy" backlash is prevented by Cozy being the true default.
- Any horror content is **skippable and never on the critical path**. A warning card precedes it
  even when enabled.

## 2. Enemy design rules (when creatures are on)

1. **Tells before threats.** Every creature has a unique audio cue at 15+ m and a visual tell at
   8+ m. `[AGADH]` "unpredictable and inconsistent" enemies are banned.
2. **No one-shots.** Full-health characters survive at least two hits of anything in Standard;
   Challenge may escalate, but only after a layer teaches the threat.
3. **No spawn camping, no following home.** Enemies do not chase into the hub, checkpoint rooms,
   elevators or the surface. `[OMT]` "the worm follows you home… it can reappear 10 seconds later"
   is a named anti-pattern.
4. **Always avoidable.** Every enemy can be avoided with movement, light, noise, or the timer; none
   requires combat. Combat exists as an option (`04_TOOLS.md` charges, lamps), not a requirement.
5. **No equipment removal. Ever.** No sequence disables the drill, suit, map or recall. `[AGADH]`
   finale is the canonical violation.
6. **Agency always:** players can always leave, hide, fight, or recall. No forced stealth, no
   instadeath pits, no button-mash doors. `[SPOT]` parkour/chase rooms are the cautionary tale.
7. **Fair density:** no more than one major creature encounter per ~10 minutes of digging, and
   creature-free "rest layers" every other layer.

## 3. Creature roster (all opt-in, all telegraphed)

| Layer | Creature | Threat style | Counterplay | Horror? |
|---|---|---|---|---|
| 1 | Friendly moles, beetles | Ambience, collect stray ore | None needed; pet them | No |
| 2 | Cave slimes | Slow bump, slows you | Sidestep, light | No |
| 3 | Guardian statues | Patrol lines, wake if lit | Avoid light beams, use silent module | Spooky, mild |
| 4 | Blind fish | Startle, steal a pickup (returns it later) | Move slowly, lantern | No |
| 5 | Crystal crawlers | Nest defense around rich veins | Break nest, use charges | Mild |
| 6 | Ember wisps | Heat zones follow movement | Jet suit, vents | No |
| 7 | **Hollow Choir** (horror-only) | Full opt-in horror set: sound design, unseen stalkers | Lights, noise hygiene, group play | **Yes, opt-in only** |

The `[AGADH]`-style giant-mole set piece is reimplemented as an **optional Layer 7 den** ("The
Burrow") with consent, tells, counters and a real reward — for players who *want* that fantasy. It
never gates the ending.

## 4. Environmental hazards

| Hazard | Tell | Soft mode | Standard | Challenge |
|---|---|---|---|---|
| Heat vents | Shimmer, ticking rock | Warm tint | Chip damage, avoidable | Push + timed |
| Cold zones | Breath fog, blue vignette | Slow | Slow + battery drain | Damage |
| Flooded pockets | Drip audio, waterline | Swimming cosmetic | Slow swim, oxygen meter | Currents, oxygen |
| Unstable ceilings | Cracking, dust | Cosmetic dust | Drop rubble (non-lethal chip) | Lethal if ignored |
| Gas pockets | Odor particles, hiss | Haze | Knocks you back, light dims | Ignite risk (charges) |

Rules: every hazard shows a tell ≥ 2 seconds before effect; none can kill from full health in
Standard; none appear in Cozy as more than visual flavor; all are documented in the in-game
handbook with a screenshot.

## 5. The horror policy (for the "Spooky/Full" option)

Horror is allowed to be *good* here because it is opt-in, bounded and standalone:

- **Bounded:** horror content lives in specific marked dens/zones, never the main shaft, and can be
  exited at any time (recall works everywhere).
- **No tool removal, no forced chase sequences, no unskippable set pieces.**
- **Intensity slider:** Spooky (atmosphere, distant sounds) vs Full (jumpscares, stalkers, chase in
  dens).
- **Content warning card** before entering any Full-horror zone, every time.
- **Co-op:** if any player has horror off or intensity lower, the lobby uses the lowest setting.
- **Achievements** are fully obtainable with horror off `[SPOT]`/`[AGADH]` achievement issues.

## 6. Danger and modes

| Mode | Creatures | Hazards | Death | Notes |
|---|---|---|---|---|
| Cozy | Ambient only | Cosmetic/soft | None (rescue only) | Everything completable |
| Standard | Light by default, Active optional | Damaging | Respawn at checkpoint, **no item loss** | The "intended" feel |
| Challenge | Active, more types | Deadly | Full penalties (time/distance only) | Clear labelling; rewards cosmetic |
| Creative/Endless | Off | Off | None | Sandbox |

No mode changes story, collectibles or achievements — only pressure. `[SPOT]` "wrong build can
dead-end a save" cannot happen: death never destroys progress, choices are respecable
(`06_UPGRADES_AND_ECONOMY.md`).

## 7. Testable requirements

| Requirement | Verification |
|---|---|
| No creature exists in Cozy beyond ambience | Automated content audit + playtest |
| Every damage source has a ≥ 2 s tell | Design review checklist per encounter |
| No horror zone on the critical path | Graph analysis of the quest graph |
| Store page mentions optional horror verbatim | Marketing review gate |
| Achievements obtainable with horror/creatures off | Full 100% run with all danger disabled |
| Lowest-settings lobby rule in co-op | Multiplayer test matrix |
