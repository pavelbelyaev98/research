# 14 — Accessibility

> The corpora contain concrete, avoidable harm: RSI from click-to-dig `[AGADH]` `[OMT]`, motion
> sickness and eye strain in every game (`[AGADH]` 31 FOV mentions with "vertigo, headache"; `[MELT]`
> "no settings to reduce motion sickness, which made it unplayable for me"; `[SPOT]` an unusually
> frequent complaint even among players who never get sick), QWERTY-only bindings `[AGADH]`,
> left-handed lockout `[SPOT]`, unreachable color-coded UI, and unadvertised horror for anxious
> players `[OMT]` `[SPOT]`.
> Accessibility here is designed for the **core audience of a cozy game**: hands, eyes, ears,
> nerves and schedules must all be respected.

## 1. Motion comfort (the genre's #1 accessibility issue)

| Feature | Options | Default |
|---|---|---|
| FOV | 60–110° + unit toggle | 90° |
| Motion blur | Off entirely | Off |
| Camera shake | 0–100% | 40% |
| Head bob | 0–100% | 30% |
| Acceleration / sprint FOV kick | Off/On + strength | Off |
| Rolling/lean effects | Off/On | Off |
| Damage vignette pulses | Off/Subtle/On | Subtle |
| Screen flashes | Normal/Reduced/Off | reduced at first launch if triggered |
| **Comfort camera** | reduces rapid vertical motion; widens collision "grace" | On if player reports sensitivity in wizard |
| **Third-person camera option** | full alternate camera mode | Available (a first for the genre) |
| Horizontal lock | prevents roll in tight tunnels | Off |
| Transition fades | short vs instant | instant |
| Speed lines / particle wind | Off/On | Off |

Design requirements (not just settings):

- No forced camera takeovers, no head-snap during rescues, no rotating "elevator" cams in the
  critical path unless the player chose the mode that includes them.
- Camera motion is frame-rate-independent and smoothed at any FPS `[SPOT]` drill-speed-tied-to-FPS
  and camera stutter complaints.
- A "Motion Comfort" preset one click away from first launch; a mid-game reminder is available in
  settings ("getting queasy? try this").

## 2. Motor and dexterity

| Feature | Notes |
|---|---|
| Hold-to-dig + auto-dig assist | Default; no mashing anywhere (`11`) |
| Toggle for every hold action | dig-lock, sprint, aim, placement |
| One-hand presets | left-only / right-only layouts for KBM and controller |
| Input remap for 100% of actions | every device, with profiles (`11`) |
| Aim/placement assists | snap-to-voxel-plane, generous grab radii, no precision QTEs |
| Auto-collect | on by default; removes fiddle |
| Auto-walk/auto-ascend assist | hold-to-move along tunnels, optional |
| Reduced input buffering | inputs never dropped during animations |
| Speech-to-text / text-to-speech | optional chat/commands and UI readout |
| Difficulty assists independent of mode | infinite battery option, no fall damage, slower timers |

Every action required by the critical path must be performable **without rapid repeated input,
without simultaneous multi-button holds, and with one hand**.

## 3. Vision

| Feature | Options |
|---|---|
| UI scale | 50–200% |
| Font scale | 80–200%, with a dedicated UI font option |
| Colorblind modes | Protan/Deutan/Tritan + custom palette editor for map/ore/HUD |
| High contrast modes | Off/On + outline strength for interactables and ore |
| Map palette | per-element color customization; shape-based icons as fallback |
| Subtitles | size/background/opacity/speaker labels/position (`13`) |
| Screen reader | menus, shop, inventory, quest log (1.0 scope: UI text; world narration optional) |
| Text-to-speech | all dialogue text readable aloud (system voices) |
| Brightness/contrast/gamma | sliders + test pattern (`13`) |
| Flash reduction | caps strobe frequency; no content relies on flashing |
| Camera wobble reduction | see §1 |
| Photo-sensitivity warning | first-launch screen + content flags |

Ore and rarity are never identified by color alone: each has a **shape, icon and name label** option.

## 4. Hearing

- Subtitles for all dialogue and all significant sounds (default: all sounds), with directional
  indicators available as text ("drip — below-left").
- Visual equivalents for all audio tells: creature tells have a screen-edge indicator option
  (toggle), hazard tells have visual particles already (`08`).
- Mono audio; independent volume for dig loop, music, ambience.
- Vibration (controller) as an optional redundant cue for tells.

## 5. Cognitive and emotional

| Feature | Notes |
|---|---|
| Pause anywhere | including menus/dialogue; timers stop in single-player |
| No timed content by default | challenge timers only in Challenge mode and contracts, always opt-in |
| Quest clarity tools | objective line, map markers, "story so far", hint system (`12`) |
| Simplified controls preset | fewer verbs during early game (tutorial pacing) |
| Content warnings | horror card, flashing, "intense sequence" cards before the relevant zones |
| Anxiety-friendly options | creatures off, no jumpscares, no chase sequences, "nothing hunts you" mode |
| Arachnophobia/animal toggles | swap creature models for non-scary variants |
| No FOMO | no daily-login rewards, no expiring content; dailies are optional seeds |
| Readable pacing | "take a break" gentle reminder after 2 h continuous play |
| Skip/summary | every mandatory story beat skippable with a text summary |

## 6. Content toggles summary (single screen, no hidden options)

- Creatures: Off / Ambient / Light / Active (`08`)
- Horror: Off / Spooky / Full (`08`)
- Gore: Off / Reduced / On (default Reduced)
- Flashing: Normal / Reduced / Off
- Toilet humor: Off/On (default Off) — and the toggle covers **everything** including opening
  scenes and sounds; `[SPOT]`'s incomplete toggle is a named anti-pattern
- Arachnophobia mode
- Blood/gore decals off by default

## 7. Compliance and verification

- Target: **Xbox Accessibility Guidelines** and **PlayStation accessibility tags**, plus Steam's
  accessibility tags; publisher QA passes WCAG-adjacent checks for UI.
- **Full 100% completion run performed entirely with each major assistance enabled** (creatures off,
  no fall damage, infinite battery, auto-dig, mono audio, screen reader on) — achievements still
  unlock (`18`).
- Motion-sickness testers (self-identified sensitive) review each layer before content lock; their
  sign-off is a release gate for that layer.
- A public accessibility statement (web + in-game) listing every feature and its default.

## 8. Testable requirements

| Requirement | Verification |
|---|---|
| Every hold action has a toggle equivalent | Automated input audit |
| 100% of critical path completable with auto-dig + creatures off + infinite battery | Scripted assist run |
| No required content uses color alone | Colorblind simulation audit per UI screen |
| Screen reader reaches every menu and shop item | Manual SR test with NVDA/Narrator |
| Motion-sensitive testers can play 60 min without symptoms at Comfort preset | Moderated test |
| Content toggle changes take effect without save reload | Toggle matrix test |
