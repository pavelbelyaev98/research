# 00 — Source Audit: `LEGACY/OLD_IDEA.md`

**Source:** "Something Down There", 1,432 lines, 54 sections, authored by an earlier AI with embedded
notes from user sessions (dated 2026-09-12 etc.).
**Audited:** 14 September 2026.
**Process role:** raw material only. Nothing in it is binding unless you confirm it (see `Q01` and the
L-register in `02_DECISIONS.md`). This audit extracts what is strong, what conflicts, and what the
document never answers.

---

## 1. One-paragraph summary of the legacy idea

A short first-person excavation game: a drained reservoir, free-form digging with no pre-dug holes, a
single evolving shovel from normal to absurd homemade machinery, a passive silent detector that cues
curiosity toward non-minor finds, recognition-based reveals ("...oh, it's a chushkopek"), an abstract
inventory, selling only at the surface with a physical Sell All machine, a shared digging/jetpack
battery, rescue at zero fuel, 2–3 h completion, randomized discovery placement per save, a
screenshot "fridge" of first finds, a slow-build mystery that ends in something impossible, and
"Continue Playing" after the ending. Tone: fun/absurdity/curiosity first, relaxation second; bright
cartoon art; ambient audio only, no music, no VO.

## 2. What kind of document this is (credibility notes)

| Observation | Implication |
|---|---|
| It is an accumulated revision log, not a clean spec: lines address a developer/AI ("Preserve…", "The user selected…", "Current user verdict…") | Treat as a diary of decisions and experiments, not an authority |
| It references artifacts absent from this repo: "the report", "Sunny r8" art, test fixtures, a playable field with "928 minerals and 96 rocks", old 12 m saves, a four-mode excavator, trial sounds | All "implemented/exists" claims are **unverified historical claims** |
| Line 3 says "A research proposal is not a selected mechanic" while dozens of sections declare decisions "selected" or "locked" | Global ambiguity; resolved by Q01 (nothing is binding until confirmed) |
| Contains explicit "reopened/undecided/deferred" markers (distinctive-find purpose, ending object, C4 inclusion, gun endpoint, tutorial, condition system) | These are genuine open questions and go into the question bank |

## 3. Internal contradictions and unresolved states (C-list)

| ID | Contradiction / ambiguity | Where |
|---|---|---|
| C01 | Global status: "not a selected mechanic" vs. pervasive "selected/locked" language | line 3 vs. §6, §37, §44 |
| C02 | Unverifiable references to an existing implementation (minerals count, r8 art, old saves, experimental tools) | §6, §9, §12, §44 |
| C03 | Setting says reservoir "explicitly selected 2026-09-12" but boundary language, materials and art are still open; riverbed/waterworks listed as prior alternatives | §6 |
| C04 | Final toolkit unknown: one evolving shovel + "guns intended later" + experimental four-mode excavator + "Shave" preference | §9, §46, §53 |
| C05 | Distinctive finds: purpose, frequency and retention **explicitly reopened**; sale-plus-photo is only a "comparison baseline" | §12, §28 |
| C06 | Detector: currently must be silent; earlier beeping/stereo concept deferred; "exact presentation needs review" | §16, §18, §50 |
| C07 | Rescue: ordinary loot lost + fee, but "fee should never ruin a save"; exact policy open | §37 |
| C08 | Return: "no free normal teleport" + HOME aid proposal + player-placed markers all unresolved | §32 |
| C09 | Ending: "not locked", object undecided, but the sequence already has ruled-out failure modes | §48, §49 |
| C10 | 2–3 h playtime + "dense, not stretched" but no price/business decision anywhere | §51 |
| C11 | Condition system optional/low priority yet its stated purpose is "to justify Shave" (which is described as liked) | §29 |
| C12 | Extremely detailed exposure/pickup rules marked "remain to be validated" | §21 |
| C13 | Achievement guidance exists but no platform/feature plan (cloud, cards, etc.) | §28 |
| C14 | "Style selection completed" (Sunny r8) but "broader production presentation remains open" | §44 |
| C15 | C4 name selected, inclusion open; placement/controls "need their own design/approval" | §38 |
| C16 | Co-op: preserve save format for possible future co-op, don't build networking — untested against single-player balance | §37 |
| C17 | "No music" selected; audio section says every sound needs approval — music decision may deserve one more pass | §43 |

## 4. Tensions with the review evidence (T-list)

Severity: **H** = likely to generate the genre's most common negative reviews if unchanged; **M** = needs a
deliberate decision; **L** = note and move on.

| ID | Tension | Evidence | Sev. | Goes to |
|---|---|---|---|---|
| T01 | Rescue deletes ordinary carried loot + charges a fee | `[AGADH]` blackout ore loss ("want to do bad things to the creators"); `[MELT]` freeze-loss; `[OMT]` item deletion | **H** | Q26 |
| T02 | 2–3 h completion risks "paid demo" perception even at low price | `[AGADH]` 1–3 h at $5 still "paid demo"; `[OMT]` "just play the demo" | **H** | Q17 |
| T03 | No free teleport + climbing your own hole every trip | `[SPOT]` "will you let me dig or not?!"; `[MELT]` "hours of tedious back-and-forth" | **M** | Q27 |
| T04 | Guns "intended later" risk invalidating the shovel investment | `[MELT]` Tesla gun invalidated flamethrower; lesson: progress, never replace | **M** | Round 2 |
| T05 | Finite item population + per-save random placement + persistent saves needs a precise replay model | `[KD]` "no randomization, same playthrough"; `[SPOT]` no replay value | **M** | Q18 |
| T06 | Silent detector cues are good for comfort but must never be the only channel; deaf/colorblind players | Accessibility requirement in `PERFECT_DIGGING_GAME/14` | **M** | Round 5 |
| T07 | No music: some players praise silence (`[KD]` "the lack of BGM was wonderful"), others count no-music as a flaw (`[AGADH]` audio row) | Corpora disagree | **L** | Q22/Round 5 |
| T08 | One tuned balance vs. mode fit (cozy vs challenge audiences) | Mode mismatch is a repeated theme (`[AGADH]` `[OMT]` `[SPOT]`) | **M** | Q25 |
| T09 | Future-proofing for co-op without building it | `[KD]` broken co-op is worse than none | **L** | Q24 |
| T10 | Condition/grading system would add evaluation friction | `[OMT]` invisible systems disliked; no player asked for condition grades | **M** | Q30 |
| T11 | C4 must be powerful and forgiving, or it repeats the dynamite trap | `[KD]` "bombs do nothing"; `[AGADH]` dynamite clipping | **M** | Q30 |
| T12 | Sell and upgrade stations separated; surface friction risk | `[MELT]`/`[SPOT]` travel friction; doc itself warns "walk through building" loops | **L** | Q27/Round 4 |
| T13 | Fridge screenshots on every first find: charming but a storage/tech cost | Unique identity device; verify feasibility | **L** | Q18/Round 5 |

## 5. Salvage classification

### 5.1 KEEP — strong ideas to carry forward (pending your confirmation)

| # | Idea | Why it survives scrutiny |
|---|---|---|
| K01 | Detector-driven curiosity loop with silent, non-value cues | Directly fixes `[AGADH]`'s "little to discover" and `[MELT]`'s no-guidance issues without becoming treasure GPS |
| K02 | Single evolving tool, hold-to-dig from minute one, full rebinding | Matches the strongest anti-frustration lessons (`[AGADH]` RSI, `[OMT]` tool-swap fatigue) |
| K03 | Untouched start, no pre-dug holes, free-form excavation | The genre's core fantasy; differentiates from guided games |
| K04 | Sideways digging is genuinely valuable (clusters, no depth price multipliers) | Fixes `[KD]`'s straight-down trivialization without friction mechanics |
| K05 | Recognition reveal sequence (partial shape → identity → reaction) | The best "reward" idea in the document; no other reviewed game does it deliberately |
| K06 | No tedious final cleaning / no identification bureaucracy | Removes the exact friction `[MELT]` shovel and `[AGADH]` cleaning complaints imply |
| K07 | Abstract inventory + instant collect + physical Sell All comedy | Best of `[OMT]`'s QoL praise without inventory management |
| K08 | Money banked only on safe return | Creates the "I need to get this home" tension reviewers loved in `[SPOT]` without stamina |
| K09 | First-find fridge (name + depth only, player's own screenshot) | Personal memory artifact; better than `[MELT]`'s perk-less pedestals |
| K10 | Shared battery for digging + jetpack | One legible pressure system instead of three (`[SPOT]` stamina overload, `[AGADH]` battery + fall + inventory) |
| K11 | Excavation progress never resets; full terrain persistence | The #1 trust issue in the genre (`[AGADH]` hole not saved) |
| K12 | Continue Playing after the ending with all tools intact | Directly fixes `[AGADH]` disabled-tools finale and `[SPOT]` empty post-game |
| K13 | Slow-build mystery, normal systems at the finale | Fixes `[AGADH]` genre-shift and `[SPOT]` retcon endings |
| K14 | Rescue as emergency fallback that protects unique items | Good skeleton — needs loot policy decision (T01) |
| K15 | Placed, remote-detonated, genuinely powerful C4 (conditional) | Strongest version of explosives in the genre, if powerful |
| K16 | Large-find cable-yank extraction gag | Memorable physical comedy; keeps player in control |
| K17 | Finite item population per save | Makes the wall/fridge meaningful; no infinite loot treadmill |
| K18 | Prototype-first list (numbers not designed on paper) | Correct process; maps cleanly to our QA approach |
| K19 | Explicit NOT-list (no archaeology/crafting/survival/puzzle/management) | Strong scope discipline |
| K20 | Core test moment ("I should probably go back… fuck it, one more thing") | This is the review-proof definition of the loop |
| K21 | Garage-project tool escalation as a visual story | `[MELT]` proves visible upgrades sell progression |

### 5.2 CONFIRM / RESOLVE — needs an explicit decision

| # | Item | Question |
|---|---|---|
| R01 | Loot loss + fee on rescue | Q26 |
| R02 | 2–3 h + price | Q17 |
| R03 | Return aids / markers / teleport | Q27 |
| R04 | Replayability model + fridge persistence across saves | Q18 |
| R05 | Distinctive-find purpose, frequency, sell-vs-keep | Round 3 |
| R06 | Tool endpoint, guns, tier structure | Round 2 |
| R07 | Condition system | Q30 |
| R08 | Boundary language, materials, world size | Round 2 |
| R09 | Difficulty/modes | Q25 |
| R10 | C4 inclusion detail | Q30 / Round 3 |

### 5.3 DROP / CAUTION — recommend not carrying into the new concept

| # | Item | Reason |
|---|---|---|
| D01 | Item condition grading | Adds evaluation friction for near-zero player value (T10); drop unless a prototype proves otherwise |
| D02 | Any mandatory final cleaning pass | Forbidden by our anti-patterns; the document already agrees |
| D03 | Default loot deletion on failure | The genre's most reliably hated mechanic (T01); if kept at all, it must be opt-in "hard" mode |
| D04 | Separated surface stations requiring walks/menus | Keep sell + upgrade within seconds of each other (`[MELT]`/`[SPOT]` friction) |
| D05 | Audio-only cues | Accessibility violation; all cues need a visual channel |
| D06 | Multi-currency, blueprints, RNG gates | The document already forbids these; keep it that way |
| D07 | Hedging language in shipping specs ("proposed", "comparison baseline") | Decisions in this process must end as explicit `CONFIRMED`/`REJECTED` entries |

## 6. What the legacy document never answers (gaps → question rounds)

| Gap | Round |
|---|---|
| Business: price, platform, release model, demo, updates, localization | Round 1 (`01_QUESTIONS_VISION.md`, Q17–Q24) |
| Audience, age rating, session length, mode structure | Round 1 (Q14–Q16, Q25) |
| World: size, boundaries, materials, terrain tech, save model detail | Round 2 (world & terrain) |
| Tools: tiers, gun decision, upgrade tracks, numbers philosophy | Round 2 (systems & progression) |
| Discoveries: roster, frequencies, purpose/retention, detector rules detail | Round 3 (content & discovery) |
| UX/accessibility beyond comfort basics; menus; HUD; tutorial wording | Round 4 (interface & body) |
| Production: engine, art pipeline, audio pipeline, localization, QA, achievements | Round 5 (production & polish) |
| Ending object and mystery beats | Round 3 / after prototype (per doc) |

## 7. Audit conclusion

The legacy document contains a **genuinely good game** with a stronger identity than most of the
comparative set: a dense, 2–3 h curiosity loop with recognition-based rewards, no management bloat,
and honest "continue after credits" endgame goals. Its risks are concentrated in four decisions —
**loot loss on rescue, runtime/price, return friction, and the eventual gun/tool endpoint** — plus a
large amount of unverified "already implemented" status that this process should treat as fiction
until you confirm it.

Nothing above is approved. Every L-item is queued for your verdict in `02_DECISIONS.md`.
