# 06 — Upgrades and Economy

> Two catastrophic economy patterns dominate the review corpora:
> **(1) everything is maxed halfway** (`[AGADH]` "max out before the hole is 15% of the way down",
> `[MELT]` "ended the game with 100k and nowhere to spend it"), and
> **(2) upgrades that don't register** (`[OMT]` "invisible effects +5% range", `[KD]` dynamite that
> does nothing, `[MELT]`'s Tesla gun invalidating all prior investment).
> This economy is engineered against both.

## 1. Upgrade architecture

Five parallel tracks; every track has a purpose in every layer:

| Track | Tiers | Effect scale | Acquired |
|---|---|---|---|
| **Dig power** (shovel/drill) | 6 | +25–40% speed/radius each | Coin + layer materials |
| **Capacity** (backpack/storage) | 6 | +20–35% weight each | Coin |
| **Traversal** (anchor/jet suit) | 4 each | Distances, speed, safety | Coin + modules |
| **Auxiliary** (collector, scanner, lamp, charges, terraformer, suit) | 4–5 each | Utility unlocks | Coin + contracts + POIs |
| **Deep modules** | 12 types | Behavior changes | POIs/contracts/museum — **never RNG-only** |

Plus non-power sinks that scale to the end:

- **Museum restoration** (per wing; each wing gives a perk),
- **Hub upgrades** (workshop machines, greenhouse, skyline, dock),
- **Cosmetics** (tool skins, outfits, hub decor),
- **Permits** (optional deep zones, challenge dens),
- **Consumable stockpiles** (speed up future runs),
- **Gifting** (NPC quests).

## 2. The "no dead zone" law

> At any point between minute 5 and the credits, the player must have **at least 3 available
> purchases**, and the cheapest one must cost **≤ 40 minutes of their current earning rate**.

Implementation:

- Upgrade costs are computed from a **global curve** (below) but availability is gated by layer
  progression, not by "all upgrades bought".
- The shop shows locked tiers with visible requirements ("Auger IV — unlock at Layer 5") so there is
  always a next goal.
- Late-game coin has infinite sinks (cosmetics, museum, contracts, permits, gifting, prestige
  flourishes). Money is never useless `[AGADH]` `[MELT]` `[OMT]`.

## 3. Pricing curve (first-pass formula)

For track `t`, tier `n`:

```
cost(t,n) = base_t × growth_t^(n-1) × layer_multiplier(depth at unlock)
```

Starting constants (to be tuned in playtest):

| Track | base | growth | Target purchase cadence |
|---|---|---|---|
| Dig power | 60 | 2.6 | every 45–90 min |
| Capacity | 40 | 2.4 | every 40–70 min |
| Traversal | 90 | 2.8 | every 60–90 min |
| Auxiliary | 50 | 2.3 | every 30–60 min |
| Modules | fixed POI tokens | — | 1 per 45 min |

Earning rate scales ~12× from Layer 1 to Layer 7 via ore values, while total costs scale ~20×, so the
player is always "almost there" but never soft-locked `[SPOT]` "need to buy the expensive tier
upgrade twice over to finish" is explicitly prevented by a **finale readiness check**: the game
shows the completion requirements long before the end, and the critical-path finale never requires
optional side grinding.

## 4. Respect and respec

- **Free, instant respec** of all upgrade tracks at the workshop (modules included).
- **No irreversible choices.** `[SPOT]` permanent turret branch that forced a full restart ("I HATE
  THAT IN ORDER TO TRY NEW TURRET I HAVE TO START COMPLETELY OVER") is a named anti-pattern.
- **No respec penalty, no currency loss.** Experimentation is encouraged; the game explicitly
  advertises build flexibility.
- If a patch rebalances an upgrade, affected saves receive an automatic, free stat reconciliation
  plus a respec token (see `20_LIVE_UPDATES_AND_DEV_PROCESS.md`).

## 5. New Game+ and post-game economy

`[AGADH]` locked achievements behind NG+ and wiped the yard; `[KD]` did NG+ right (keep gear,
terrain resets, new skins); `[SPOT]` had no NG+ at all. Our rule:

| NG+ element | Design |
|---|---|
| Gear | 100% carried over (tools, modules, cosmetics) |
| Terrain | Regenerates with a new world seed |
| Layers | Kept unlocked; additional "ascended" variant content in each layer |
| Upgrades | Tracks carry; a *prestige* flourish tier (cosmetic + small utility) unlocks |
| Achievements | All achievable in the first playthrough; NG+ adds none |
| Difficulty | Player-selectable per NG+ cycle, independent of mode |
| Economy | Sinks scale; ore values gain a small NG+ multiplier |
| Speedrun support | In-game timer, split display optional, ghost replay of your best run |

## 6. Contracts and bounties (lategame structure)

To keep the loop purposeful after credits `[SPOT]`'s biggest endgame gap:

- **Contract board:** 3 active slots; generated from a fixed template bank (no infinite RNG spam).
  Examples: "Deliver 60 ruby in 20 min", "Map 3 unchecked dead ends", "Excavate a 12×12 room to
  100%", "Find the fossil in Layer 4's east caves".
- Rewards: coin, modules, cosmetics, museum tokens, permits.
- **Daily seeded dig**: fixed seed, global leaderboard optional, no rewards gated behind it.
- **Excavation contracts** ("clear all dirt" style) are **never** required for achievements and are
  bounded in size so they feel like satisfying side jobs, not 20-hour grinds `[SPOT]`'s "clear all
  dirt" achievement hate.

## 7. Economy telemetry (what to instrument)

- Time between purchases (target median 30–45 min, p90 ≤ 70 min).
- % of players with 0 affordable purchases at any session end (target < 2%).
- Coin held at credits (target: enough for ~2 remaining sinks, not 100k+ like `[MELT]`).
- Upgrade "felt" survey prompt once per tier: "Did you notice the change?" (target > 95% yes).
- Fraction of players who ever respec (want > 15%; proves safety).

## 8. Numbers sanity table (mid-game example, Layer 4)

| Item | Cost | Player income/hour at Layer 4 | Hours to afford |
|---|---|---|---|
| Dig tier 4 | 4,500 | ~1,200 | ~3.8 total-run hours (not consecutive) |
| Capacity tier 4 | 3,000 | ~1,200 | ~2.5 |
| Jet suit 2 | 5,200 | ~1,200 | ~4.3 |
| Lamp 3 | 1,600 | ~1,200 | ~1.3 |
| Module | POI token | — | Discovered |

Every number in this table is validated by the "cheapest purchase ≤ 40 min" law against the actual
earning curve before content lock.
