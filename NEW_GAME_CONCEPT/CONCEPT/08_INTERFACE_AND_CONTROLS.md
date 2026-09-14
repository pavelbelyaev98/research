# 08 — Interface and Controls

## 1. HUD

Minimal by design (I01). The HUD answers exactly one question: *can I keep digging?*

| Element | Behavior |
|---|---|
| **Depth** | Current depth below the surface rim |
| **Bag** | Count / capacity; turns a warning color as it fills |
| **Battery** | Current charge; the shared dig + jetpack resource |
| **Return warning** | Adaptive safe / risky / critical state; never exact required-energy math |
| **Detector** | Not a widget. Diegetic feedback on the tool plus, at most, a subtle screen-edge hint (F07; presentation TBD) |

Not on the HUD: minimap, compass, ore counters, objective list, damage numbers, news ticker, or any
permanent tutorial text.

## 2. Inventory screen

- Inspect-only grid (I04): collected finds with name and a short deadpan inspection line.
- No stats, no equipping, no sorting chores, no selling here.
- Uniques/components are marked as not sellable and displayed separately from the bag.
- Opening it is a pause-friendly moment; looking never drains the battery.

## 3. Pause menu

Direction (final tabs TBD, I03): Resume · New Game · Settings · Quit, with save status visible.
Correct back behavior is mandatory: ESC/B closes the current menu and never traps input. Settings
persist immediately and across launches.

## 4. Controls

| Input | Default | Notes |
|---|---|---|
| Dig / use tool | Hold left mouse / trigger | Hold-to-dig; toggle mode available; auto-dig assist optional |
| Jetpack | Space / A or bumper | Simple input; stable handling; rebindable |
| Crouch (precision) | Ctrl / stick click | Held; no stealth or stamina |
| Interact (machines, placement) | E / face button | Context-obvious prompts |
| Inventory | Tab / select | Inspect grid |
| C4: throw / detonate | Rebindable pair | Multiple charges; remote detonation |
| Photo mode | Rebindable | Pause-only |

Rules (I07):

- **Every action is fully rebindable** on every device.
- **Controller parity is mandatory:** every screen, including shop, inventory and display placement,
 works with a controller; glyphs swap automatically.
- **Left-handed preset** mirrors mouse buttons and updates prompts.
- Sensitivity, invert, deadzone and hold/toggle options exist per action.
- Optional gyro for fine control.
- No action in the game requires rapid repeated input, simultaneous multi-button holds, or mashing.

## 5. Feedback rules

- Every pickup has visible, audible feedback; the player never wonders whether something was
 collected (the "apparently I collected it but didn't see it" failure is banned).
- Detector feedback has a visual channel; the game is fully playable muted.
- Readability is never color-only: shapes, icons and labels back up every color cue.

## 6. Photo mode

Pause-only and simple (I13): hide HUD, adjust FOV, apply basic filters, toggle a watermark. **No free
camera** (there is no player model to frame). The player composes from their own view — which is the
point: the hole and the find are the subject.

## 7. Save system (player-facing)

- **Autosave** continuously at a measured interval and on events (sales, upgrades, recoveries);
 already implemented in the demo and to be kept (I14).
- **Three manual save slots** for different worlds/seeds.
- Save status is visible but unobtrusive; no save spam.
- Steam Cloud comes later (I14); the save format is designed so it can be added without changes.
- Loading restores the exact hole, inventory, display and progression — never fresh terrain with old
 purchases.

## 8. Settings that must exist (summary)

Motion comfort (FOV, shake, bob, comfort preset), controls (rebinding, sensitivity, handedness),
audio (ambience/SFX levels, mute), UI (scale where applicable), gameplay toggles (auto-dig assist,
toggle dig), and save management. Options persist immediately; every effect that exists has a
corresponding control (I08).

## 9. Accessibility pointer

The full suite is specified in `10_ACCESSIBILITY_AND_COMFORT.md`: motion comfort defaults, motor
assists, colorblind palettes, sound subtitles, zero-pressure design and pause-anywhere behavior.
