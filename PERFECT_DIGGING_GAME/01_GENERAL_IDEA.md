# 01 — General Idea

> **Working title:** Project SHOVEL (final name TBD). One-line pitch: *"A cozy first-person digging
> game with a hand-crafted underground, visible progression, full respect for your time and hands —
> and a finale that pays off instead of trolling you."*

## 1. The fantasy

Players across all five corpora agree on the primal appeal: the childhood dream of digging an
enormous hole in the backyard `[AGADH]`, the Motherload/flash-mining nostalgia `[AGADH]`, the
"primal satisfaction of moving dirt" `[KD]`, the zen of watching material vanish `[OMT]` `[MELT]`,
and the greedy "one more run" risk of a deep dig `[SPOT]`.

The game must deliver four fantasies, in this order of priority:

1. **I am digging a hole.** The verb is tactile, pleasant and endless. It is the game.
2. **I am getting stronger.** Every purchase is felt in the hands within seconds.
3. **I am discovering things.** The underground hides a world: structures, artifacts, stories.
4. **I can stop whenever I want.** No pressure, no punishment, no lost evenings of progress.

## 2. Positioning

| Decision | Choice | Why (evidence) |
|---|---|---|
| Genre | First-person cozy dig-'em-up with light management | The highest-rated games in the comparative set are exactly this, and their fans are explicit about not wanting more `[AGADH]` `[OMT]` `[MELT]` |
| Default tone | Cozy, warm, gently absurd humor | "Relaxing/zen/cozy" is the #1 or #2 praise theme in all five corpora |
| Danger | **Opt-in only** (settings + mode selection at first launch) | Unadvertised monsters are the #1 complaint of `[OMT]`; forced stealth the #1 of `[AGADH]`; forced horror/parkour a top-5 of `[SPOT]` |
| Camera | First-person, full motion-comfort options | Genre convention; every corpus contains motion-sickness complaints |
| Price | $9.99 launch, regional pricing, frequent sales | $5 games were still attacked as "paid demo" for 1–3 h `[AGADH]` `[KD]`; $12.99 was accepted for 10+ h `[SPOT]` |
| Content | 10–14 h critical path, 20–25 h completionist, plus endless | "Too short" is top-2 in every corpus; 5–8 h at $12.99 drew "Early Access vibes" `[SPOT]` |
| Monetization | Buy once, free content updates, cosmetic/supporter DLC only | Paid DLC before the base felt finished drew anger `[MELT]`; free 2.0/1.1 updates bought enormous goodwill `[KD]` `[SPOT]` |
| Platforms at 1.0 | PC + Steam Deck Verified; full controller support | Deck praise and controller complaints are both recurring themes |
| Multiplayer | 1.0 solo-first; co-op as a 1.x update **only if** parity rules in `16_MULTIPLAYER_AND_COOP.md` are met | Co-op is `[KD]`'s whole point but also the source of its worst problems (host-only content, no shared money, desync) |

## 3. Who it is for

**Primary:** fans of PowerWash Simulator, SteamWorld Dig, Motherload; podcast/audiobook players;
people who want a 30–60 minute session that always feels productive; completionists who want a fair
100%.

**Secondary:** co-op friend groups (post-launch), casual streamers, older players who want low-APM
relaxation, players with RSI/motion sensitivity who are currently locked out of this genre.

**Explicitly not for:** horror seekers, PvP players, live-service/season-pass audiences, people who
want a 60-hour grind, people who want mandatory combat.

## 4. The four modes at 1.0 (all from day one)

Mode selection is a first-launch screen with clear descriptions, and can be changed per save
(NG+ carries over). This is the single most important anti-backlash device in the design: the exact
complaints that "ruined" the reviewed games were almost always about *the wrong mode for that
player* `[AGADH]` `[OMT]` `[SPOT]`.

| Mode | Pressure | Enemies/Horror | Fall damage | Hunger/Battery | Notes |
|---|---|---|---|---|---|
| **Cozy** (default for new players) | None | Off | Off (soft stagger) | Battery recharges fast, never punish | Pure fantasy fulfillment `[MELT]` `[OMT]` cozy-mode lesson |
| **Standard** | Light | Off by default; opt-in creatures | Light, forgiving | Real but generous | The "intended" experience |
| **Challenge** | Yes | Increasing waves/creatures | Full | Tight | For the `[SPOT]` audience, clearly labelled |
| **Creative/Endless** | None | Configurable | Off | Off | Terrain saved; also the post-game sandbox |

Every mode remains fully completable for achievements (`18_ACHIEVEMENTS.md`).

## 5. Design pillars (the tie-breakers)

When two features conflict, the higher pillar wins:

1. **The single verb is sacred.** Digging must remain satisfying and un-interrupted. Anything that
   stops the player digging "every 30 seconds" is cut or made optional `[SPOT]` stamina/beer.
2. **Progress, never replace.** No mid-game tool that invalidates prior investment `[MELT]` Tesla
   gun; no stat-only "invisible" upgrades `[OMT]`; upgrades show physically `[MELT]`.
3. **Cozy by default, danger by consent.** Nothing scary or stressful on the critical path without
   explicit opt-in and labelling `[OMT]` `[AGADH]` `[SPOT]`.
4. **Every hour has a purpose.** The economy and story arcs are tuned so the player never has
   "nothing to buy / nothing to do" `[AGADH]` `[MELT]`.
5. **Respect the body.** Hands (hold-to-dig, no RSI), eyes (FOV, no forced blur/shake), hardware
   (performance), and schedule (saves, pause anywhere).
6. **Honest marketing.** Store page, tags, trailer and demo state exactly what is inside — including
   anything scary or stressful `[OMT]` "please label it as a horror game".
7. **The finale pays the bill.** The ending and post-game honor the hours played `[AGADH]` empty
   chest + forced stealth; `[SPOT]` "all that digging, pointless".

## 6. What the game is explicitly NOT

- **Not a horror game.** Horror exists only as an opt-in toggle, is always telegraphed, and never
  removes player agency or tools `[AGADH]` mole finale, `[OMT]` worms, `[SPOT]` chase rooms.
- **Not a stealth game.** Ever. No sequence disables your equipment.
- **Not a survival game.** Battery/heat/weight are soft pacing tools with configurable impact, not
  death spirals. Losing an inventory on a blackout is forbidden `[AGADH]` "want to do bad things to
  the creators" over ore loss.
- **Not a roguelike, not an idle game, not a live service.**
- **Not a clone.** Distinct identity: own art direction, own writing voice, own landmark set, own
  finale. "Asset flip / rip-off" accusations are a permanent tax on `[KD]` and `[OMT]` and must be
  designed out via original, cohesive art `[KD]` "assetflip", `[MELT]` "AI slop" accusations.
- **Not dependent on RNG for progression.** No blueprint lottery replacing shops `[KD]` 2.0.

## 7. Fun hypothesis (to validate in prototype)

- A 10-second dig loop that feels good with a shovel and *better* with each of 6 tool tiers.
- A map that answers "where have I been / what did I miss" in one button press.
- A shop that always has exactly one thing the player wants and can almost afford.
- A landmark every 30–60 seconds of digging, so curiosity never dies `[SPOT]` underground world is
  universally praised as its best asset.
- A 45-minute "I'll just do one more run" session that ends because the player decides, not because
  the game does.

## 8. Success metrics (post-launch)

- Review sentiment on the phrase "too short" < 5% of English reviews (vs. top-2 complaint in the
  comparative set).
- "Performance" mentions in negative reviews < 3% (vs. #1 `[KD]` complaint).
- Zero save-loss bug reports sustained after launch window (vs. all four reviewed PC games).
- Completionist 100% achievement rate reachable in one playthrough (vs. `[AGADH]` NG+ lock,
  `[MELT]` 45/46 bug, `[SPOT]` hostile achievements).
- Steam Deck Verified maintained across patches.
