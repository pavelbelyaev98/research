# 03 — Discussion: Rescue, Falls/Health, Tool Evolution

Three items you asked to keep discussing. Each section: review evidence → design problem → options →
recommendation. Answer the follow-ups (Q26f/Q28f/Q30f) to close them in the register.

---

## 1. Rescue without loot loss and without abuse (Q26)

### 1.1 What the reviews actually say

| Game | Failure rule | Reception |
|---|---|---|
| `[AGADH]` | Battery at 0 explodes; back to surface, **entire inventory lost** | Top-tier anger: "The whole 'You ran out of energy and lost all your ores' mechanic makes me want to do bad things to the creators" |
| `[MELT]` | Freezing sends a rescue robot that **takes carried resources** | Mixed: "I liked that you don't die, you freeze instead" survives as praise, but resource loss generated negatives; the August heat patch made it worse and sentiment dropped |
| `[OMT]` | No autosave/health economy; deaths and lost progress | "AFK for 5 minutes to let my health slowly refill"; "no autosave… the save is lost" |
| `[SPOT]` | Failed defense rolls back to a save; healing scarce | Softlock and lost-progress complaints; "wrong build can dead-end a save" |
| `[KD]` | Fall damage (2.0), host-only saves | Settings/save complaints dominate, not rescue |

**Conclusion:** the punishment players resent is **deletion of carried loot and progress**, not the
existence of a failure state. Time loss alone is accepted; item loss is not.

### 1.2 The abuse question

Rescue in this concept is **automatic at 0 fuel** — the player cannot summon it. So the abuse
vectors are only:

1. **Deliberate drain** — stop digging and burn/hold fuel to 0 to skip the climb. Fuel is also the
   digging resource, so this always costs the most valuable thing the player has (digging time).
2. **Finished player skip** — a player who decides they are done for the session intentionally
   strands themselves to skip the ascent. This is the real abuse case.
3. **Broke player free teleport** — with no money, a wallet-capped flat fee is free.

### 1.3 Options

| Model | Loot | Fee behavior | Abuse resistance | Review risk |
|---|---|---|---|---|
| **A. Depth-scaled fee + auto-debt** | Kept | Fee grows with depth; wallet pays what it can; remainder becomes interest-free debt auto-deducted from future sales | High — deep teleports always cost the most, and the cost is eventually paid | Low |
| B. Flat fee, capped by wallet | Kept | Free when broke | Low at depth, high near surface | Low but abusable |
| C. % of carried loot value | Kept (taxed) | Scales with haul | High | Medium — players read it as "my loot got taxed", close to the hated feeling |
| D. Free rescue | Kept | None | None | Low, but it is a teleport button in disguise |
| E. Legacy: loot loss + fee | Lost | Fee | High | **Highest** — the genre's most-hated mechanic |

### 1.4 Recommendation

**Model A.** Specifics to tune in prototype:

- Fee = `base + depth × rate`, shown live in the HUD as the return-power warning escalates
  ("recovery cost: $X").
- Wallet is charged first; shortfall becomes debt. Debt:
  - never blocks movement, purchases or the ending,
  - auto-deducts from future sales (a small cut until paid),
  - cannot exceed a capped fraction of total lifetime earnings (no permanent ruin).
- Recovery puts you at the surface with full fuel, **all finds intact**, unique items untouched.
- No manual rescue; only 0 fuel triggers it. (Pause-menu rescue stays out.)
- This preserves the trip-planning tension: leaving too early is always better than being rescued,
  because the fee and the lost digging time are pure loss.

---

## 2. Health bar: needed? (Q28)

### 2.1 Evidence

| Game | Health model | Reception |
|---|---|---|
| `[AGADH]` | Health, recharging, harsh fall damage | "Fall damage is not gracious with distance at all"; survival called "absolutely unnecessary"; 1-voxel specks "will break your legs" |
| `[OMT]` | Slow-regen health, no way to buy it | "No way of buying health… going AFK for 5 minutes to let my health slowly refill is just a waste of time" |
| `[MELT]` | No death; freeze → rescue robot | "I liked that you don't die, you freeze instead" — praised even in mixed reviews |
| `[SPOT]` | Health; scarce healing in the city | Healing scarcity listed among city complaints; deaths/rollback frustration |

### 2.2 Recommendation

**No health bar.** The battery is the only depletable resource, and it already carries the
"when do I turn back?" decision. Falls:

- small falls: nothing;
- bigger falls: stagger + battery knock (soft consequence, no chip damage);
- extreme falls (or zero battery anywhere): recovery (Model A fee).

This keeps one single difficulty (`Q25`) coherent: one resource, one failure state, no health
management, no healing items, no AFK regen. If a later prototype shows falls are toothless, the
lever to tune is **battery knock amount**, not adding HP.

---

## 3. Shovel vs. guns: tool evolution (Q30b)

### 3.1 Evidence

| Game | Tool change | Reception |
|---|---|---|
| `[AGADH]` | Shovel → powered → drill, each **strictly better** | Praise: "Getting the drill feels so good after making a mess"; "switches from diggy digging to straight up Hoovering dirt… feels really good" |
| `[MELT]` | Flamethrower → **Tesla gun required for blue snow**, slower, pricier, old upgrades worthless | The #1 design complaint: "completely invalidates your progress… like starting from the beginning" |
| `[OMT]` | Tool never changes, only numbers | "Nothing changes in the game… the gameplay or the tool you have don't evolve" |
| `[KD]` | Pickaxe tiers fine; dynamite trap | "Dynamite is beyond useless" |
| `[SPOT]` | Drill tiers; top drill still small; permanent turret branch | "Even the top drill has a criminally small digging radius"; "to try new turret I have to start completely over" |

### 3.2 Synthesis rules (these are the risk controls)

1. **Investment survives.** Any new dig method inherits the same upgrade track. Never "start again".
2. **No chore switching.** Modes are instant and optional; the game never requires cycling tools.
3. **At least as good where used.** A new method must not be a downgrade in its own situation.
4. **Add, don't replace.** The previous method stays available and remains best in some cases
   (Shave for precision, Scoop for volume).
5. **No separate economy.** One tool, one upgrade line. No gun money sink.

### 3.3 Options

| Option | Description | Risk |
|---|---|---|
| **A. One machine, shared upgrades, optional modes** | The shovel evolves; attachments unlock **Shave** (fast, precise), **Scoop** (big, cheap), late **Nozzle** (projected blast). Final absurd form = shovel-cannon. All modes share the upgrade track | Low — satisfies all five rules |
| B. Separate gun tool, own upgrades | Classic "new weapon" structure | High — repeats the Tesla failure by construction |
| C. No guns, shovel + C4 only | Safest scope | Safe but loses the absurd "it became a machine" escalation you want |
| D. Decide after prototype | Test Shave/Scoop/C4 in the slice, then decide the nozzle | Safe, but delays the game's late-game identity |

### 3.4 Recommendation

**A, validated in the slice.** Concretely:

- The tool keeps one identity and one upgrade level; upgrades automatically improve **all** modes.
- Modes are unlocked by visible attachments bolted onto the same machine (motors, hopper, nozzle).
- The late "gun" is the **nozzle attachment**: it fires a short-range dirt-devouring blast — a
  different feel for specific situations (hard formations, large rooms), not a replacement.
- C4 (already IN) covers the "big boom" fantasy; the nozzle covers "absurd machine" without a
  second economy.
- The final-tier visual is the garage-built monster: a shovel that has clearly become a cannon.

If the prototype shows the nozzle is not fun, drop it and keep Shave/Scoop/C4 — the design stays
valid because nothing else depends on it.
