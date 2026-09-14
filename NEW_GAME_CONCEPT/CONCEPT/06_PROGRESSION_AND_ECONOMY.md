# 06 — Progression and Economy

## 1. The shape of progression

- **One currency: money.** No second currency, no crafting, no blueprints, no license tiers, no RNG
 gates.
- **Money is banked only when sold at the surface**. This makes every trip a risk decision
 without ever deleting anything on failure.
- **Strictly sequential purchases:** you always buy the next level of a track; a lucky find cannot
 skip levels (I06).
- **Fully transparent shop:** current → next effect, cost, and practical benefit always shown;
 locked items visible with their requirement (S11).
- **The final meaningful purchase lands near the end** of the run so its power is used
 (target ~75–85% of first completion; prototype-tuned).

## 2. Upgrade tracks (six)

| Track | What it improves | Milestone-level changes (every ~3rd level) |
|---|---|---|
| **Tool** | Power, bite size, adaptation quality | New head/attachment, dramatically faster digging, access to previously tough ground |
| **Battery** | Capacity and efficiency of the shared dig+jetpack battery | Longer expeditions; efficiency that makes old trips trivial |
| **Jetpack** | Speed, efficiency, altitude, assists | Sustained ascent, steering assists, hover hold |
| **Inventory** | Bag capacity | Strong steps; a full trip becomes a real haul |
| **Detector** | Range, cue clarity, broad direction | Confident long-range hunches |
| **C4** | Blast size, pack size, efficiency | Room-clearing blasts; cheaper demolition |

Per-track level count is flexible (~6 by current design), but the structure stays: many small
increments with a capability punctuation every roughly third level (S02). The 30–45 minute cadence
target measures these milestone (capability) purchases, not every level. Every purchase must be
visible or audible on the tool or the HUD — no "invisible +5%" upgrades.

## 3. Money in

- Commons and distinctives sell for money; value bands: common income, distinctive value, rare =
 several expeditions, unique = effect instead of money (D05).
- Common finds stay worthwhile at every depth; the deep game does not turn early income into
 garbage.
- Rare finds excite without breaking the curve; a rare find should afford one big upgrade, not half
 the tree.
- Cluster hauls, large-find extraction and display completions provide occasional big paydays.

## 4. Money out (including late game)

Primary: the six tracks.

Late-game sinks keep money meaningful after the tracks are maxed (S03b):

- extra C4 charges and consumables;
- lamps (buy individually; useful for lighting and photography);
- display upgrades (more frames/of the display growing, decorative pedestals);
- cosmetic tool skins and yard items;
- small conveniences (fuel top-ups, spare charges).

There is no point where the intended player has literally nothing to buy while still digging.

## 5. Fuel (shared battery)

- One battery powers **digging and jetpack**.
- Drain occurs only during powered actions; reading, standing, thinking and inspecting never drain.
- Refills are **purchased at the surface**: full or partial, amount and price shown before purchase;
 bigger tanks keep current fuel rather than granting a refill (S04).
- **Return-power warning:** an adaptive indicator with safe / risky / critical states — never exact
 required-energy math. It accounts for depth and the route, not just a percentage threshold (S04).
- At zero fuel anywhere: automatic recovery to the surface with full fuel, **all finds kept**, a
 depth-scaled fee, and any shortfall as interest-free debt automatically deducted from future sales
 (Q26f). No manual rescue option; no confirmation prompt.
- Recovery never blocks progress, never deletes items, and never permanently ruins a save.

## 6. Capacity (the bag)

- **Generous starting capacity**: the first expedition must already feel good; upgrades improve a
 loop that works, they do not repair a miserable one.
- Capacity grows in strong steps; the HUD shows count/capacity continuously (I01).
- **Hard stop when full:** you cannot pick up; the find stays in the world exactly where it is and
 can be retrieved later (S05b).
- **Nothing is ever deleted**: no overflow deletion, no inventory destruction, no loot loss on
 failure of any kind.
- Uniques and ending components never consume capacity.

## 7. Selling

- Selling happens only at the surface Sell All machine; the inventory screen never sells.
- **One-button Sell All** (I05) with a physical, comedic machine animation and clear money feedback.
- Individual selling available at the machine for players who want it.
- Money is banked instantly on sale; there is no bank/branch/ATM system.

## 8. What the economy never does

- No RNG-gated progression (no blueprints replacing shops).
- No condition/grading system (Q30c).
- No expiring coupons or time-limited offers.
- No multi-currency.
- No dead end where everything is purchased halfway through the run.
- No loot deletion as a failure consequence.
- No item durability; tools never break.
- No payed power, no premium currency, no microtransactions.

## 9. Tuning targets (validated in prototype; exact values per Rule 8)

| Metric | Target |
|---|---|
| First purchase | within the first minutes |
| Median time between milestone (capability) purchases | 30–45 min; small level purchases land more often |
| Purchases affordable at any moment | ≥ 3 |
| Maxed tracks before credits | 50–85% of players (i.e., some left for Continue Playing) |
| Rare find value | ≈ one big upgrade, never several |
| Recovery fee | noticeable, never progress-blocking |
| Resources left at credits | enough for a few remaining sinks, never an absurd pile |
