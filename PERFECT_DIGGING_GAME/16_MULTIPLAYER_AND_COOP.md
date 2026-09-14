# 16 — Multiplayer and Co-op

> Co-op is `[KD]`'s entire identity and the source of both its best reviews and many of its worst:
> loved — "the primal satisfaction of moving dirt is amplified exponentially when you are racing a
> friend"; hated — "money isn't shared, as suggested by the description", "only the host can pick
> up dinosaur bones", "multiplayer is not synchronized", host-only achievements, dynamite upgrades
> only applying to the host.
> Co-op is **solo-first, added only when parity is guaranteed**. If the rules below cannot be met,
> it ships later — or not at all. Broken co-op poisons the whole product's review score.

## 1. Scope decision

- **1.0: single-player only, built and tuned as such.**
- **1.x (target: +3–6 months): co-op for 2–4 players**, cross-platform PC/Deck between Steam
  friends. 8-player is a stretch goal only if sync telemetry holds.
- Co-op is **content-complete with solo**: same world, same story, same achievements, same modes.
  No co-op-exclusive happy path.

## 2. Parity rules (hard requirements)

| Rule | Detail | Failure prevented |
|---|---|---|
| **Shared money (default)** | All income goes to a shared pool; optional "split" toggle at lobby creation | `[KD]` "money isn't shared" |
| **Shared unlocks** | Tool tiers, map reveals, checkpoints, modules are party-wide; individual capacity/loadout is per-player | `[KD]` host-only bones/buttons |
| **Every player can interact with everything** | Keys, buttons, chests, quests, collections | `[KD]` host-only content |
| **Achievements for everyone** | Conditions are tracked per player, unlocked for all participants where the action was shared | `[KD]` host-only achievements |
| **Story progression for all** | A shared campaign flag; guests can continue solo later with their own character? — design answer: **party save** (see §5) | `[SPOT]`/`[KD]` progress loss on switching |
| **Danger settings use the minimum** | Creatures/horror/fall settings = lowest common denominator unless host explicitly overrides with consent | Accessibility: a guest must never be forced into horror `[OMT]` |
| **No player tether** | Players can split up across the whole map; map/waypoints shared | "Babysitting" complaints |
| **No friendly fire** (default) | Optional in Challenge with clear labelling | `[KD]` fall damage/friendly fire friction |

## 3. Networking design

- **Host-authoritative with client prediction** for movement/digging; terrain edits applied
  deterministically from the shared seed + operation log.
- **Terrain deltas only** over the wire (dig/place ops), not voxel streams; late joiners receive a
  compressed world snapshot + op log.
- **Steam Datagram/relay or LAN**; NAT punch-through with relay fallback; join-in-progress.
- **Disconnect resilience:** a dropped guest keeps their character/inventory locally and can
  rejoin the same session (a 10-minute grace window); host crash → the party save is recoverable
  from the last autosave by any member. `[KD]` "if it crashes once, it breaks completely".
- **Lobby UX:** Steam friends list invite, join code, lobby browser for public Endless seeds;
  ready-up; "continue from party save".
- **Ping/packet-loss UI:** latency indicator with explanation; the game states its region/relay.

## 4. Co-op-specific design

| System | Co-op design |
|---|---|
| Revive | Downed players can be revived by a teammate in 3 s; otherwise respawn at checkpoint (no item loss) |
| Inventory | Per player; shared storage chest at hub with per-player tabs; trade window |
| Money | Shared pool (default) or split (toggle); visible contribution stats for fun |
| Checkpoints | Shared; activating gives every player the network |
| Scan/map | Shared fog + per-player temporary pings |
| Contracts | Party-wide objectives with individual contribution tracking |
| Difficulty | Enemy/hazard scaling tied to player count only in Challenge; Cozy stays cozy |
| Emotes/comms | Ping wheel (go here / danger / look / thanks), emotes, text chat, optional voice via
platform |
| Griefing controls | No terrain destruction of placed structures by others; optional "player-placed
blocks untouchable" rule; host toggles |

## 5. Saves in co-op

- **Party save** owned by the host but portable: any participant can host the next session from
  their cloud copy without losing progression (each guest's museum/cosmetics remain theirs).
- Guests earn their own cosmetics/museum items in their profile; campaign completion is recorded
  for every participant.
- No host-only achievements or items. Ever. `[KD]` rule.

## 6. Performance in co-op

- Budget: 4 players + 2,000 m world updates ≤ 2 MB/s upstream per client at 20 Hz net tick for
  terrain ops (digging is batched at 10–20 Hz with prediction).
- Soak test: 4 clients, 3 hours, 33% packet loss simulation, 200 ms latency, verify no desync of
  terrain hash.
- Terrain hash reconciliation runs every 30 s; mismatch triggers a delta resync (never a save wipe).

## 7. Post-launch success gates for co-op

Ship co-op only when all are true:

- [ ] 4-player terrain hash stays identical for 3 hours under packet-loss soak.
- [ ] Reconnect after forced disconnect works 20/20 attempts.
- [ ] Party save migration between two Steam accounts works end-to-end.
- [ ] All achievements unlock for guest and host in a scripted co-op run.
- [ ] Shared money/unlocks verified by automated gameplay bot for both players.
- [ ] Guest with all danger toggles off is never subjected to creatures/horror from other players'
      settings.
- [ ] Performance with 4 players stays within the solo 60 FPS target on recommended hardware
      (±10%).
