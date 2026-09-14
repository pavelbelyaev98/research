# 10 — Accessibility and Comfort

Accessibility here is core design, not a patch: this is a game about a body digging a hole, and the
body must be respected (Pillars 6–7). Every reviewed digging game in the reference set drew
avoidable complaints about hands, eyes, motion or pressure. This one does not.

## 1. Motion comfort (the genre's biggest issue)

| Setting | Default | Options |
|---|---|---|
| Field of view | 90° | 60–110°, unit toggle |
| Camera shake | Low | 0–100% |
| Head bob | Off | Off / subtle / on |
| Comfort preset | Available at first launch | One click applies FOV, no bob, no shake, soft transitions |
| Forced roll / camera lean | Never | Not a feature |
| Jetpack camera effects | None by default | Each effect has a toggle where it exists |

Design rules:

- No screen shake from digging, ever; shake only exists where it can be disabled (F05, F08).
- No cinematic camera takeovers, no rotating elevator shots on the critical path.
- Camera motion is smooth at any frame rate.
- A player who says "I get motion sick" in the first-launch wizard gets the comfort preset applied
 automatically.

## 2. Motor accessibility

- **Hold-to-dig** is the default; a **toggle** is available; an **auto-dig assist** keeps digging at
 the aim point while held (I10).
- Every hold action has a toggle equivalent.
- **One-hand presets** for left-only and right-only play, on keyboard/mouse and controller.
- **Full rebinding** of everything, including menus (I07).
- No QTE, no mashing, no rapid double-inputs, no precise timing anywhere in the critical path.
- Generous input buffering: inputs during animations are never dropped.
- Aim/placement assistance: snap-to-valid-surface placement for C4 and lamps, generous interaction
 radii, no pixel-perfect hotspots.
- No health management and no fall death: bigger falls only stagger you and knock the battery, and extreme falls trigger recovery (Q28), so nothing punitive happens while learning controls.

## 3. Vision

- **Colorblind palettes** for materials, ore, detector cues and UI, plus custom palette option
 (I09).
- **Shape + label redundancy** everywhere: no information is color-only (F12).
- Contrast and brightness options; the game is readable at both ends of the display range.
- **Subtitles for all significant sounds** (I09), including ambient tells, with size/background
 options (deferred until the text pass, I12).
- UI scale/font scale planned as an optional later addition (I12).
- Detector feedback is visual by design; the game is fully playable muted.

## 4. Hearing

- All dialogue-equivalent text is on screen.
- All informational sounds (station feedback, C4 placement confirm, pickup) have visual
 counterparts (F06).
- Ambience and SFX volume controls; a mono option is a planned addition if the audio pass supports
 it (I12 deferred).

## 5. Cognitive and emotional comfort

Zero-pressure design (I11):

- **Pause anywhere**, any time; no online requirement.
- **No timed content** in normal play (no countdowns, no day/night deadlines, no decay).
- **No missables**: story objects and display slots remain findable; nothing expires.
- **No FOMO**: no daily rewards, no limited events, no login streaks.
- **No jumpscares, no horror, no combat** (Q13). Dark areas exist but are calm, never scary.
- Intensity warnings are unnecessary by content policy, but a brief note about dark areas appears in
 the first-launch settings tour (I11).
- The return-power warning is informational, never panicky; recovery always protects the player's
 finds.

## 6. Difficulty

**One single difficulty, tuned fair** (Q25):

- The only failure state is running out of battery, and it costs a fee, not loot.
- No scaling enemies, no punishment for exploring, no twitch requirements.
- Assist options (auto-dig, toggle dig) do not disable achievements or content.
- The game has no "easy mode" because it has no unfair mode to compensate for.

## 7. Save safety as accessibility

Losing progress is a disability-comfort issue as much as a technical one (I14):

- Autosave continuously; 3 manual slots; loading restores the exact hole.
- No save loss, no terrain reset, no "fresh world with old purchases".
- Cloud saves arrive later without changing the save format.

## 8. Verification

- Motion-sensitive testers review every zone before content lock; their sign-off is a release gate.
- Assist-mode (auto-dig, toggle, muted, colorblind palette) full run must complete normally.
- All station interactions verified with controller only and with one hand.
- No content audit failure: no horror, no flashing, no forced camera motion on the critical path.
