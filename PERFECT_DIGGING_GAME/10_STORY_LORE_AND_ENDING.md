# 10 — Story, Lore and Ending

> `[MELT]`: "There is no lore, no plot, just dig and uncover things" — players *wanted* the story
> that the props promised. `[KD]`: "Where the hell is the boss fight?", a story that was "essentially
> absent". `[AGADH]`: a story so abrupt it made players refund. The fix is not a huge plot — it is
> **story delivered continuously, tied to the digging, and honest about its scale.**

## 1. Narrative premise (working)

You inherited a house from a grandparent you barely knew, on land with a sealed well and a deed
that says, in old legalese, *"all that lies beneath."* The underground is a layered archaeology of
every previous owner: a mining camp, a drowned town, a cult of crystal, a forge city, a precursor
engine. Each layer answers one question and asks another. The final descent is about what the
grandparent was really protecting — and the player chooses what to do with it.

Tone: warm, wry, a little melancholy, never grimdark. Humor lives in item descriptions, NPC
dialogue and museum plaques — never in undercutting the ending.

## 2. Delivery channels (continuous, passive-first)

| Channel | Count | Purpose | Required reading? |
|---|---|---|---|
| **Lore notes / tapes** | 90 | Layer stories, prior owners' voices | No |
| **Artifact plaques** | 60 | Museum context, world history | Optional |
| **Environmental storytelling** | Every landmark | Show, don't tell: table settings, barricades, murals | No |
| **Hub NPCs** | 6 (trader, smith, archivist, pilot, kid, groundskeeper) | React to progress, give quests, carry B-plots | No |
| **Radio broadcasts** | 18 | World outside, creepy or funny depending on Horror setting | No |
| **Main quest beats** | ~24 | The critical path story | Yes, short and skippable |
| **Museum completion** | 8 wings | Payoff scenes, mechanical perks | Optional |

Rules:

- **Story is delivered where the player already is**: at the shop, in the map UI, in the artifact
  they just found, in a 30-second NPC line. No walk-and-talk escort missions, no forced cutscenes
  mid-dig.
- **Main beats are ≤ 90 seconds each, skippable, replayable** from the archive.
- **The archive UI** tracks everything found, with a "story so far" recap generated from unlocked
  notes (a simple, spoiler-safe summary).
- **No lore item is missable.** Deterministic placement, map-marked via scan.

## 3. Per-layer story arc structure

Each layer follows the same shape so writers can parallelize and players can trust the rhythm:

1. **Arrival** (visual identity + a question)
2. **Evidence** (3–5 notes/artifacts revealing what happened here)
3. **The gate** (the mechanic that must be solved to go deeper, tied to the story)
4. **The revelation** (one short beat that reframes the question)
5. **The trace** (a link to the next layer, usually an object or a name)

Example sketch (Layer 3 Ruins): the buried village sealed its well; notes reveal they were hiding
from something in the deep; the glyph door requires three fragments; the revelation is that the
"something" was the previous digger; the trace is a family name that reappears in Layer 7.

## 4. Ending design (anti-betrayal rules)

The mechanical rules live in `09_ENDGAME_AND_POSTGAME.md`. The narrative rules:

1. **The twist must re-contextualize, not negate.** Bad endings that say "it was all fake / a game
   show / you were a sucker" are banned as main resolutions `[SPOT]` "means nothing", `[AGADH]`
   "you are one in a long line of suckers".
2. **The player's labor is acknowledged.** The finale explicitly reflects the tunnels dug, the
   museum filled, the people helped (stat screen woven into the scene, not a spreadsheet).
3. **Three variants, none canonical-punishing:**
   - **Keep It** — seal the engine and give the land back (cozy default).
   - **Open It** — use the engine; the deep world blooms into the surface (wonder ending).
   - **Share It** — invite the town in; the museum becomes public (community ending).
   Choice is presented clearly, without gotchas, and changeable by replaying the finale from the
   gallery.
4. **The grandparent mystery resolves.** No "the real treasure was the friends we made" cop-out;
   there is an actual answer, conveyed in ≤ 3 minutes.
5. **Post-credits is warm.** A short epilogue shows NPCs reacting to the outcome; it sets up NG+
   without invalidating the choice.

## 5. Optional spooky layer (consent-gated)

For players with Horror enabled (`08_HAZARDS_ENEMIES_AND_HORROR.md`), additional radio
transmissions, the Hollow Choir, and "The Burrow" den tell a **separate, self-contained horror
micro-story** that can never gate the main plot, achievements, or the museum. It ends with a real
reward and a proper resolution for those who opt in.

## 6. Writing budget and production

| Asset | Target | Notes |
|---|---|---|
| Main story words | 12,000–16,000 | Short, punchy, no walls of text |
| Lore/notes words | ~30,000 | Written by 2 writers over production |
| Localization-ready from day 1 | yes | No baked text in textures; string tables + font coverage |
| VO | none at 1.0 (barks only) | Text-first; voice update only if budget allows |
| Narrator | no | The player's own voice is the fantasy |

Localization matters: the comparative corpora include large Russian, Chinese, Japanese, German,
Spanish, Portuguese, French, Korean and Turkish audiences, and `[MELT]` earned specific praise for
full Russian localization. At 1.0: EFIGS + Russian, Portuguese-BR, Simplified Chinese, Japanese,
Korean, Polish, Turkish string-table ready (ship what budget allows, structure supports all).

## 7. Story test checklist

- [ ] No mandatory story beat exceeds 90 seconds.
- [ ] A player can name the Layer 3 story in one sentence after playing it.
- [ ] Every artifact gives a mechanical or narrative reward (`05_ITEMS_AND_RESOURCES.md`).
- [ ] All three endings are reachable, distinct and satisfying (playtest survey).
- [ ] No lore item is missable; archive completion is achievable with horror off.
- [ ] The ending explicitly reflects player stats/tunnels/museum in-scene.
- [ ] Store page and trailer do not spoil or misrepresent the tone.
