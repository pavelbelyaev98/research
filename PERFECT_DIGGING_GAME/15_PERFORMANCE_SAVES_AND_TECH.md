# 15 — Performance, Saves and Tech

> Technical failures are the comparative set's most damaging recurring theme:
> `[KD]` — "Solid 11fps on a 3070", "near zero optimization", "shaders compiling… every load",
> crashes and broken saves; `[MELT]` — 5–10 s autosave freezes, wiped saves, no cloud, a tutorial
> softlock; `[AGADH]` — fatal errors on selling/recharging/buying, the dug hole not saved at all,
> progress wiped by crashes; `[OMT]` — crashes, no autosave, FPS decay over time, falling through
> textures; `[SPOT]` — save loss, softlocks, drill speed tied to FPS.
> Every one of these is a **release blocker class** in this project.

## 1. Performance budget

| Tier | Target hardware | Target |
|---|---|---|
| Minimum | GTX 1050 / RX 560 / modern iGPU (Deck-class) | 30 FPS @ 720p low, stable frame pacing |
| Recommended | GTX 1060 / RX 580 / Deck | 60 FPS @ 1080p medium |
| High | RTX 3060+ | 120+ FPS @ 1440p high |
| Steam Deck | Verified | 40 FPS cap @ 800p medium, ≤ 15 W in-loop |

Technical requirements:

1. **Frame-rate-independent simulation.** Dig speed, movement, enemies and timers advance on a
   fixed timestep with delta-time; no gameplay value may read `1/fps`. `[SPOT]` "drill speed changes
   with fps" is a named anti-pattern with an automated regression test.
2. **Voxel engine:** chunked, greedy-meshed, jobs/burst parallel; mesh uploads budgeted per frame;
   no per-voxel GameObjects. Memory target: ≤ 2 GB VRAM at high, ≤ 4 GB RAM baseline.
3. **No shader-compilation walls.** Shader warm-up happens during the first launch "preparing
   world" screen (with a progress bar, skippable to menu), plus async precache per layer. Every
   subsequent launch must reach gameplay in ≤ 20 s on recommended hardware. `[KD]` "minutes of
   shader compilation on every launch".
4. **No FPS decay over time.** Chunk GC, pooled resources, bounded queues; a 3-hour soak test must
   show < 5% average-FPS degradation. `[KD]`/`[OMT]` FPS drains.
5. **No blur-by-default.** TAA sharpness slider, sharpening option, no forced bloom, no chromatic
   aberration; blurry-image complaints are a supported bug class `[KD]` "extremely blurry… unplayable".
6. **Crash-free operations.** Selling, buying, recharging and saving are covered by automated
   stress tests; `[AGADH]`'s "Fatal Error on selling ore" is a P0 bug class forever.
7. **No overheating spirals:** frame cap option, CPU thread control, "Eco" mode; `[MELT]` "heats my
   PC to 90 degrees" and `[KD]` "overheating" are explicitly designed against.

## 2. Save architecture (the most important system in the game)

### Data model

- **Everything persists:** terrain deltas (all dug voxels + placed objects), ore state, landmark
  state, quest flags, player, inventory, museum, cosmetics, map fog, settings, statistics.
  `[AGADH]` "saving only saves your tool upgrades not the hole you've dug" is the canonical failure.
- **Delta encoding:** chunks store diffs from the seed, not full copies; a 2,000 m world stays in
  the tens of MB, compressible.
- **Versioned schema** with forward migrations; every save carries app version + content version.

### Mechanics

| Requirement | Implementation |
|---|---|
| No save-time freeze | Save is serialized/compressed on a worker thread; only entity handoff touches the main thread (< 16 ms), with a subtle UI spinner, never a multi-second hitch `[MELT]` |
| Atomic writes | Write to temp → fsync → rename; keep 3 rolling backups + the last manual save |
| Autosave | Every 5 min, on layer transitions, on major purchases, on quit, after rescues; configurable |
| Manual saves | 5 slots + quick-save; saving during any state is legal |
| Crash safety | Journaled session delta; after a crash, offer "recover to 60 s before crash" |
| Cloud | Steam Cloud from day 1, with conflict UI (newest / local / cloud / merge-copy) `[AGADH]` `[MELT]` `[SPOT]` no-cloud complaints |
| Multi-machine | Settings + keybinds + save slots sync; Deck ↔ PC tested every patch |
| Corrupt-save recovery | Auto-detect, load latest good backup, explain what happened, never silently reset `[SPOT]` "saves disappeared?!" |
| Export/import | Versioned file export for support and for players |
| Save integrity test | Automated fuzz: kill process at 100 random points, verify recovery |

## 3. Crash and error handling

- Global crash handler with a readable report + one-click "copy for support"; local last-logs kept.
- **No fatal-error popups as normal UX.** Any reproducible crash on a core action is release-blocking.
- Safe mode: after 3 consecutive crash-on-launch events, offer safe graphics + reset settings.
- Network/Steam outages degrade gracefully (offline play always works).

## 4. Achievements and platform services

- Steam achievements are granted via a **retroactive stat system**: stats are saved in the profile;
  achievements unlock whenever their condition is met, including from old saves and imported saves.
  `[AGADH]` "only 1 of 10 achievements registered" and `[MELT]` "45/46 forever" cannot occur.
- No platform-service dependency for core play; no always-online requirement.

## 5. Loading and streaming

- Zero-load layers: the world streams in as you descend (single scene with chunked LOD; no
  per-layer loading screens that break pacing).
- Fast travel has a short, charming transition (≤ 3 s) with progress feedback; no black-screen
  hangs.
- Boot to menu ≤ 10 s, menu to play ≤ 20 s on recommended hardware (warm shader cache).

## 6. QA automation (must exist before content lock)

| Test | Frequency |
|---|---|
| 3-hour soak (memory, FPS drift, save size) | Nightly |
| Kill-at-random autosave fuzz + recovery | Nightly |
| Frame-rate independence matrix (30/60/144/uncapped) | Every build |
| Core-action crash sweep (sell/buy/save/travel) | Every build |
| Save-version migration (N-3 → N) | Every schema change |
| Deck suspend/resume + cloud sync | Weekly |
| Colorblind & UI-scale screenshot audit | Every UI change |

## 7. Telemetry (opt-in, anonymized)

- FPS percentiles per hardware tier, crash-free session %, save failure count, purchase cadence,
  trip length, mode/horror setting distribution, achievement completion.
- **No PII, no gameplay recording, clear opt-out**, and telemetry never affects gameplay balance
  without a public patch note (`20_LIVE_UPDATES_AND_DEV_PROCESS.md`).
