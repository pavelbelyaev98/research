# 20 — Live Updates and Dev Process

> The update record in the comparative set is a masterclass in how goodwill is won and lost:
> **Won** — `[KD]` free 2.0 update ("they could have made a 10 dollar game then just abandoned it,
> but instead they ADDED on a 2.0"), `[MELT]` near-daily patches, `[SPOT]` free content updates and
> fast patches. **Lost** — `[KD]` 2.0 "patched in stress", moved tools behind RNG, invalidated the
> dumb-fun pacing; `[MELT]` August heat rebalance made the cozy game stressful ("devs rebalanced
> something, now I lose too much heat"); `[SPOT]` 1.1 invalidated saves and forced restarts;
> `[AGADH]` no updates at all after launch ("over a year and still nothing has come").

## 1. The prime directive

> **Never make an existing player's experience worse without their consent.**

Every change is classified before it ships:

| Class | Examples | Rules |
|---|---|---|
| **Fix** | crash, softlock, save bug, UI trap | Ship as fast as possible; announcement; never breaks saves |
| **Content** | new landmark family, contracts, cosmetics, QoL | Free; optional install; old saves remain valid and 100%-able; no power creep |
| **Balance** | economy numbers, heat/battery tuning, drop rates | Only if it makes the game easier or adds options; if it can make things harder, it ships **opt-in** (difficulty option, toggle) or to a **beta branch** first; never applied retroactively to break a build |
| **Rework** | systems changes | Requires a player-facing choice: "play classic or updated?" Legacy branches stay available |

`[KD]`'s 2.0 split and `[MELT]`'s heat nerf are exactly what the balance rule prevents: the 1.0
experience is a promise, and it remains playable.

## 2. Patch discipline

1. **No save-breaking patches, ever.** Schema migrations are tested N-3 → N and never wipe.
2. **Settings preserved** through every update `[KD]` settings reset complaint.
3. **Patch notes in plain language:** one-line summary first ("Your tools now..." / "Fixed the
   freeze when..."), then technical details; in-game changelog in the hub radio.
4. **Betas:** an opt-in beta branch for balance and experimental content; players can revert to
   stable with one click (Steam betas). Feedback survey built into the opt-in.
5. **Hotfix SLA:** crash/save/blocker fixes within 48 h of a confirmed report; a hotfix rollback
   path exists.
6. **Content updates target every 6–10 weeks** for the first year: alternating QoL/community wish
   and new content; each update includes at least one direct response to top community requests.
7. **No stealth changes.** Every gameplay-affecting change is in the notes with a "why" line.

## 3. Rebalancing with consent (the `[MELT]` rule)

If a balance change would make existing saves feel harder:

- Ship it **behind a new preset or toggle** ("Classic Comfort" vs "New Balance"), default Classic
  for existing saves, New for new saves.
- Give affected players a **free respec + compensation** (currency or cosmetic) on first launch
  after the patch.
- Explain the change in-game (hub radio patch note) and in the Steam announcement.
- Run it on the beta branch for ≥ 2 weeks with telemetry before promoting it.

## 4. Community process

| Channel | Purpose | Cadence |
|---|---|---|
| Steam announcements | Patch notes, roadmaps | Every update |
| Bug tracker (public board) | Reports → status (open/in-progress/fixed) | Reviewed weekly |
| Feature voting board | Player wishlist with dev triage | Quarterly |
| Dev log | Design reasoning, "why we changed X" | Monthly |
| Discord | Chat, events, screenshot contests | Daily (community mods) |
| Curator/review outreach | Answer critical reviews, fix real issues | Ongoing |

Commitments:

- **Reply publicly to the top 20 critical reviews** with concrete answers or fixes; `[KD]`'s review
  section descended into astroturf accusations while `[AGADH]`'s silence bred resentment.
- **No arguments, no defensiveness:** acknowledge, fix or explain, move on.
- **Community wishlist transparency:** mark each popular request as Planned / Exploring /
  Won't do (with a reason). No silent ignoring.

## 5. Roadmap: first 12 months (illustrative)

| Window | Theme | Contents |
|---|---|---|
| Launch | Complete 1.0 | All modes, post-game, NG+, museum, 45 achievements |
| +6 weeks | Stability & QoL | Save integrity pass, map improvements, top-10 requests |
| +3 months | Landmark Update | New landmark family + contracts + 10 cosmetics (free) |
| +4 months | Co-op beta | 2–4 player parity build on opt-in beta `[16]` |
| +6 months | Co-op release | Full parity, party saves, shared achievements |
| +8 months | Depths Update | New Layer 7 variant "Ascended", horror den expanded (opt-in) |
| +12 months | Anniversary | Endless seed events, stats retrospective, community showcase |

No paid DLC for base content; supporter packs only.

## 6. Telemetry and listening

- Watch the same themes players wrote thousands of reviews about: length, performance, save
  integrity, map clarity, mode fit, price perception.
- After each update, run a **sentiment diff** on new reviews (keyword themes from the analyses):
  target no negative growth in "performance", "saves", "too short", "lost progress".
- A public **"state of the game"** post twice a year: what shipped, what's next, what was learned.

## 7. Anti-patterns (named, from evidence)

- Abandonment after launch `[AGADH]` "over a year and still nothing".
- Stealth nerfs that invalidate cozy builds `[MELT]`.
- Free updates that erase the original experience instead of adding an option `[KD]` 2.0.
- Updates that invalidate saves and force restarts `[SPOT]` 1.1.
- Settings that don't persist; patches that reset options `[KD]` `[SPOT]`.
- Ignoring a public issue tracker while reviews pile up.
