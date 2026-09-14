# 23 — Scope, Roadmap and QA

## 1. Scope principles

1. **Polish beats breadth.** Every system in the five played games that shipped half-finished became
   a review theme. Scope is sized so that everything at 1.0 is finished.
2. **Content is authored, systems are engineered.** Landmarks, lore and audio are hand-made;
   terrain, placement and contracts are systematic.
3. **Co-op is out of the critical path until 1.0 ships** (`16`), because it multiplies QA and is
   the most common source of "broken" reviews.
4. **No Early Access by default** (`19`).
5. **Everything has an owner and a test.** No feature is "done" without an automated or scripted
   verification (`§6`).

## 2. Team shape (indicative, 15–18 months)

| Role | Count | Focus |
|---|---|---|
| Design lead | 1 | Pillars, economy, loop |
| Level designers | 2 | 70 POIs, landmark kits, gate logic |
| Gameplay engineers | 2 | Tools, voxel interaction, economy, saves |
| Engine/graphics engineer | 1 | Voxel renderer, performance, streaming |
| Tech artist | 1 | Pipeline, shaders, LOD, Deck |
| 3D/2D artists | 2 | Props, characters, UI |
| Audio designer/composer | 1 | Dig loops, ambience, adaptive music |
| Writers | 2 (part-time) | 12–16k main + ~30k lore words |
| Producer/QA lead | 1 | Milestones, telemetry, release gates |
| QA testers | 2 (+ external pass) | Soak tests, accessibility, full runs |
| Community/publisher liaison | 1 (shared) | Store page, demo, comms |

Total ≈ 15 people for ~18 months; budget assumes a premium indie scale. If the team is smaller,
the cut order is: co-op (already post-launch), daily seeds, some landmark families, ending variants
(3 → 2), creature roster (12 → 8).

## 3. Milestones

| Phase | Duration | Goal | Exit criteria |
|---|---|---|---|
| **P0 Prototype** | 2 months | Prove the dig feel | 10 testers can dig for 20 min with a placeholder shovel and report "satisfying" ≥ 4/5; frame-rate independence and save-delta proof-of-concept green |
| **P1 Vertical slice** | 3 months | One complete loop + one landmark + one upgrade tier + maps + settings | Full settings menu functional; 45 min of real gameplay; save/load round-trip with terrain; motion-comfort testers pass |
| **P2 Production** | 6 months | Layers 1–7 greyboxed, all tools, economy v2, story drafted | Internal 4-hour run with no blockers; economy telemetry within targets; art style guide locked |
| **P3 Content complete** | 4 months | All POIs, lore, audio, achievements, post-game modes | Content lock; all modes playable; localization strings frozen; Deck Verified candidate |
| **P4 Polish & cert** | 3 months | Balance, accessibility pass, demo, marketing | All release gates (`§5`) pass; demo certified; store page live |
| **P5 Launch + live** | — | Ship, then 12-month roadmap `[20]` | Post-launch monitoring; update cadence |

## 4. Vertical slice definition (what must be fun on its own)

- One 45-minute layer with a hand-built landmark, a gate key, one optional den.
- Full tool tier 1→2 escalation with visible changes.
- Complete UX: map, shop, respec, settings, accessibility, pause, save/load, Deck controls.
- One NPC arc and one artifact set.
- The exact performance budget, shader warm-up, and save architecture of the final game.

If the slice is not fun, **the design changes here**, not in production.

## 5. Release gates (all must pass)

### Gameplay
- [ ] Critical path 10–14 h; 100% 20–25 h; post-game content available at launch.
- [ ] No purchase dead-zone: ≥ 3 affordable purchases at all times after minute 5 (`06`).
- [ ] Final power upgrade at ~85% depth; all money sinks infinite afterward.
- [ ] No sequence disables tools; automated assertion in final sequence test.
- [ ] Horror/creature content 100% optional and off by default; critical path audit clean.

### Technical
- [ ] Perf budget met on min/recommended/Deck (`15`).
- [ ] 3-hour soak < 5% FPS drift; no memory growth beyond budget.
- [ ] Nightly kill-at-random save fuzz passes 100%.
- [ ] Cloud sync conflict scenarios tested; Deck ↔ PC round trip verified.
- [ ] Crash-free rate ≥ 99.5% of sessions in beta telemetry.

### Interface & accessibility
- [ ] 100% rebinding on all devices; left-handed/one-hand presets verified.
- [ ] Motion-comfort testers complete 60 min without symptoms at defaults.
- [ ] Screen-reader pass; colorblind audits; subtitle coverage 100%.
- [ ] Controller-only and assist-mode full runs complete.

### Content & business
- [ ] All 45 achievements grantable in a clean, assist-enabled run (`18`).
- [ ] All 70 POIs playtested; zero unfair geometry; map complete.
- [ ] Demo carries save into full game; store page tags/warnings accurate (`19`).
- [ ] Localization: EFIGS + RU/PL/PT-BR/zh-Hans/ja/ko/tr (or explicitly scoped and disclosed).
- [ ] Accessibility statement published; credits contain no-AI-assets statement.

### Review-risk audit (from the corpora)
- [ ] "Too short" risk: median tester playtime ≥ 10 h; critical path verified.
- [ ] "Performance" risk: no negative beta reports unresolved.
- [ ] "Save" risk: zero save-loss reports for 4 consecutive weeks before launch.
- [ ] "Cozy betrayal" risk: no unlabelled scary content anywhere.
- [ ] "Asset flip" risk: screenshot cohesion test ≥ 95%.

## 6. QA systems (build once, run forever)

| System | Tooling | Gate |
|---|---|---|
| Dig feel tests | Playtest protocol + input telemetry | Every milestone |
| Economy simulator | Offline bot player, Monte Carlo of builds | Every economy change |
| Save fuzzer | CI job: kill at random during autosave, verify recovery | Nightly |
| Perf soak | 3-hour scripted loop on min-spec + Deck | Nightly |
| Content audit | Script: horror tags, unbreakable walls, critical-path graph | Every content merge |
| Accessibility matrix | Automated input audit + human SR/motion tests | Every UI change |
| Achievement verifier | Scripted clean-run profile per achievement | Nightly |
| Locale smoke | Pseudolocalization + 12-locale boot test | Weekly |

## 7. Risk register (top risks and mitigations)

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Scope creep kills polish | High | High | Locked pillar checklist; cut order defined (`§2`); vertical slice gate |
| Performance debt from voxel renderer | Medium | High | Engine work in P0; soak tests from P1; budget as release gate |
| Economy tuning misses targets | Medium | High | Offline simulator; telemetry; 3 tuning passes before content lock |
| Co-op pulls resources from 1.0 | Medium | Medium | Co-op explicitly post-launch; hard gate in `16` |
| Review-driven anxiety causes overcorrection | Medium | Medium | Rules in `21`/`22`; changes classified per `20` |
| Localization debt | Medium | Medium | Strings externalized from P1; pseudoloc tests weekly |
| Update breaks old saves | Low | Very High | Migration tests N-3 → N; backups; no save-breaking class allowed |

## 8. Definition of done (one paragraph, for the whole game)

> The game is done when a new player can launch it, understand it in five minutes, dig for twelve
> hours without ever being punished for resting, choose any danger they want and none they don't,
> finish a story that respects what they built, keep playing forever in modes that ship with the
> game, and—at no point—lose a save, a tool, an item or an hour to a bug. That is the whole
> assignment. Everything in this folder exists to keep it that way.
