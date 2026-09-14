# 07 — Questions, Round 5: Interface and Accessibility

Rules-level. Answer by ID; answers go to `02_DECISIONS.md`.

This round covers what the player sees and touches: HUD, tutorial, menus, controls, comfort and
accessibility. Art direction and production details come in Round 6.

---

### I01 — HUD contents
**Context:** The HUD must answer "can I keep digging?" instantly and otherwise stay invisible.
**Options:**
- **A)** Minimal: depth, bag count/capacity, battery, return warning. Detector feedback is diegetic
  (a light/glow on the tool). No minimap, no compass, no ore counters. *(Recommended)*
- **B)** A + a small detector indicator widget.
- **C)** Rich HUD (ore counts, timers, objectives).
**Recommendation:** A. `[KD]`'s clutter and blur and `[SPOT]`'s busy nights were complaints; the
important numbers here are exactly two (bag, battery) plus depth. Detector cues belong to the world.
> **ANSWER:**

### I02 — Tutorial and onboarding
**Context:** The loop is simple, but conventions (sell here, upgrade there, battery, saving) must be
clear without a lecture.
**Options:**
- **A)** Diegetic first loop: a short guided sequence — dig, collect, sell, buy one upgrade — with a
  skip option for experienced players; a compact pause reference always available. *(Recommended)*
- **B)** No tutorial; rely on the pause reference and exploration.
- **C)** Text popups for each first action.
**Recommendation:** A. `[KD]` was criticized for having no proper tutorial; `[SPOT]`'s vague quests
frustrated players. Keep it short and skippable.
> **ANSWER:**

### I03 — Pause menu
**Context:** The pause menu is the trust contract: settings, save state, quit, reference.
**Options:**
- **A)** Four tabs: Resume, Settings, Controls, Session info (depth/collected/playtime); save status
  shown; ESC/B closes everything correctly. *(Recommended)*
- **B)** Minimal resume/settings/quit.
- **C)** Console-style radial menu.
**Recommendation:** A. Every reviewed game had a menu complaint (ESC behavior, settings persistence);
a simple tabbed menu with correct back behavior is cheap and expected.
> **ANSWER:**

### I04 — Inventory UI
**Context:** Inventory is abstract; its screen is for looking at what you found, not managing it.
**Options:**
- **A)** A grid of collected finds with name and a short inspection line; no stats, no equipping, no
  sorting chores; selling only at the machine. *(Recommended)*
- **B)** A plain list.
- **C)** No inventory screen; bag count only.
**Recommendation:** A. Inspecting finds is part of the reward; the display wall and inspection screen
are the two places where "what did I find?" gets its moment.
> **ANSWER:**

### I05 — Selling interaction
**Context:** Selling must be fast and funny, not a deposit chore.
**Options:**
- **A)** Walk to the Sell All machine, press one button, everything sellable is processed with a
  physical animation and money feedback; individual selling available from the machine for
  old-fashioned players. *(Recommended)*
- **B)** Sell All only.
- **C)** Manually feed items one by one.
**Recommendation:** A. `[AGADH]`'s missing quality-of-life on selling and `[MELT]`'s trip friction
make one-button selling mandatory; the animation keeps the physical comedy.
> **ANSWER:**

### I06 — Purchase sequence rule
**Context:** Can a player with a lucky rare find skip upgrade levels?
**Options:**
- **A)** Strict sequence: you always buy the next level of a track, never skip. *(Recommended)*
- **B)** Free buying: any affordable tier can be purchased immediately.
- **C)** Sequence with visible previews of what every future level does.
**Recommendation:** A. It keeps pacing predictable and prevents one lucky find from deleting the
economy; `[SPOT]` showed that tier-skipping and permanent gating both hurt. A and C can combine.
> **ANSWER:**

### I07 — Controls defaults
**Context:** Basic input comfort is a hard requirement, not an upgrade.
**Options:**
- **A)** Hold-to-dig default plus a toggle mode, full rebinding for every action, controller parity,
  left-handed preset, sensitivity options, gyro optional. *(Recommended)*
- **B)** Same but no controller parity (mouse/keyboard focus only).
- **C)** Fixed defaults.
**Recommendation:** A. `[AGADH]`'s click-spam and `[OMT]`'s broken controller support are named
anti-patterns; controller support is already mandatory (Q19).
> **ANSWER:**

### I08 — Motion comfort
**Context:** Every reviewed game drew motion-sickness complaints, even non-VR ones.
**Options:**
- **A)** Full suite at launch with safe defaults: FOV slider, camera shake 0–100% (default low), head
  bob toggle, comfort preset, no forced roll; settings persist. *(Recommended)*
- **B)** Basic FOV + shake.
- **C)** No options.
**Recommendation:** A. `[AGADH]` had 31 FOV mentions including vertigo; `[MELT]` had no
motion-sickness options and lost purchases; `[SPOT]` caused nausea unusually often. This is the
cheapest refund-prevention in the project.
> **ANSWER:**

### I09 — Readability and color
**Context:** Materials, ores and cues must never rely on color alone.
**Options:**
- **A)** Colorblind palettes for material/ore labels and detector cues, shape + label redundancy,
  contrast option, subtitles available for all significant sounds. *(Recommended)*
- **B)** Colorblind palette only.
- **C)** None.
**Recommendation:** A. The detector is visual and silent; it must also be readable with reduced color
vision and muted audio (the game is ambience-only, so some players will play muted).
> **ANSWER:**

### I10 — Motor accessibility
**Context:** The genre's core action must not hurt hands or require fast inputs.
**Options:**
- **A)** Auto-dig assist, hold-to-dig, toggle holds, one-hand presets, no QTE/mashing anywhere,
  generous input buffering. *(Recommended)*
- **B)** Remapping only.
- **C)** None.
**Recommendation:** A. `[AGADH]` RSI warnings and `[MELT]`'s shovel click-spam are the evidence.
> **ANSWER:**

### I11 — Cognitive and emotional comfort
**Context:** Nothing should pressure the player except the battery they chose to spend.
**Options:**
- **A)** Pause anywhere, no timed content in normal play, no missable objects or story, modest content
  warnings (darkness/intensity), no FOMO systems, no daily chores. *(Recommended)*
- **B)** Add optional timed challenges.
- **C)** Pressure by default.
**Recommendation:** A. `[SPOT]`'s unskippable sections and `[AGADH]`'s unlabelled finale are the
cautionary tales; this game's promise is "you can stop whenever you want".
> **ANSWER:**

### I12 — Text and screen support
**Context:** Small studio, but text is core.
**Options:**
- **A)** UI scale, font scale, subtitles for all significant sounds, controller-navigable menus, screen
  reader support for menus if feasible. *(Recommended)*
- **B)** Basic text size only.
- **C)** Full narration everywhere.
**Recommendation:** A. Keeps scope sane while covering the highest-impact needs; `[MELT]`/`[SPOT]`
suffered from tiny, low-contrast UI.
> **ANSWER:**

### I13 — Photo mode and streamer support
**Context:** Absurd visuals are a marketing engine; players and streamers will want clean shots.
**Options:**
- **A)** Simple pause-only photo mode: hide HUD, free camera around the player, FOV, basic filters,
  watermark toggle. *(Recommended)*
- **B)** No photo mode.
- **C)** Advanced director tools.
**Recommendation:** A. Cheap, delightful, and directly serves the "ridiculous for thumbnails" goal.
> **ANSWER:**

### I14 — Save UX
**Context:** Per-save randomized worlds mean multiple runs; saves must be trustworthy.
**Options:**
- **A)** Autosave at checkpoints/sales + 3 manual slots + Steam Cloud + settings persistence.
  *(Recommended)*
- **B)** Single rolling save.
- **C)** Manual saves only.
**Recommendation:** A. Save loss/cloud absence is a top complaint across the reference set; the cost
of doing it right is small.
> **ANSWER:**

### I15 — Achievements
**Context:** Achievements should be a fair record of play, not a second job.
**Options:**
- **A)** One-run achievable, deterministic, no NG+ locks, no host-only, no "no cheating" detectors,
  mostly discoveries/upgrades/actions players naturally do. *(Recommended)*
- **B)** Minimal set (10–15).
- **C)** No achievements.
**Recommendation:** A. `[AGADH]`'s NG+-locked achievements, `[MELT]`'s 45/46 bug and `[SPOT]`'s
hostile ones are all named anti-patterns; fairness here is a differentiator.
> **ANSWER:**

### I16 — Content disclosure
**Context:** Honest store copy prevents the "cozy game betrayed me" review wave.
**Options:**
- **A)** Store page states plainly: absurd excavation, dark areas, no horror, no combat, one
  difficulty, 3–5 h. *(Recommended)*
- **B)** Minimal tags.
- **C)** Trailer-only marketing.
**Recommendation:** A. `[OMT]`'s unadvertised horror and `[AGADH]`'s "advertised as cozy" backlash
are the two most cited trust failures in the set.
> **ANSWER:**

---

## Answer sheet
> I01: | I02: | I03: | I04: | I05: | I06: | I07: | I08:
> I09: | I10: | I11: | I12: | I13: | I14: | I15: | I16:
