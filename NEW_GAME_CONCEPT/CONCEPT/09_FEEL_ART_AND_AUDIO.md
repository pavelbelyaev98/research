# 09 — Game Feel, Art and Audio

## 1. Visual style

Stylized painted low-poly (F01): strong silhouettes, restrained texture detail, painted gradients,
cohesive custom art. Bright and readable, never realistic mud, never asset-store clutter.

- **Zones read instantly:** strong palettes per zone with gradual transitions (F02).
- **Materials read by shape as well as color**, so colorblind players can still tell ground apart.
- **Objects read by silhouette**, because recognition is the core reward (D07).
- No AI-generated images or textures; custom Blender models, art direction owned by one style guide
 (A01).

## 2. Zone palettes and mood

| Zone | Palette | Lighting mood |
|---|---|---|
| Recent fill | Warm browns, greens, rusty metal, bright sky | Warm daylight, open, hopeful |
| Old sediment | Grey-blue, clay orange, dull steel | Cool daylight fading, nostalgic |
| Deep clay/stone | Saturated clay reds, dark rock, wet gleam | Dim, lamp-friendly, heavy |
| Ancient constructed | Cold tones, unnatural smoothness, faint glow accents | Near-black ambient, lamps essential (reached gradually) |

Darkness escalates gradually across the zones; readability always wins over mood (W03, F09).

## 3. The absurdity, visually

Absurdity is controlled and deadpan (F03):

- The machine escalates into a welded, bolted, over-batteried monster (F11).
- Objects are placed straight-faced; the jokes are in what they are and what they are worth.
- Physical comedy is allowed: pile wobble, a car yanked out of the ground, the Sell All machine
 visibly struggling with a haul.
- No random wackiness, no jokes baked into every texture, no cartoon eyes on the drill.

## 4. Dig feel

Chunky, weighted and steady (F05):

- Each bite removes a readable chunk; dust and crumbs follow.
- The camera never shakes or jerks from digging. No motion effects are added just to have toggles
 for them.
- Audio is per material: sand hisses, clay thumps, rock cracks, concrete grinds (F12).
- The machine's behavior and sound improve with upgrades, so power is felt in the hands, not read
 from a stat screen.
- Downward digging feels good with the starting shovel; upgrades make it feel ridiculous.

## 5. Material behavior

Each material family has a distinct response profile (F12):

| Material | Bite | Residue | Sound |
|---|---|---|---|
| Dry sand | Fast, prone to spilling | Pours, no clumps | Soft hiss |
| Soil | Even | Crumbs | Dull thud |
| Clay | Sticky, slower | Clumps that stick | Wet thump |
| Gravel | Trickles | Loose stones | Rattle |
| Compact sediment | Resistant, steady | Flat chips | Muffled crunch |
| Rock | Slow, chipping | Shards | Sharp crack |
| Concrete | Very tough for early tools | Sparks, dust | Grinding screech |

## 6. Audio design

Ambience and feedback only. **No music. No voice acting** (F06, Q22b).

- **Zone ambience layers:** wind and distant water near the surface; drips and settling rock deeper;
 a low, almost-silent hum in the ancient zone. Layers crossfade with depth.
- **Action feedback:** dig loops per material, footsteps, jetpack thrust, C4 blast, machine
 interactions, pickup chimes, the Sell All machine's noises.
- **No audio-only clues.** Every sound that carries information has a visual counterpart. The
  detector is silent by design and readable while muted.
- **No threat-adjacent audio anywhere.** The deep zone hums; it never breathes, whispers, follows or
  stalks. Nothing in the mix implies a presence (Q13, `11_ENDING_AND_MYSTERY.md`).
- **Mix:** ambience stays under the dig loop; picking, digging and the Sell All machine are the
 loudest, most satisfying elements.
- Licensed audio may be used where needed, but custom is preferred; every sound is reviewed for
 long-session fatigue (A01).

## 7. FX policy

Comfort-safe effects (F08):

- Dust, crumbs, sparkles, smoke from C4, splash from water-adjacent areas.
- No screen shake by default, no blood or gore, no full-screen flashes, no chromatic aberration,
 no forced bloom.
- Particles never collide and never deal damage.
- Intensity is adjustable; nothing visually discomforting is mandatory.

## 8. UI art

Clear, readable, industrial-worksite in flavor (F10 direction: not retro, exact style TBD): stenciled
labels, simple type, high contrast, scale-friendly. UI never competes with the world; it stays out of
the way.

## 9. Photo-ready moments (by design, not by marketing)

The game should naturally produce absurd, striking screenshots: a ridiculous machine silhouetted in
a deep hole, a gramophone half-buried in pale sediment, a car mid-yank on a cable, a warm lamp pool
in a near-black zone. Photo mode (pause-only, HUD hidden) exists for exactly these moments
(I13).
