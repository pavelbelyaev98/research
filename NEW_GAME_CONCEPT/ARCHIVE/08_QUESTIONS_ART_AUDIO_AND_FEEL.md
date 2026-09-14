# 08 — Questions, Round 6: Art, Audio and Game Feel

Rules and directions; asset counts and exact values are prototype/production decisions. Answer by ID;
answers go to `DECISIONS.md`.

This round defines how the game looks, sounds and feels moment to moment: visual identity, zone
palettes, absurdity, camera and hands, dig feedback, audio design, detector presentation and FX
policy. Production/tech is Round 7.

---

### F01 — Visual style
**Context:** Direction is bright, cartoonish, simple, readable; no realistic mud, no ugly procedural
surfaces, no asset-flip mix.
**Options:**
- **A)** Stylized low-poly with painted gradients; strong silhouettes; restrained texture detail;
  cohesive custom art. *(Recommended)*
- **B)** Minimal voxel look like the reference digging game (flat cubes, simple shading).
- **C)** Semi-realistic.
**Recommendation:** A. It supports readable object silhouettes (critical for the recognition loop),
ages well, and is achievable for a small team. B risks looking like a clone of the reference game;
C breaks readability and the humor.
> **ANSWER:**

### F02 — Zone visual identity
**Context:** Four depth zones must read instantly by color, material and mood, so the underground
never feels identical.
**Options:**
- **A)** Strong distinct palettes per zone: warm brown fill → grey-blue sediment → saturated clay/red
  stone → cold ancient/constructed tones, with gradual transitions. *(Recommended)*
- **B)** Subtle shifts only (more natural, easier to get lost).
- **C)** Hard bands with abrupt color changes (clear, but gamey).
**Recommendation:** A. `[MELT]`'s "all corridors look identical" was its most persistent complaint;
readable zone identity is the cheapest fix.
> **ANSWER:**

### F03 — The absurdity factor
**Context:** The game must feel ridiculous in a controlled way: garage-built machinery, oversized
attachments, objects that don't belong.
**Options:**
- **A)** Absurdity through the tool (visibly insane homemade additions) + object identity + physical
  comedy (objects falling out, pile wobble), not random wackiness. *(Recommended)*
- **B)** Grounded and dry; comedy only in item names.
- **C)** Maximal silliness everywhere (jokes in every texture).
**Recommendation:** A. `[AGADH]` succeeded because it was honest and committed to one joke executed
well; `[SPOT]`'s constant toilet humor polarized players. Controlled absurdity with deadpan delivery
is the identity.
> **ANSWER:**

### F04 — Camera and body
**Context:** First-person, no player model; hands and the tool carry the fantasy.
**Options:**
- **A)** Visible hands and the evolving tool; minimal idle animation; slight effort cues when digging;
  no full body. *(Recommended)*
- **B)** Tool only, no hands.
- **C)** Floating camera (nothing visible).
**Recommendation:** A. The tool is the progression fantasy; upgrading the same object is only
satisfying if you see it constantly.
> **ANSWER:**

### F05 — Dig feel
**Context:** One verb, used thousands of times. It must feel chunky, weighted and stable.
**Options:**
- **A)** Chunky bites with weight, dust and material debris, satisfying audio per material; camera
  steady, no jerk or shake; the machine feel improves with upgrades. *(Recommended)*
- **B)** Fast and quiet, minimal feedback.
- **C)** Realistic heavy machinery with vibration and screen shake.
**Recommendation:** A. `[AGADH]`'s crunch and `[OMT]`'s vacuum satisfaction carried those games;
screen shake and motion effects are the opposite direction for this audience.
> **ANSWER:**

### F06 — Audio design
**Context:** Ambience + action feedback only; no music; no VO; sounds must never be the only clue.
**Options:**
- **A)** Layered environmental ambience per zone (wind, water, distant rumbles) + per-material dig
  loops + pickup/station feedback. Every audio cue has a visual counterpart. *(Recommended)*
- **B)** A + a sparse optional music layer off by default (already decided against music).
- **C)** Minimal sound (digs only).
**Recommendation:** A. `[KD]` players actively praised mining with no music; the environment doing
the scoring fits the fantasy, and ambient layers make depth feel different.
> **ANSWER:**

### F07 — Detector presentation
**Context:** Cues are silent and never reveal value; they must be noticeable but not annoying.
**Options:**
- **A)** Diegetic and subtle: the tool emits a faint glow/shiver, plus a soft edge-of-screen shimmer
  that grows as you approach the target's general direction; one target at a time. *(Recommended)*
- **B)** An on-screen compass/dot pointing at the nearest target.
- **C)** Audible pings (optional audio ticks).
**Recommendation:** A. B becomes a treasure GPS; C conflicts with the no-audio-clue rule and the
ambience-only soundscape. A keeps the "hunch" feeling that makes discovery feel earned.
> **ANSWER:**

### F08 — FX policy
**Context:** Effects must serve readability, never discomfort.
**Options:**
- **A)** Dust, crumbs, sparkles, smoke from C4; no screen shake by default, no blood/gore, no
  full-screen flashes; all intensity options adjustable. *(Recommended)*
- **B)** Cinematic effects with shake and flashes.
- **C)** No effects at all.
**Recommendation:** A. `[MELT]` and `[KD]` drew headaches from forced effects; here every effect is
optional or comfortable by default.
> **ANSWER:**

### F09 — Lighting mood per zone
**Context:** Sky light fades with depth; placed lamps matter; dark areas exist but are never pitch
black.
**Options:**
- **A)** Zone moods: bright warm daylight near the surface → cool dim dug depths → near-black ambient
  in the deepest layer where lamps become essential; lamps provide warm pools of readable light.
  *(Recommended)*
- **B)** Uniform lighting at all depths.
- **C)** Random lighting shifts.
**Recommendation:** A. It gives depth a physical feeling and makes lamp placement meaningful, while
the ambient floor prevents the "unreadable darkness" failure.
> **ANSWER:**

### F10 — UI art style
**Context:** Menus, shop, inventory and display labels need an identity consistent with the world.
**Options:**
- **A)** Clean, industrial-worksite style: stenciled labels, metal/paper textures, simple readable
  type. *(Recommended)*
- **B)** Skeuomorphic paper notebook.
- **C)** Retro pixel UI.
**Recommendation:** A. It matches the reservoir worksite fantasy, stays readable at any resolution,
and avoids the "generic sci-fi HUD" look.
> **ANSWER:**

### F11 — Tool escalation visuals
**Context:** The tool is the progression story: normal shovel → absurd homemade machine.
**Options:**
- **A)** Visibly bolted-on parts at each major level: motors, batteries, bigger heads, pipes, a
  ridiculous late nozzle; the silhouette grows; one continuous object. *(Recommended)*
- **B)** Clean replacement models (a new tool every tier).
- **C)** Stat changes only, same model.
**Recommendation:** A. `[MELT]`'s bolt-on upgrades were specifically praised; `[OMT]`'s
"different colored vacuum" skins were mocked. The garage-project look is the identity.
> **ANSWER:**

### F12 — Zone-specific material feedback
**Context:** Materials must be recognizable by how they look, sound and dig, not just color.
**Options:**
- **A)** Each material family has distinctive chunk shape, dig audio, particle and resistance
  response (sand pours, clay sticks, rock chips, concrete sparks). *(Recommended)*
- **B)** Color/texture differences only.
- **C)** Identical behavior, cosmetic differences.
**Recommendation:** A. It makes material changes readable to colorblind players and makes "the ground
changed" a felt discovery rather than a palette swap.
> **ANSWER:**

---

## Answer sheet
> F01: | F02: | F03: | F04: | F05: | F06: | F07:
> F08: | F09: | F10: | F11: | F12:
