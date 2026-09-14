# 05 — Discoveries

## 1. Find categories and tiers

| Tier | Count target | Detector | Destination | Money |
|---|---|---|---|---|
| **Common** | 20–30 types | Always silent | Sell only | Reliable income, worthwhile at any depth |
| **Distinctive** | 30–50 types | Noteworthy ones signal; some stay silent by design | **Purpose TBD (D03)** — either first copy to display with duplicates sold, or sell with a snapshot; user is researching | Good money |
| **Unique** | Small set (a few) | Signals | Kept on the display forever; unsellable; grants a passive benefit | No sale |
| **Rare passives** | TBD (S10, find-or-buy recommended) | Signals | Grants a permanent effect | No sale |

Commons include the mineral ladder (coal → copper → iron → silver → gold → emerald → ruby → diamond),
bottles, plain stones, commonplace scrap, packaging and rubbish. "Common" means routine to find
repeatedly, not merely familiar.

## 2. The detector

The detector is passive equipment: the player never equips it. They simply dig (L31).

- **Silent and visual.** No audio pings (F07; exact presentation TBD). The tool reacts; a subtle
  screen-edge hint may show direction and proximity. The reference game's edge indicator is a
  researched option.
- **Never reveals value or rarity.** A huge object may read "stronger" because of size, but the
  detector never says what it is. No "special cue" that makes ordinary finds feel like waste.
- **One foreground target at a time**, stable switching, quiet intervals between cues. Constant
  beeping-like interruption is forbidden.
- **Eligibility is authored per object**, never decided by price, size or metal content. Some
  distinctive finds deliberately do not signal, so that digging itself keeps rewarding the player
  outside signal-chasing.
- Signals can always be ignored; not following one costs nothing but an undiscovered object.

## 3. The reveal and recognition loop

1. The player digs normally; the object appears partially.
2. **Interesting objects do not disappear when touched.** They stay physically present; the player
   excavates around them and watches the silhouette resolve.
3. Once enough is exposed, the object becomes interactable and can be collected.
4. **Recognition is the reward:** curved metal → handle → rectangular body → "…oh, it's a washing
   machine."
5. No archaeology: no brushing minigame, no 100% cleaning requirement, no identification timers, no
   mailing objects for appraisal (L33). The game decides when enough is revealed; the player
   decides what is worth revealing.

Small/common finds are quick: a bite or two, instant pickup, clear feedback so nothing is collected
unseen.

## 4. First-slice objects (built before bulk production)

| Object | Tests |
|---|---|
| Washing machine | Large appliance: box + circular door readability |
| Hand drill | Small handheld silhouette recognition |
| Gearbox / engine block | Machine parts; natural lead-in to a cluster |
| Mammoth bone / tusk | Organic curves; ties to the Danube bones inspiration |
| Gramophone | Funny, display-worthy oddity with a distinctive horn |

These five are prototyped and reviewed before any large content batch (D07).

## 5. Related-object clusters

Five authored micro-scene templates to start, rotated and placed procedurally with slight jitter
(D06):

1. **Bone scatter** — skull fragment, ribs, tusk piece spread over a few meters.
2. **Vehicle parts** — wheel, axle, bumper, engine block, arranged as if a car sank here.
3. **Household cluster** — plates, bottles, stove, sewing machine in a collapsed heap.
4. **Machine fragments** — gears, drive shaft, boiler plate leading toward something larger.
5. **Odd arrangement** — deliberately placed objects (a circle of bottles around a tool), feeding
   the mystery.

Rules: authored relationships, no pre-dug chambers, counted once in the finite population, validated
for spacing. A cluster is a suggestion, never a quest marker.

## 6. Large discoveries

A few per run (target 3–5): a car, a large appliance pile, a machinery section (D10). The player
excavates most of it first; extraction is a physical event — a cable descends, attaches, and the
object is yanked out with physics comedy. No cinematic camera; the player stays in control. Some
very large discoveries may remain in place permanently as landmarks.

## 7. Value and rarity

Four bands (D05):

1. **Common** — reliable income, always worth collecting, never trivialized by depth.
2. **Distinctive** — good money; the "that haul paid for the drill" tier.
3. **Rare** — several expeditions' worth, never enough to buy half the upgrade tree at once.
4. **Unique** — grants an effect instead of money.

No jackpots that finish the economy; no trash that feels like a waste of a slot.

## 8. Display integration

- The surface display is a growing shelf/wall/column with **predefined outlines** (D11).
- **Empty frames are visible from the start; the shape inside stays hidden until discovery**
  (D11b). This gives collection goals without spoiling silhouettes.
- The player never chooses placement: when a unique (or first-find distinctive, if D03 resolves
  that way) is collected, they carry it to its waiting outline and place it.
- The display records name + depth found. No prices, no condition, no rarity labels.

## 9. Inventory behavior for finds

- The bag is abstract; there is no physical carrying of buckets or crates (L41).
- **Hard stop when full:** the player cannot pick up; the find stays exactly where it is in the
  world, and can be retrieved on a later trip (S05b).
- **Nothing is ever deleted.** No overflow teleport, no inventory destruction, no drop-on-death.
- Uniques and ending components never consume capacity and are never lost (L38).

## 10. References and humor

Original parody only (D13): objects may evoke an era or a region without naming real brands, games
or people. The humor comes from what the object is and how the economy treats it — deadpan, not
loud (Q09). No body-sound jokes.

## 11. Mystery objects

The three-step escalation (D08) is delivered entirely through finds:

1. **Anachronistic junk** — a soda can too deep, a rubber duck in an ancient layer.
2. **Too correct** — a rustless tool, a bottle standing upright under tons of sediment, a part
   matching no nearby machine.
3. **Constructed impossibilities** — machinery built from ancient materials with a modern function.

The trail ends at the final object: **a modern object built in impossibly ancient materials**
(Q12). See `11_ENDING_AND_MYSTERY.md`.
