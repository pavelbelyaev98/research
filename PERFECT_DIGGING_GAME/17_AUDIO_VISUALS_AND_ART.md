# 17 — Audio, Visuals and Art Direction

> Praise themes to protect: "the sound effects (that satisfying shovel crunch!) actually make it
> relaxing" `[AGADH]`; "the sound design punctuates every strike… as though the Earth itself is
> reluctantly acknowledging my authority" `[KD]`; "the caves with all the glowing ice and crystals
> are truly beautiful" `[MELT]`; "the lighting that you can place… garlands of colors" `[OMT]`;
> "one of the few soundtracks I didn't mute after an hour" `[SPOT]`.
> Failure themes to kill: "blurry and dark" `[KD]`, "AI slop / mismatched asset store props"
> `[MELT]`, "assetflip / carbon copy" `[KD]` `[OMT]`, and forced bloom/blur that caused headaches.

## 1. Art direction: one cohesive world, zero asset-flip

**Style target:** hand-authored stylized low-poly with voxel terrain; painterly material ramps,
strong silhouettes, warm hub vs. cool depths. Think "cozy diorama that gets stranger the deeper
you go."

Hard rules:

1. **No mixed asset packs.** Every environment asset is authored or fully re-authored (repainted,
   re-lit, re-scaled) to the style guide. Marketplace assets may be used only as placeholders
   during production and must be on the cut list before content lock. `[KD]` asset-flip
   accusations and `[MELT]` "potion bottles in an ice world" mismatches are project risks we
   remove by policy.
2. **No AI-generated art, audio, text or VO at any point.** Disclosure is explicit in the credits
   and store page. The reputational cost (`[MELT]` "AI-slop" reviews) far exceeds any savings.
3. **Style guide is a build pipeline:** palette per layer, material chart, prop kit per landmark
   family, lighting rules, post-processing limits. Art review gates every new asset.
4. **Cohesion test:** a blind screenshot test — can reviewers tell all props belong to one game?
   Target ≥ 95% yes.

## 2. Readability and lighting

| Rule | Detail | Lesson |
|---|---|---|
| Player light is always sufficient | The critical path is never so dark that the player cannot navigate without placing lamps | `[KD]` "extreme darkness" |
| Contrast between diggable and non-diggable | Material shape + color + audio, never color alone | Accessibility |
| Ore is legible at a glance | Rarity via shape, glow, particle; optional outline | `[OMT]`/`[MELT]` sparkle praise |
| Layer palettes are distinct | Soil browns → stone grays → ruin teals → flood blues → prism violets → forge oranges → hollow blacks | `[MELT]` "all corridors identical" |
| No forced post-processing | Bloom off/optional; no chromatic aberration; no film grain by default | `[MELT]` `[KD]` |
| Blur is a bug | TAA implemented with sharpening; a "blurry" support ticket is actionable | `[KD]` |
| Landmarks glow with purpose | Each POI has a beacon read at distance ≥ 60 m | `[SPOT]` secrets density |

Performance constraints per layer: ≤ 2 texture atlases active, ≤ 600 draw calls in the loop,
≤ 350k visible triangles at high settings, LOD cascades for voxel chunks (`15`).

## 3. Audio direction

**Goal: the dig is the music.** The loop must sound satisfying with the soundtrack off.

| Layer of sound | Implementation |
|---|---|
| Dig by material | Unique, layered loops per material family (dirt, stone, metal, crystal, sand, mud); pitch rises subtly with tool tier; satisfying tail "schwoop" on pickup |
| Loot | Rarity chimes (short, non-fatiguing, randomized pitch ±5%); combo chimes for vein clears |
| Ambient by layer | Distinct beds: birds/soil creaks → distant drips → low stone groans → water → crystal hum → forge rumble → hollow silence with heartbeat |
| Traversal | Winch ratchet, jet whoosh, lift cable; all comfort-safe (no sudden loud transients near the player's head) |
| Creature/hazard tells | Unique, telegraphed, with a "visual tell" counterpart option `[08]` |
| Music | Ambient, adaptive, sparse; layer themes crossfade with depth; hub theme warm; **music volume can be zeroed without losing any cue** |
| Dig-loop control | Independent volume/mute (podcast players are the core audience; the community explicitly loves silent mining with audio off) `[KD]` "the lack of BGM was wonderful" |
| Mixing | Loudness-normalized (≤ -16 LUFS-I integrated for ambience, dialogue prioritized), dynamic-range modes, mono option |

Audio tells must never be the only warning for danger (`14_ACCESSIBILITY.md`).

## 4. UI and FX art

- UI is diegetic-ish: paper/wood/metal in the hub, miner's notebook style for map and archive,
  clean sans for settings.
- Ore/rarity palette uses shapes + icons; colorblind palettes are first-class (`14`).
- Particles: dust, sparkles, crumbs — **no particle has collision or damage** (`04` §5).
- Screen effects are minimal: subtle vignette slider, damage flash reduction option, no
  full-screen blobs that obscure gameplay.
- Photo mode (pause-only): FOV, filters, DOF, watermark toggle; content toggle for creators.

## 5. Art production budget

| Asset class | Count target | Notes |
|---|---|---|
| Layer environment kits | 7 | Palette + 25–40 props each |
| Landmark interiors | 24 | Reusable kits + 3 signature rooms |
| Tools + skins | 9 tools × 4 skins | Skins are visual-only, earned in-game |
| Creatures | 12 models (7 families) | Optional content, reuse rigs |
| UI icon set | ~180 | Consistent stroke system |
| Audio: dig loops | 6 materials × 3 tiers | Layered, mixable |
| Music tracks | 12–16 | Ambient, adaptive, 1 hub, 7 layers, 4 stings |
| Lore/audio logs | 18 voice-less (text) + ambience | No VO at 1.0 |

## 6. Quality gates

- [ ] Blind screenshot cohesion test ≥ 95% "one game".
- [ ] No marketplace asset without full re-authoring passes content lock.
- [ ] Credits and store page contain an accurate "no AI assets" statement.
- [ ] Dig sound test: 10 players, 1 hour, survey "satisfying?" ≥ 4.5/5.
- [ ] Contrast/readability audit in brightness extremes (calibrated dark and bright displays).
- [ ] Photo mode does not grant gameplay advantages and pauses single-player.
