# 04 — Tool and Movement

## 1. One machine

There is exactly one excavation tool. It starts as an ordinary shovel and ends as a garage-built
absurdity. The player never switches tools; upgrades bolt onto the same object (F11).

- **Visible body:** the tool only — no hands visible (F04). The player watches the machine evolve
 for the whole game.
- **Visual escalation:** motors, battery packs, wider heads, pipes, reinforcement, a late nozzle,
 welded plates and cables. The silhouette grows ridiculous while staying recognizably the same
 machine.

## 2. Digging input

- **Hold-to-dig is the default.** Continuous digging from the very first shovel; no click-per-bite.
- **Toggle mode** available; press once to start, once to stop.
- **Auto-dig assist** available in accessibility settings.
- **Full rebinding** for every action on keyboard, mouse and controller; left-handed preset;
 sensitivity options; optional gyro (I07).
- No mashing, no QTEs, no rhythm inputs, anywhere in the game (I10).

## 3. Automatic material adaptation (the mode model)

There is no mode button and no required switching (S09c). The machine reads the ground and changes
behavior automatically:

- **Early/mid game:** distinct behaviors cycle by material — a fast precise bite (Shave-like), a wide
 cheap scoop (Scoop-like), and eventually a blast head (Nozzle-like). The player sees and hears which
 head is active.
- **Soft preference, never a lock:** each material family clearly rewards one behavior (sand rewards
 the fast bite; hard rock rewards the blast head; loose fill rewards the wide scoop), but every
 behavior can dig everything (W05b, S09b). A visual/audio cue hints when a different behavior would
 be much more effective; ignoring it costs speed, never access.
- **Late game convergence:** the machine evolves toward one smart vacuum head that handles everything
 efficiently. Exact late behavior is validated in playtesting (S09c provisional).
- **Upgrades improve all behaviors at once** — one shared tool upgrade level (Q30f). No separate
 upgrade economy for a second tool.

## 4. Upgrade tracks and the tool

The tool's own track (Tool) controls power, bite size and adaptation quality; see
`06_PROGRESSION_AND_ECONOMY.md` for all six tracks. Every third level introduces a visible
capability change; increments in between improve feel (S02).

## 5. Jetpack

- Starts simple and **stable**; never deliberately hard to control (S07b).
- Each upgrade improves speed, fuel efficiency, altitude and assists (hover hold, softer landings).
 Control quality never degrades.
- Simple input (Space; controller equivalent); full rebinding still applies.
- Works in narrow player-made shafts without wall bumps dealing damage or knocking the player around.
- With upgrades, returning from old shallow digs becomes trivial — a designed power fantasy.

## 6. Precision crouch

- Held crouch lowers the viewpoint and slows horizontal movement, allowing low tunnels.
- No stealth, no stamina, no automatic cliff protection.
- Crouch is for precision and shaping; it never gates progress.

## 7. C4

- **Thrown or placed, then remotely detonated.** Multiple charges can be active at once (S08b).
- Charges **stick where they land** — no bouncing or clipping through targets (the reviewed
 anti-pattern).
- Placement is forgiving: a clear valid/invalid preview; no pixel-perfect hotspots; invalid attempts
 do not consume a charge.
- The blast is **properly powerful**: a large, predictable volume of ground disappears with matching
 cleanup. Saving for charges must feel worth it.
- Charges cost money; C4 is an optional accelerator, never the only way past anything (W05b).
- Its own small upgrade track: blast size, pack size, efficiency (S01).

## 8. Falling and failure (movement side)

- **No health bar.** The battery is the only resource (Q28f).
- Small falls: nothing. Bigger falls: a stagger and a battery knock. Extreme falls (or 0 battery
 anywhere): recovery to the surface with all finds kept, a depth-scaled fee, and any shortfall as
 interest-free debt auto-deducted from future sales (Q26f).
- Falls never delete items, never kill, never roll back progress.

## 9. What the tool is not

- Not a weapon; there is no combat (Q13).
- Not a light source (W03g).
- Never disabled, removed or invalidated by the story (C01).
- Not joined by a separate gun tool. The late nozzle is an attachment on the same machine; the final
 visual is a shovel that has clearly become a cannon (Q30b).
