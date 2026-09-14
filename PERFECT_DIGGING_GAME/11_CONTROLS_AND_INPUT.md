# 11 — Controls and Input

> Every reviewed game has control complaints:
> `[AGADH]` "Let me hold down the mouse button to dig please, I'm not gonna mash m1 over hours";
> `[OMT]` "no FOV slider… controller support missing or broken"; `[KD]` "no key rebinds, ESC doesn't
> close menus"; `[SPOT]` "the exit turret key is fixed as 'E'… I'm left-handed"; `[MELT]` "no way
> to disable motion blur". This file is a hard requirements list, not a nice-to-have.

## 1. Hold-to-dig (non-negotiable)

- **Press-and-hold is the default and always valid.** A tap performs a single dig step; holding
  performs continuous digging with no per-action penalty.
- No QTE, no mashing, no rhythm minigame, no "click faster" rewards. `[AGADH]` RSI complaints and
  `[MELT]` shovel click-spam are explicit design inputs.
- An **auto-dig assist option** (on by default when enabled): holding aims at the nearest voxel of
  the same material within the reticle cone and keeps digging.
- Controller: trigger analog controls dig strength where the tool supports it; a "dig lock" toggle
  allows fully hands-light sessions.

## 2. Full rebinding for everything

- **Every action is rebindable**, on every input device: keyboard, mouse, controller, Steam Deck
  controls. This includes menus (open/close, tabs), map pan/zoom, HUD toggles, recall, ping,
  placement rotate, screenshot.
- `[SPOT]` fixed `E`/`G`/`C`/`V` and `[AGADH]` AZERTY/left-handed complaints: **zero hard-coded
  keys**, and the game detects AZERTY/QWERTZ layouts.
- **Left-handed mode**: mirror mouse buttons; on-screen prompts follow the remap.
- **Conflicts are detected and resolved** with a clear dialog; duplicate bindings are allowed but
  flagged.
- **Profiles**: per-device binding sets, exportable/importable, synced via Steam Cloud.
- **Reset to defaults** per action, per device, or all.

## 3. Controller, Deck and input parity

- First-class controller support: full parity for every action (including map, inventory, shop and
  menus), correct glyph swapping, and no mouse-only screens. `[OMT]` "controller support
  missing/broken relative to the demo" is a named anti-pattern.
- **Steam Deck Verified:** readable text at 1280×800, suspend/resume safe (non-destructive pause),
  playable with sticks+triggers from first launch, ≤ 12 W typical draw in the loop.
- Gyro aim/fine-placement is supported but optional.
- Both input devices active simultaneously, with automatic last-used glyph switching (no
  "controller detected" popups).

## 4. Camera and mouse behavior

| Setting | Range | Default |
|---|---|---|
| Mouse sensitivity | 0.1–10 | 2.0 |
| Controller sensitivity | 0.1–10 (per-axis) | 2.0 |
| Invert Y / X | toggle each | Off |
| ADS/zoom sensitivity | % | 100% |
| Smoothing/acceleration | off/on + strength | Off |
| Toggle vs. hold for sprint/aim/dig-lock | per action | Hold |
| Field of view | 60–110° + vertical/horizontal unit toggle | 90° (with warning if < 75°) |

Additional guarantees:

- **Pause anywhere** (single-player), including mid-fall and mid-dig; saving on pause.
- **Safe alt-tab / focus loss:** the game pauses; no enemies spawn during the pause.
- **No accidental drop/use protections:** drop-item and recall require a hold or confirm; can be
  disabled by players who prefer speed.

## 5. Default keymap (all rebindable)

| Action | KBM | Controller |
|---|---|---|
| Dig / use tool | LMB (hold) | RT (hold) |
| Alt tool (charges/terraformer) | RMB | LT |
| Interact / place | E | A |
| Jump / jet | Space | A / LB (hold) |
| Sprint | Shift | LS click |
| Map | M / Tab | Select |
| Inventory | I | Y |
| Recall to checkpoint | R (hold) | D-pad Down (hold) |
| Beacon place | B | D-pad Up |
| Lamp place | L | D-pad Right |
| Pause | Esc | Start |
| Skip / advance text | Space | A |

## 6. Input accessibility hooks

Details in `14_ACCESSIBILITY.md`; the control-layer hooks:

- **One-hand layouts:** presets for left-only/right-only play (all dig/traversal/interact on one
  device side); mouse-only and controller-only presets.
- **Sticky keys for holds:** any hold action can become a toggle (dig-lock, sprint toggle, aim
  toggle).
- **Timing assists:** no action requires rapid double-input or precise timing in the critical path;
  if designed otherwise, it gets an alternative trigger.
- **Input buffering:** generous (200–300 ms) so inputs during animations are never dropped.
- **Deadzone/saturation/curve** controls for sticks and triggers.

## 7. Testable requirements

| Requirement | Verification |
|---|---|
| Digging one hour causes no requirement to click > 1×/s | Input telemetry test |
| Every action appears in the rebind UI on every device | Automated UI audit |
| AZERTY/QWERTZ detection works on first launch | Locale test matrix |
| Deck suspend/resume mid-dig restores exactly | Deck compliance test |
| No screen is unreachable with controller only | Full controller-only playthrough |
| Left-handed preset produces correct prompts | Screenshot diff audit |
