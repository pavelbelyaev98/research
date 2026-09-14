# 05 — Items and Resources

> Rule: **nothing you carry is ever destroyed by arbitrary systems.** Capacity pressure may slow you
> or end a trip; it never vaporizes loot. `[AGADH]` battery-blackout destroyed the whole inventory,
> `[OMT]`'s third rare item deletes the first, `[MELT]` freezing dropped carried ice — all forbidden.

## 1. Resource taxonomy

| Class | Examples | Purpose | Sells? |
|---|---|---|---|
| **Common ore** | Dirt, stone, coal | First money, crafting filler | Yes |
| **Metal ore** | Iron, copper, silver, gold | Upgrade currency, tool tiers | Yes |
| **Gem ore** | Amber, amethyst, emerald, sapphire, ruby, diamond | High value, museum pieces | Yes, but museum copies keep perks |
| **Exotic ore** | Uranium, adamant, prism, corestone | Late gates, final upgrades | Yes (deep) |
| **Junk / salvage** | Bottles, scrap, toys, electronics | Sell + collectible flavor | Yes |
| **Fossils** | Bone shards, ammonites, giant skulls | Museum, lore, optional summons | No (museum only) |
| **Artifacts** | Precursor tools, tablets, machine parts | Museum: lore + small passive perk | No |
| **Lore items** | Notes, tapes, photos, journals | Archive UI, story | No |
| **Key items** | Glyphs, seals, valves, sigils, keys | Gates, quests | No |
| **Consumables** | Batteries, charges, light sticks, rations, repair kits | Utility | Can be sold |
| **Placeables** | Lamps, ladders, platforms, signs, storage crates, beacons | Base-building, routing | Reclaimable |
| **Cosmetics** | Tool skins, hub decorations, outfits | Self-expression | No (duplicates convert to currency) |

### Ore value table (starting values; tune per economy)

| Layer | Ore | Base value | Notes |
|---|---|---|---|
| 1 | Dirt/stone/coal | 1 / 2 / 5 | Starter income |
| 2 | Iron / copper | 12 / 18 | Tool tier 3–4 |
| 3 | Silver / amber | 35 / 45 | Gem intro |
| 4 | Gold / amethyst | 70 / 90 | Economy spike, sinks open |
| 5 | Emerald / sapphire / ruby | 130 / 160 / 220 | Ring/geode formations |
| 6 | Diamond / uranium | 300 / 380 | Heat/hazard layer |
| 7 | Adamant / prism / corestone | 500 / 700 / 1,000 | Final upgrades + museum |

Ore spawns in **recognizable formations** (veins, geodes, clusters) with audio/visual tell, so
scanning and vein-reading are real skills `[AGADH]` "detector" praised; `[SPOT]` "dig every speck"
satisfaction.

## 2. Inventory rules

- **Weight-based, generous, transparent.** Base capacity comfortably holds 20–30 minutes of
  thorough digging; upgrades double it across the game.
- **Overflow goes to storage, not the void.** When full, the next collectible is auto-sent by
  "delivery drone" to hub storage (a visible, charming animation). No loss, no penalty.
- **Rare/temporary items have a dedicated overflow-safe pouch**, minimum 8 slots. `[OMT]`'s
  2-slot rare inventory that deleted items is a named anti-pattern.
- **No item rot, no timers, no coupon expiry.** `[OMT]` discount coupons that expired before use
  are banned; discounts are permanent unlocks instead.
- **Quick-deposit, sort, search** in all storage UIs from day one; storage is unlimited at the hub.
- **Weight pressure is a soft trip-ender**: slow walk at 100–120%, no movement penalty under 100%.
  Never drop items automatically; never block picking up.

## 3. Consumables

| Item | Use | Balance rule |
|---|---|---|
| Battery cell | Recharges suit/flashlight/drill charge | Cheap, stackable; Cozy mode unlimited |
| Blast charge | Digging / ore-safe modes | Upgradeable; must outperform shovel per second `[KD]` "bombs do nothing" |
| Light stick | Placeable temporary light | Stacks, cheap, color-coded |
| Ration | Heals in Standard/Challenge | **Buyable and craftable** — no RNG sandwich spawns `[OMT]` "AFK 5 minutes for health" |
| Repair kit | Fixes placeables/vehicle only | Tools never break, so no tool repair |
| Oxygen/insulation doses | Extend layer access | Optional assist in Cozy |

## 4. Placeables and base-building (light)

Digging games that let players *shape* terrain (dirt-spitting, staircases, lamp networks) generate
some of the warmest reviews `[OMT]`. But full building overwhelms the loop, so scope it:

- 12 placeable types at 1.0 (lamps, ladders, platforms, stairs, fences, signs, crates, beacons,
  rails, pipes, planters, trophies).
- **Ghost preview + snap**; reclaim for full refund; no placement limits underground.
- **Surface base:** decorate the yard/hub with earned trophies and museum rewards.
- Terraformer tool can stamp saved blueprint patterns ("10-step spiral stair").
- No structural physics, no collapse, no upkeep.

## 5. Collectibles and museum

Museum/pedestals exist in `[MELT]` and were loved *in concept* and hated *in execution* — artifacts
"just placed on stands and give no perks" `[MELT]`. The fix:

| Collectible | Count | Reward per completed set |
|---|---|---|
| Fossils | 40 | Lore entries + museum display + one of: backpack, scan, or lamp upgrade token |
| Artifacts | 24 sets pieces | Passive perks: +5% ore value per set, faster rescue, discount |
| Lore notes/tapes | 90 | Story arc completion, hub NPC dialogues, a secret ending scene |
| Rainbow/prismatic ores | 7 | Cosmetic tool skins + a trophy room |
| Junk rarities | 100+ | Flavor descriptions, "curio shelf" fills, small currency trickle |

Rules:

- **Every collectible gives something mechanical or narrative.** No dead trophies `[MELT]`.
- **No missables:** deterministic placement, respawn-safe, map-marked after scan.
- **No RNG-gated completion.** `[SPOT]` buggy collectathon achievements are banned by placement
  determinism.
- Set completion should reward exploration, never require grinding a drop table.

## 6. Currencies and sinks

One primary currency (coin) + one late-game token (core shards from Layer 6+). No premium currency,
no gems-for-cash.

Coin sinks (see `06_UPGRADES_AND_ECONOMY.md` for numbers): tool tiers, utility tiers, modules,
capacity, consumables restock, museum restoration, hub cosmetics, contracts, permits for optional
deep zones, speedrun/challenge entry fees (small), gifting hub NPCs.

## 7. Item acquisition sources

| Source | Guarantees |
|---|---|
| Digging | Bulk income; depth = value scale |
| Landmarks | Modules, key items, artifacts, story items, unique cosmetics |
| Contracts | Targeted rewards (e.g. "100 iron → lamp module") |
| Museum milestones | Mechanical perks and cosmetics |
| Hub NPC quests | Discounts, tool skins, flavor |
| Endless mode | Seeded procedural ore + all collectible families |

No source is mandatory; each source has a parallel path to the same capability (e.g. modules can be
bought with coin *or* found). This keeps builds from dead-ending `[SPOT]` "wrong build can dead-end
a save".

## 8. Anti-patterns (named)

- Loot destroyed on blackout/freeze/fall `[AGADH]` `[MELT]` — **never**.
- Rare-item slots that delete previous rare items `[OMT]` — **never**.
- Expiring coupons `[OMT]` — **never**.
- Random lamp colors requiring reroll installs `[OMT]` — lamps are freely color-selectable.
- Paid RNG loot or slot machines as core progression `[OMT]` slot machine is a decorative minigame
  with **negative expected value removed** (purely for fun, cosmetic prizes only).
