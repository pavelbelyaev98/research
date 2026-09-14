# 14 — Prototype and Validation Plan

Purpose: prove the loop before content exists. Numbers are not designed on paper (Rule 8); they are
discovered here.

## 1. The core hypothesis to test

> A player will repeatedly choose "one more thing" over going home, because the detector hint, the
> partial silhouette, and the next affordable upgrade all pull harder than the battery warning.

If that experience does not occur in the prototype, nothing else matters yet.

## 2. Vertical slice scope (first playable)

| Element | Slice version |
|---|---|
| Site | One diggable area, full voxel, boundaries visible (concrete + bedrock) |
| Tool | One machine, 2–3 upgrade levels with visible bolt-on changes, hold-to-dig, automatic material adaptation stub |
| Materials | 3 distinct families with different feel (e.g., soil, clay, rock) |
| Detector | One prototype presentation (tool reaction + edge hint) and one silent distinctive find |
| Objects | The five first-slice objects: washing machine, hand drill, gearbox, mammoth bone, gramophone |
| Clusters | One template (bone scatter or vehicle parts) |
| Hard pockets | One concrete plug with two solutions (power or C4) |
| Pressure | Shared battery, return-power warning, recovery fee + debt |
| Economy | Sell All machine, two tracks (Tool, Battery), 1–2 purchases each, transparent shop |
| Display | One row of outline frames; place the first find; empty frames visible, shapes hidden |
| Surface | Compact yard: shaft, machine, bench, fuel, display |
| Interface | Minimal HUD, inspect grid, pause, full rebinding, controller support |
| Saving | Autosave + restore exact hole (already in demo) |
| Story | One anachronistic junk object for the mystery trail |

Explicitly out of the slice: zones 2–4, the full roster, the ending, achievements, photo mode, late
sinks, large-object extraction.

## 3. Experiments (numbers to discover)

- Voxel size vs. dig satisfaction and recognition readability (W11).
- Starting shovel speed vs. frustration; upgrade step sizes.
- Battery drain per stroke vs. desired session length; recovery frequency.
- Bag capacity vs. trip length; where the hard stop actually lands.
- Detector range, frequency, quiet intervals; how often players follow cues.
- Recognition: exposure percentage at which players identify each of the five objects.
- Cluster spacing: how far players search after finding one related object.
- Hard pocket: how many attempts before players leave and return later.
- Rare find value: how many expeditions a "big find" should equal.
- Station time: seconds spent in the yard per trip.

## 4. Validation metrics (playtest gates)

| Metric | Target |
|---|---|
| First noteworthy discovery | within the first 10 minutes, every seed |
| Voluntary lateral digging | the majority of testers dig sideways at least once per session unprompted |
| Recognition quality | ≥ 80% of testers correctly name slice objects from partial exposure |
| Voluntary full uncovering | ≥ 70% choose to keep revealing an interesting object rather than skip it |
| Purchase cadence | a meaningful purchase every 30–45 min |
| Trip decision | testers report the go-home-or-continue moment as tense, not annoying |
| Return friction | yard + return time ≤ ~15% of session time |
| Station clarity | no tester asks what the Sell or Upgrade stations do after using them once |
| Recovery | feels like an emergency, never like a shortcut |
| Save integrity | zero lost holes, inventories or display states across interrupted sessions |
| Feel | no floating snags; no unreachable pickups; no stuck spots |
| Performance feel | no cold-start hitch on the first dig; stable frame pacing while digging; no progressive decay across a long session (F13) |
| Return navigation | testers find their way back to the surface unaided; none report feeling lost (W13) |
| Mystery tone | testers describe the deep zone and the impossibilities as awe and curiosity, never dread (Q13) |

## 5. The core test script (observe, don't explain)

1. New player, no tutorial, unguided 30 minutes.
2. Observe: what they dig, whether they follow cues, when they first return, how they react at each
 station.
3. Inspect the resulting hole: shape, lateral branching, abandoned pockets.
4. Interview: what they remember finding, what they wanted next, what annoyed them.
5. Compare against the metrics above; adjust content distribution and feedback before adding content.

## 6. Build order

1. **Feel prototype:** dig, materials, cleanup, battery, recovery. No economy, no art.
2. **Loop prototype:** sell, upgrade, display, detector, first object recognition.
3. **Slice:** all vertical-slice elements above with placeholder art (custom models only per A01).
4. **Pacing pass:** multiple seeds, measure the metrics, tune generation rules.
5. **Content production:** zones 2–4, full rosters, mystery trail, ending.
6. **Polish and release prep:** comfort settings, achievements, verification passes.

## 7. Release gates (design-side)

- Core test moment observed repeatedly in external playtests.
- All validation metrics met or consciously waived by the developer.
- Muted + auto-dig + controller-only full run completes with no blockers.
- Clean-save 100% completion verified (achievements, display, tracks, zones).
- No save-loss, no terrain reset, no stuck states, no unreachable finds.
- Session-length stress run keeps dig rhythm stable: no shader or streaming hitch on the normal
  digging path (F13).
- Return navigation: testers get back to the surface unaided; no lostness or stuck reports (W13).
- Mystery tone check: testers read the impossibilities as wonder, not threat (Q13).
