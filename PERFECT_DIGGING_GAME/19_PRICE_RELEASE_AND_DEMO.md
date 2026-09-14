# 19 — Price, Release and Demo

> The comparative set shows price-versus-content is judged brutally:
> $5 for 1–3 h still produced "paid demo" reviews `[AGADH]`; ~$5–7 for 3–8 h was usually accepted
> (`[KD]` "each got our $5 worth", `[MELT]` "I feel like I robbed them") but attracted "wait for
> sale" advice; $12.99 for 5–12 h drew "Early Access vibes at full price" `[SPOT]`.
> The lesson: **price is a promise about scope.** Make the promise conservative and exceed it.

## 1. Pricing

| Decision | Value |
|---|---|
| Launch price | **$9.99 / 9,99 €** base (regional pricing via Steam's recommended matrix) |
| Content promise | 10–14 h critical path; 20–25 h for 100%; 30+ h with post-game modes (all at launch) |
| Sales | Standard Steam cadence from month 2; no launch-week discount gimmicks; first sale ≥ 6 weeks after launch to protect day-one buyers |
| Deluxe/supporter bundle | Optional cosmetic + soundtrack bundle, clearly optional, never containing gameplay power |
| Refund respect | The first 2 h are a complete, satisfying taste of the real loop and progression — not a funnel. We never design around the refund window; we design so nobody wants to refund |

Rationale: $9.99 with 10+ hours and full post-game positions us between the under-delivering $5
tier and the over-promising $13 tier, and undercuts accusations of "paid demo" with a
content-to-price ratio comparable to the best-reviewed examples.

## 2. Early Access policy

**Default: no Early Access.** Release when the game is complete, like the best-received titles in
the set ("I appreciate the devs not putting the game in Early Access for several years" `[SPOT]`).

If EA is ever chosen (business decision only, e.g. funding):

- Store page and trailer state exactly what exists vs. what is planned, with a dated roadmap.
- Price during EA is **lower** and rises at 1.0 with a thank-you perk for EA buyers.
- No paywalled content; saves always migrate forward; no wipe on 1.0.
- "Should have been Early Access" can never be said about a 1.0 launch because 1.0 only happens
  when the checklist in `23_SCOPE_ROADMAP_AND_QA.md` passes.

## 3. Demo policy

Demos were a bright spot (positive demo experiences in the corpora, and "the game is barely longer
than the demo" as the failure mode) `[OMT]`. Our demo:

| Aspect | Rule |
|---|---|
| Size | 30–45 minutes: Layer 1 + one landmark + the first upgrade tier |
| **Save transfer** | Demo progress carries into the full game, automatically (same save format) |
| Content | A true slice, not a curated trailer level; shows real pacing and the real map |
| Restrictions | Limited only by depth/items, never by fake timers or "buy full version" walls mid-flow |
| Honesty | Demo includes the same settings/accessibility screens as the full game |
| Availability | Permanent free demo; included in Next Fest |
| Safety | Demo cannot exceed ~35% of the critical path, so "just play the demo" is never the right advice `[OMT]` |

## 4. DLC and monetization policy

| Allowed | Forbidden |
|---|---|
| Free content updates (layers' variants, contracts, landmark families) | Paying for power, currency or upgrades |
| Cosmetic/supporter DLC clearly labelled | Paid RNG/loot boxes |
| Soundtrack + art book bundles | Paid post-game modes that feel cut from 1.0 |
| Full expansion **only after** 1.0 is content-complete and roadmap delivered | DLC before the base game's promised scope is met `[MELT]` "DLC before the base felt finished" |

All gameplay content updates are **save-compatible and free**.

## 5. Store presence and communications

- **Tags and description:** include "Cozy", "Relaxing", "Exploration", "Base Building", "Mining",
  "Single-player", "Co-op (upcoming)" — and **state optional horror plainly**: "Optional horror
  elements can be enabled in settings; off by default."
- **Screenshots/GIFs:** actual gameplay from representative early/mid/late areas; no overpromising
  cinematics.
- **Trailer:** 60–90 s; shows digging escalation, a landmark, the hub, upgrades, an ending tease
  without spoilers; ends with the content promise ("10–14 hours, complete story, endless mode").
- **Content warnings** on store page for optional horror and flashing (reduced by default).
- **Accessibility tags** filled out accurately (see `14`).
- **No fake influencers or bought reviews.** `[KD]`'s "rating is bought" accusations are a
  cautionary tale; the review section is fed by the demo and real content only.
- **Press/creator keys:** generous, with an embargo that lets reviewers finish the game (avoid
  "reviewed in 2 hours" distortion).

## 6. Launch readiness gates

- [ ] All content complete and polished (no "will patch later" core features).
- [ ] 20+ hour playtest full run completed by all QA testers with zero save loss.
- [ ] Deck Verified, controller-only run verified, accessibility statement published.
- [ ] Localization complete for EFIGS + RU/PL/PT-BR/zh-Hans/ja/ko/tr (or explicitly scoped).
- [ ] Store page, demo, trailer, tags, horror disclosure, and price live and accurate.
- [ ] Day-one patch is a bonus, not a necessity: no launch blocker fixes pending.
