# 18 — Achievements

> Achievement disasters in the comparative set:
> `[AGADH]` — all achievements locked behind a second "achievement mode" playthrough ("INCREDIBLY
> scummy"), buggy counters, an RNG speedrun; `[MELT]` — the "all achievements" meta-achievement
> stuck at 45/46 forever; `[SPOT]` — false "no cheating" basketball detection, bugged collectathons,
> "clear all dirt" grinds; `[KD]` — host-only achievements in co-op (and, to its credit, an easy,
> fair 100% many players praised); `[OMT]` — broken reward achievements.
> Achievements are a trust contract. Ours are all obtainable, first-run, deterministic and tracked.

## 1. The ten rules of achievements

1. **Enabled from the very first launch.** No unlock wall, no NG+ requirement, no hidden mode.
   `[AGADH]` rule.
2. **All obtainable in a single playthrough** (NG+ optional). Completionism is a destination, not a
   replay tax.
3. **Mode- and setting-independent.** Cozy, assists, creatures-off, horror-off, infinite-battery
   runs can earn every achievement. `[SPOT]`/`[AGADH]` friction with difficulty is forbidden.
4. **Deterministic.** No achievement depends on RNG drops, random world placement, or luck.
   `[AGADH]` RNG speedrun, `[SPOT]` RNG collectathons.
5. **Retroactive and persistent.** Stat conditions are stored and checked on load; achievements
   unlock for conditions already met in older saves or after imports. `[AGADH]` one-of-ten
   registration failure is a P0 bug class.
6. **No false-positive detectors.** There is no anti-cheat or "no cheating" logic. The basketball
   equivalent (if minigames exist) always counts. `[SPOT]`.
7. **No host-only achievements in co-op.** Guests and hosts earn all shared achievements. `[KD]`.
8. **Progress is visible.** In-game achievement screen shows progress bars, hints ("How to earn"),
   and a "show on map" tie-in for location-based ones.
9. **Bounded effort.** No single achievement exceeds ~3 hours of focused effort for a competent
   player; "clear all dirt"-style goals are per-contract and never achievements.
10. **Localized, spoiled-safely.** Names/descriptions translated; hidden names revealed after
    unlock; no story spoilers in pre-unlock text.

## 2. Achievement set at 1.0 (~45 total)

| Category | Count | Examples (paraphrased) | Guarantee |
|---|---|---|---|
| Story progression | 8 | Finish each layer arc; see all three endings | Guaranteed |
| Milestones | 6 | First 1,000 coin; first 1,000 m; drill tier 6 | Guaranteed |
| Discovery | 10 | Activate all checkpoints; find each layer's landmark family signature | Deterministic |
| Museum | 6 | Complete each museum wing; assemble the fossil skeleton | Deterministic |
| Mastery | 6 | 100% a cave volume with no charges; no-damage layer descent; beat a challenge den | Skill, no RNG |
| Collection | 5 | Find all lore tapes; all artifact sets; all 7 prismatic ores | Deterministic placement |
| Social/flavor | 4 | Pet a mole 10 times; ride the lift 50 times; full photo album; sign the guestbook | Trivial/fun |
| Speedrun | 2 | Story% under a generous time (verified human-achievable, non-RNG), 100% under a generous time | Verified by dev playtesters |

Notes:

- The speedrun achievement's route is **stability-tested across ≥ 20 world seeds**; any RNG element
  is removed from the route, or the achievement is cut. `[AGADH]` "speedrun achievement is RNG".
- Meta-achievement ("all achievements") is included but grants only when the platform count and the
  internal stat total agree; it is tested against every platform's edge cases. `[MELT]` 45/46.
- No achievement requires online services or another player.

## 3. Implementation requirements

- **Stats system is authoritative**, achievements are derived; stats live in the profile and sync
  to cloud with the save (`15`).
- **Conflict handling:** if platform and local disagree, local stats win; achievements re-granted
  then pushed to the platform.
- **Offline earning:** achievements queue locally and push when online; no loss.
- **Test matrix:** for each achievement, an automated or scripted verification path; a nightly job
  asserts all achievements are grantable in a clean profile with default assists.

## 4. Co-op achievement rules

- Shared actions grant to all participating players within the session.
- Guests keep achievements in their own profile permanently; leaving mid-session still keeps earned
  ones.
- Party-save migration preserves every participant's achievements `[KD]` host-only rule.

## 5. Release checklist

- [ ] Every achievement has a deterministic test path in CI.
- [ ] Clean-save 100% run verified on all platforms before launch.
- [ ] Assist mode (creatures off, infinite battery, auto-dig) 100% run passes.
- [ ] Achievement UI shows progress + hints; localizations present.
- [ ] No achievement name or description spoils story content.
- [ ] Co-op scripted run grants every shared achievement to host and guest.
- [ ] Legacy-save import re-grants everything already earned.
