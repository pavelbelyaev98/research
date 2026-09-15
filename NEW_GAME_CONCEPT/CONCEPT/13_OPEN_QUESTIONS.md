# 13 — Open Questions

Everything intentionally undecided, with its current options and recommendation. None of these block
prototyping. When one is decided, it moves to `../DECISIONS.md` with a status.

## Content and systems

| ID | Question | Current options | Recommendation / note |
|---|---|---|---|
| D03 | What are distinctive finds ultimately for? | First copy to display with duplicates sold / sell-only with snapshot / notable-signal-only split | Deferred by developer. Principle fixed: **no keep/sell choice per item**; each type has one fixed purpose. Recommendation on record: first copy displays, duplicates sold; a notable-distinctives-only split is the bounded middle path |
| D14 | When does a unique's one-sentence story appear? | On pickup / on inspection / both | Deferred; the story itself is confirmed (D14) |
| S10 | How do passive upgrades work? | Find-or-buy (rare find grants a track tier) / find-only / buy-only | Deprioritized until a playfeel review; find-or-buy still leading. Constraint: passive/unique effects must preserve challenge — no sudden power spikes |
| S09 (late) | Does the machine converge to one vacuum head, or keep adaptive behaviors to the end? | Convergence / perpetual adaptation | Automatic adaptation + late convergence is the working rule; validate in playtest |
| Q32 | Social hooks for a solo game (netcode-free) | None / seed and hole-code sharing / display-wall snapshots or postcards / friend records and depth boards / co-op later | Research-derived: Keep Digging's #1 praised feature is co-op (top reviews are friend groups); co-op requests also appear in AGADAH and The Spotter. Q24 is re-opened for decisioning; if co-op stays out, decide whether any cheap social hook is wanted. Cheapest candidate: a photo-mode postcard export (seed code, hole depth/shape, favourite find) — offline, shareable, and impossible to mistake for online play |
| S13 | What is a second run? | Cold start per save (current Q18) / cosmetic and record carryover / gear-carrying reset after credits / seed signature sets (per-seed rare family + mystery flavor) / endless strata (already deferred) | Keep Digging's gear-carrying reset was widely praised; pillar 5 promises replayability. Candidate identity hook: per-seed signature sets give a second run a distinct known-unknown without meta-progression. Decide after the first playtest |
| S14 | Fall penalty severity (re-opening the Q28 direction) | Keep stagger + battery knock (current) / reduce to stagger only / no knock outside extreme-fall recovery | Keep Digging players praised no fall damage and disliked the patch that added fall death; this audience may read any fall penalty as stress. Prototype it |
| S15 | Exploit policy for duplication/value loopholes | Fix every value exploit / allow harmless physics comedy only / embrace all as community culture | Recommendation: any exploit that creates money or skips a purchase is fixed; purely physical comedy that cannot move value may stay; by construction, value never grows by combining (`06` §8) |
| D01/D02 | Exact common and distinctive rosters | — | Counts fixed (20–30 / 30–50); the object lists are content design |
| — | When does the final meaningful purchase land? | ~75–85% of first completion | Prototype-tuned |
| — | Zone names | — | Content work; placeholders in use |
| — | Post-ending endless dig mode | Optional post-credits endless strata / Continue Playing only / more authored post-game content | Deferred: feasibility of chunked procedural strata + save handling must be proven in a prototype spike before deciding. Evidence: AGADAH's most-upvoted review asks for it; Digger: Galactic Treasures' post-launch Grandpa's Farm bonus level (a 100+ layer Infinity Tunnel) was celebrated by hardcore players as a pure-digging outlet decoupled from progression; Hydroneer's most repeated long-term criticism is that the game is "pretty much over" once automation is done — late sinks + Continue Playing are the in-run answer; endless mode stays deferred pending the spike |

## World and art

| ID | Question | Current options | Recommendation / note |
|---|---|---|---|
| W01 | Site footprint (depth floor fixed at ≥100 m) | Compact vertical / wider / other | Exact depth and footprint set by feel in playtest; keep the footprint contained |
| W04 | Exact material list | 5 / 7 / 9+ families | 7 families proposed; must feel distinct per F12 |
| W11 | Voxel/chunk size | 0.5 m / 0.25 m / 1.0 m | Prototype-tuned; affects feel, recognition and performance |
| F07 | Detector presentation | Hybrid tool glow + edge hint / edge indicator only / tool reaction only | Deferred; options documented; decide with a prototype and review research |
| F10 | UI art style | Industrial-worksite / other | Clear, not retro; exact style later |
| W13 | Return-path navigation in a free-form hole (supports Q27's no-return-aids rule) | Current mitigations only (sky-lit shaft, lamps, depth readout, detector) / terrain repack or "spit dirt" ability / route-marker tool / consumable ascent aid | Meltopia's #2 complaint is getting lost (no map, tunnels all alike); One Man's Trash reviewers praised rebuilding staircases with spat-out dirt as the best QoL over AGADAH; Keep Digging players used save-and-exit as an elevator. Requirement on record: legibility, not a map widget. Recommend a return-navigation prototype metric and a terrain-repack spike. Prototype/release gates now in `14_PROTOTYPE_PLAN.md` §4/§7 |
| F13 | Performance-induced hitch feel (shader compilation, terrain streaming, late-session FPS decay) | Treat as a feel requirement with a prototype budget (cold-start hitch, stable dig rhythm) / accept / dedicated spike | Biggest cross-corpus negative: Keep Digging optimization 130 EN mentions (86 negative), 5–15 FPS reports, a 53-upvote shader rant; Meltopia freeze/stutter 78; Digger: Galactic Treasures synchronous save freezes (15–60s) on voxel serialization. Production targets stay parked; this is about feel and recognition rhythm. Rule on record: optimization work must never alter existing saves' behavior. Prototype/release gates now in `14_PROTOTYPE_PLAN.md` §4/§7 |

## Interface and production-adjacent (design-owned)

| ID | Question | Current options | Recommendation / note |
|---|---|---|---|
| I03 | Pause menu tabs | Resume / New Game / Settings / Exit | Direction fixed; exact tabs later |
| I12 | Text scale and screen reader | Optional later | Not needed for first playable; add if budget allows |
| I17 | Where the player loads in after quit/reload | Resume where saved / resume at the surface / resume at the shaft rim with a cost | Quit-reload as a free elevator would erase the battery trip tension (Keep Digging players used save-and-exit to teleport up). Decide before the prototype save pass |
| — | Ending staging | One ending / variants | Default assumption: one ending; not decided |
| — | Final object identity | Ancient household tech / modern machine in ancient materials / an ancient original of the player's own machine / other | Direction locked; object chosen after the loop works. Candidate: an impossibly ancient original of the player's escalating machine — the shovel-cannon's ancestor — so the finale rhymes with the one-machine pillar |
| — | Achievement final list | 5–10 candidates listed | Finalize with content |
| — | Exact tuning values | All numbers | Rule 8: tuned in prototype, not on paper |

## Parked (explicitly out of scope until later)

- Localization languages (business/production).
- Store copy, tags, trailer, demo timing (marketing).
- Steam Cloud timing (production).
- Performance targets (production).
- Pricing beyond the working $6.99–9.99 range (business).

## Decided-by-delegation, confirmed

The setting (drained river-fed reservoir, Danube-style news motivation), the core fantasy retention,
and the complete-1.0 release approach were proposals the user explicitly confirmed (C01–C03). They
are not open.
