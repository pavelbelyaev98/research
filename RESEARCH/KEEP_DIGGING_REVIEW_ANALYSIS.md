# Keep Digging — Review Analysis

**What players say is good and bad, based on all 3,266 scraped Steam reviews**

| | |
|---|---|
| **Game** | Keep Digging |
| **Steam App ID** | [3585800](https://store.steampowered.com/app/3585800/Keep_Digging/) |
| **Developer / Publisher** | Wild Dog |
| **Released** | 11 September 2025 |
| **Price at review time** | $6.99 (frequently sold/discounted around $4–5) |
| **Steam rating** | Mostly Positive (~80% of 3,267 reviews) |
| **Reviews analyzed** | 3,266 / 3,267 (2,599 positive, 667 negative) |
| **Scraped on** | 14 September 2026 |
| **Raw data** | `research_data/keep_digging_reviews_raw.json` (1.2 MB) |

## Corpus verification

This was a specific requirement for this document, so it is stated up front:

- **Right game:** there are two similarly named titles on Steam. *Just Keep Digging* (App ID 2974660, 17 reviews) was checked and **excluded**; every review here comes from **Keep Digging, App ID 3585800** (developer Wild Dog, released 11 September 2025).
- **Right endpoint:** all 3,266 reviews were pulled from Steam's per-app endpoint `store.steampowered.com/appreviews/3585800` via cursor pagination (33 pages), so the API itself scopes the data to this App ID.
- **Counts reconcile:** the scrape captured 3,266 of the 3,267 reviews Steam reported live at scrape time (1 negative review was no longer retrievable — likely deleted or hidden), with 2,599 positive (all) and 667 of 668 negative.
- **Quote audit:** every quotation in this document was checked against `keep_digging_reviews_raw.json`, and each was also cross-checked against the raw corpora of the four other review analyses in this repo (One Man's Trash, A Game About Digging a Hole, The Spotter: Dig or Die, Meltopia). **No quote comes from another game's corpus.** Translated quotes are marked "(translated)".

---

## TL;DR

Keep Digging is a first-person voxel digging game — reviewers most often describe it as A Game About Digging a Hole with 8-player co-op — sold for around $5 and overwhelmingly bought by friend groups, Japanese players (465 reviews) and Traditional Chinese players (437). You dig, sell ore, upgrade your pickaxe/backpack/battery, and go deeper; v1.0 ends at 1,000 m with a button that nukes the city above, and the free 2.0 update adds a 5,000 m crafting/survival mode. There is a hidden T-rex boss route, chimpanzee skins, emotes and plenty of joke content.

**Praise (recurring):** the co-op chaos, an addictive "one more dig" loop, a cheap price, the humor/monkey business, upgrade progression with New Game+ carrying gear over, and a surprisingly responsive developer.

**Criticism (recurring):** catastrophic performance (5–15 FPS on high-end PCs, crashes, minutes of shader compilation), digging straight down trivializing the whole game (devs acknowledged it), short content and a refund-friendly runtime, multiplayer ownership problems (host-only bones/buttons/achievements, money not shared), clunky UI with no keybinds/hold-to-dig, asset-flip/rip-off accusations, and a divisive 2.0 update that some players say "patched in stress."

The review section itself is part of the story: a wave of refund jokes, meme "boss guide" reviews, and Chinese-language accusations that the positive rating is bought. All of that is real player behavior in this corpus and is covered in its own section below.

---

## The numbers

| Metric | Value |
|---|---|
| Total reviews scraped | 3,266 (of 3,267 live) |
| Positive / negative | 2,599 (79.6%) / 667 (20.4%) |
| Median playtime at time of review | 3.1 h |
| Median playtime — positive reviews | 3.3 h |
| Median playtime — negative reviews | 1.6 h |
| Reported completion time | ~30 min – 1.5 h rushing straight down; 3–7 h for 100% |
| Median review length | 46 characters |
| Reviews with 100+ characters | 981 |
| Reviews with votes | 1,164 have at least one upvote |
| Review span | 11 September 2025 – 13 September 2026 |

**Language distribution:** English 1,368; Japanese 465; Traditional Chinese 437; Simplified Chinese 187; Russian 165; Turkish 130; German 102; Korean 101; French 76; Brazilian Portuguese 54; Polish 49; Spanish 25; plus smaller numbers of other languages.

**Sentiment by month:**

| Month | Reviews | Positive share |
|---|---|---|
| September 2025 (launch) | 1,822 | 81% |
| October 2025 | 412 | 79% |
| November 2025 | 155 | 82% |
| December 2025 | 152 | 83% |
| January 2026 | 120 | 85% |
| February 2026 | 130 | 84% |
| March 2026 | 102 | 73% |
| April 2026 | 101 | 82% |
| May 2026 (2.0 backlash period) | 131 | 63% |
| June 2026 | 49 | 71% |
| July 2026 | 43 | 63% |
| August 2026 | 28 | 93% |
| September 2026 | 21 | 67% |
| **Overall** | **3,266** | **79.6%** |

**Theme frequency — keyword mentions across all 1,368 English reviews:**

| Theme | Mentions | Positive | Negative |
|---|---|---|---|
| price / value | 176 | 134 | 42 |
| co-op / multiplayer | 156 | 114 | 42 |
| optimization / FPS / lag | 130 | 44 | 86 |
| devs / updates | 102 | 61 | 41 |
| monkey / chimp / skins / emotes | 98 | 75 | 23 |
| vs. "Digging a Hole" comparisons | 70 | 45 | 25 |
| achievements | 65 | 48 | 17 |
| straight-down digging | 61 | 35 | 26 |
| v2.0 | 57 | 33 | 24 |
| refunds | 55 | 32 | 23 |
| blurry / dark / visual issues | 53 | 26 | 27 |
| relaxing / chill | 43 | 37 | 6 |
| dynamite | 37 | 25 | 12 |
| crash / BSOD | 34 | 11 | 23 |
| repetitive / boring | 29 | 11 | 18 |
| ESC / menus | 28 | 14 | 14 |
| story / lore | 27 | 20 | 7 |
| ending / nuke | 25 | 15 | 10 |
| v1.0 / legacy (vs 2.0) | 25 | 15 | 10 |
| battery / energy | 24 | 15 | 9 |
| addictive ("one more", "can't stop") | 21 | 21 | 0 |
| short / speedrun | 21 | 9 | 12 |
| desync / disconnects | 21 | 10 | 11 |
| save / progress loss | 20 | 8 | 12 |
| asset flip / rip-off | 20 | 5 | 15 |
| shader compilation / loading | 18 | 6 | 12 |
| boss / T-rex / fossils | 17 | 14 | 3 |
| tutorial | 15 | 8 | 7 |
| sprint / movement | 14 | 5 | 9 |
| workers / NPCs | 13 | 7 | 6 |
| shared money | 12 | 4 | 8 |
| crypto-miner suspicion | 11 | 6 | 5 |
| click / hold-to-dig | 11 | 6 | 5 |
| keybinds | 9 | 5 | 4 |
| host-only content | 9 | 6 | 3 |

The Japanese and Chinese reviews carry the same top themes: among 465 Japanese reviews, "straight-down digging" (直下) appears in 70 and multiplayer terms in 74; among 187 Simplified Chinese reviews, "optimization" appears in 39 (26 negative) and "refund" in 31.

---

## What the game is (for context)

A first-person voxel digging game for 1–8 players. You start on a small city plot with a merchant, an upgrade station and a worker area. **Core loop:** click to dig → collect ore and gems (stone, coal, iron, copper, silver, gold, amber, amethyst, emerald, sapphire, ruby, diamond, uranium, adamantine…) → sell at the surface → upgrade pickaxe/shovel (dig radius), backpack, battery/energy, rope/wire traversal, and dynamite → dig deeper. Fast-travel "manhole" checkpoints appear at intervals; consumables include batteries, warp stones, radar, spray paint and dynamite. Ore finds sometimes hide caves, temples, ruins and chests that grant skins, emotes and worker upgrades; NPC workers provide passive income. The goal in 1.0 is 1,000 m, where a red button triggers an ending cutscene (an aircraft bombs the city from above) and offers a reset that keeps your upgrades — a New Game+ in all but name — with new skins to unlock. A hidden T-rex/dinosaur storyline runs through fossil bones found at specific depths; several detailed community guides describe summoning a T-rex boss with them (see the boss note below). The free **2.0 update** adds a second mode with a 5,000 m map, smelting/crafting, blueprints, orbs/equipment rarity, fall damage, friendly fire, and separate progress. The humor is deliberate: chimp/monkey skins, a clown, silly emotes, a golden chimp, and a merchant jokingly described as "John Capitalism."

**Corpus verification and boss note:** early reviews (launch week) insist there is no boss and no combat, while later reviews and detailed Korean/Traditional Chinese guides describe a hidden T-rex fight unlocked by collecting fossils, pressing hidden buttons and using specific emotes; treat the boss as **missable hidden content that most players never see**, and note that some reviews claiming it exists are joke/troll "guides."

---

## What reviewers praise (the good)

### 1. Co-op with friends is the whole point — and it delivers
The dominant positive: digging together (and racing each other for ore) is chaotic, funny and worth the price. Many reviews explicitly recommend it as a one-night party game with friends.

> "It understands the primal satisfaction of moving dirt is amplified exponentially when you are racing a friend to the deepest layer." — English, 0.4 h, positive, 21 upvotes
>
> "Being a digger with the boys life is good just dig. Its not much but its honest work." — English, 2.7 h, positive, 13 upvotes
>
> "It's a fun but short game. Between the 4 of us digging down the same hole, we beat it in less than 1.5 hours. I feel like we each got our $5 worth." — English, 1.7 h, positive, 14 upvotes
>
> "The chaos, the teamwork (or lack thereof), the clutch moments—it all adds up to some of the most fun I've had in a co-op game in a long time." — English, 4 h, positive

### 2. A simple, addictive "one more dig" loop
Reviewers describe losing entire evenings, digging long past bedtime, and a zen-like flow that pairs well with music or a podcast.

> "ok this game is actually dangerous lol, one more dig turned into 3 hours somehow. Super simple but honestly can't put it down!" — English, 13.7 h, positive, 10 upvotes
>
> "I was playing this until almost 8am. I yearn for the mines... Eyes bloodshot... cant... stop... digging..." — English, 4.8 h, positive, 19 upvotes
>
> "Every layer has its own surprises, every upgrade feels earned, and the deeper you go, the harder it is to pull yourself away." — English, 9 h, positive
>
> "Gameplay is a legal way to destroy your weekend." — Russian, 5.2 h, positive (translated)

### 3. Cheap, and honest about what it is
At ~$5, most reviewers consider it a fair or excellent value, even those who finish in one evening. "One hour per dollar" reasoning appears repeatedly.

> "I paid less than $5 for it and was entertained for a couple of hours. What more can you ask for?" — English, 2.8 h, positive, 10 upvotes
>
> "A lot funner than i thought it would be! Had a great time just digging ya know, a girl yearns for the mines. Great visuals too!" — English, 7.3 h, positive, 38 upvotes
>
> "Best $6.75 i've ever spent. Would've been happy to have paid 15." — English, 4.5 h, positive

### 4. Humor, monkeys and meme value
Chimp skins, worshiping cathedrals, emotes and an absurd ending give the game a personality that reviewers enjoy quoting. The chimp transformation is a recurring favorite.

> "Deep underground you'll find plenty of mine shafts, chambers, cathedrals and OMG they're worshipping the chimpanzee." — English, 9.6 h, positive
>
> "you and your friends can be chimpanzees! OOH OOH AH AH! Chimp Possy!" — English, 4.4 h, positive
>
> "OMG the ending made me laugh so hard!! I don't think Ive ever laughed so hard at the end of a game." — English, 18.2 h, positive

### 5. Progression and New Game+
Upgrades are tangible, the reset keeps your gear, and 100% is achievable in a single relaxed run — a common point in the game's favor.

> "Watching your tools evolve and knowing you can now dig further or faster brings a genuine sense of accomplishment." — English, 9 h, positive
>
> "Getting 100% is a real pleasure, not a chore." — French, 3.3 h, positive (translated)
>
> "After resetting, the terrain returns to its original state and you can unlock new skins; upgrades, enhancements and items are all retained." — Simplified Chinese, 3.8 h, positive (translated)

### 6. Relaxing, podcast-friendly, no-pressure mining
No combat (in practice), no fall damage, free battery recharge after max upgrades, radar and fast travel — reviewers call it a "mindless" game in the best sense.

> "The game is exactly what it promises — a chill, laid-back experience… just pure zen digging, selling treasures, and upgrading your gear." — Czech, 5.8 h, positive (translated)
>
> "this is a game for people who like to mindlessly mine in other games while listening to a podcast or something." — English, 5.9 h, positive
>
> "The game is meditative, dumb, addictive and absolutely wonderful." — Russian, 5.2 h, positive (translated)

### 7. A responsive developer and a generous free update
The devs patched fast after launch, added a performance mode, and later shipped the large 2.0 update for free — a point of goodwill even among critics of the update's direction.

> "they could have made a 10 dollar game then just abandoned it, but instead they ADDED on a 2.0 version which is MUCH more time consuming" — English, 8.4 h, positive
>
> "Wild Dog gave the game a free update that many another publisher would have sold as a fat DLC." — German, 13.7 h, positive (translated)
>
> "as i posted this review, the game got an update wich fixed the issue, i am now recommending this game if you have some friends to mess about with lol" — English, 6.8 h, positive

### 8. Atmosphere and small details (niche)
Fossils, temples, mineshafts, an underground "civilization" that changes with depth, satisfying dig sound, and an ending that shows your tunnels in cross-section are singled out by fans.

> "As you go deeper underground, civilization evolves, and it's nice that you get a little curious: 'What's next…?'" — Japanese, 1.9 h, positive (translated)
>
> "The lack of BGM was wonderful. I love silently continuing to work with only ambient sounds… For us miners, BGM is the sound of drilling, after all." — Japanese, 1.5 h, positive (translated)
>
> "The sound design punctuates every strike of the pickaxe with a satisfying clonk, as though the Earth itself is reluctantly acknowledging my authority." — English, 2.6 h, positive

---

## What reviewers criticize (the bad)

### 1. Performance is the #1 complaint by a wide margin
FPS in the single digits on RTX 3070/4090-class hardware, high CPU/RAM load, minutes of shader compilation on every launch, long loads, overheating, occasional BSoD, and a joke-turned-suspicion that the game is secretly mining crypto.

> "Solid 11fps on a 3070" — English, 0.2 h, negative, 13 upvotes
>
> "Near zero optimization. So much lag it hurts." — English, 0.2 h, negative, 70 upvotes
>
> "This game's more about digging into my CPU and RAM then actually digging into the ground" — English, 0.2 h, negative, 30 upvotes
>
> "shaders compiling, shaders compiling, shaders compiling, shaders compiling. This is a BIG issue every game load." — English, 0.1 h, negative, 53 upvotes
>
> "The game runs fine at the start, but the longer I played, the more my frames dropped, till it was barely 30fps. This was at lowest graphics too" — English, 16 h, negative, 10 upvotes
>
> "The strain this game has on CPU and GPU makes me question if it does have a secret crypto mining app in it." — English, 1.4 h, negative, 8 upvotes

### 2. Digging straight down trivializes the game
The fastest strategy is to dig vertically to 1,000 m, skipping exploration, upgrades and content. The developers acknowledged this in patch notes; reviewers see it as the core design flaw.

> "This game would have geen 100 times better if only the developers prevented players to dig straight down and beat the game in under an hour" — English, 1.2 h, negative, 68 upvotes
>
> "My friends spoiled the game by digging straight down." — English, 1.8 h, negative, 9 upvotes
>
> "Just dig straight down, no need to care about anything" — Traditional Chinese, 0.9 h, negative (translated)
>
> "I found, like others, that the game could be very easily completed linearly, with very little actual underground exploration." — English, 0.2 h, negative, 11 upvotes
>
> The developers' own patch note is quoted in a top review: "It's too easy to clear by digging straight down." → "We're considering new content that can't be cleared by straight-down digging." — English, 1.9 h, positive

### 3. Short, repetitive, little replay value
Critical-path completion takes ~30–90 minutes; reviewers complain there is no randomization, the same landmarks repeat, and once you finish there is nothing to do but achievement hunt.

> "quickly put together friendslop with assets from the unity store and no cohesive identity beyond What if we made Digging a Hole but multiplayer. There is no randomization of the level so every full playthrough will be about the same." — English, 3.4 h, negative, 97 upvotes
>
> "This game is only fun with friends for about an hour, so its only worth about a dollar" — English, 1.8 h, negative
>
> "Very basic game that you'll finish in an hour. Just dig straight down. No challenge or progress in gameplay, just digging down." — English, 2.1 h, negative, 20 upvotes

### 4. Multiplayer ownership problems and desync
Reviewers expected shared loot and money; instead money isn't shared despite the store description, dinosaur bones/end-game buttons are host-only, guests can desync or fail to join, and some achievements are host-only.

> "Firstly, money isn't shared, as suggested by the description of the game" — English, 36 h, negative, 11 upvotes
>
> "as you reach checkpoints you find dinosaur bones and only the host can pick them up" — English, 1.8 h, negative
>
> "Multiplayer is not synchronized" — Japanese, 0.8 h, negative (translated)
>
> "New version of the game is a huge disappointment and definitely worse than the legacy version… Everyone in multiplayer shares chest space / Does not share money / Does not share blueprints" — English, 4.3 h, negative, 22 upvotes

### 5. Crashes and save/progress loss
Crashes every few minutes on some systems; a first crash can leave the game unable to launch; settings reset every session; dug ore and even dug holes can disappear on reload.

> "deal breaker If it crashes once, it breaks completely It won't launch again no matter what fix you try" — English, 1.7 h, negative, 43 upvotes
>
> "When you load back into your world, the grass on the very top layer re-appears with no way to remove it" — English, 1.4 h, negative
>
> "After pressing save and exit, the progress was all gone" — Traditional Chinese, 4.6 h, negative (translated)

### 6. UI, controls and missing quality of life
No key rebinding, ESC doesn't close menus, settings don't persist, no sprint (Shift and Space are both jump), no hold-to-dig (one click per swing), blurry visuals with no brightness/bloom controls, and no proper tutorial.

> "Why it doesn't let you just hold left click to dig is beyond me." — English, 4.7 h, negative
>
> "Menus are a bit clunky and don't have good programming behind them (ie ESC button should close the menu)" — English, 0.1 h, negative, 53 upvotes
>
> "No spinting?… The overall design language doesn't seem cohesive. This game needs to be as polished as 'Digging a Hole'" — English, 0.1 h, negative, 53 upvotes
>
> "the incessant left-clicking will give you carpal-tunnel syndrome" — English, 1.6 h, negative

### 7. "Asset flip" and rip-off accusations
A large share of negative and mixed reviews call it a blatant clone of A Game About Digging a Hole built from store assets, with no identity of its own.

> "Blatant ripoff of A Game About Digging a Hole" — English, 1.8 h, negative, 9 upvotes
>
> "A total rip-off of A Game About Digging A Hole, made worse." — Japanese, 2.5 h, negative, 14 upvotes (translated)
>
> "This game reeks of an assetflip… Its essentially a carboncopy of the aforementioned game with more content, worse graphics, worse performance and worse gameplay." — English, 0.3 h, negative

### 8. Dynamite is weak, confusing and host-limited
Dynamite costs a lot, clears little, and in multiplayer only the host's upgrades apply — frequently called a trap upgrade.

> "Dynamite is beyond useless. Left-clicking twice at any stage of the game has bigger impact than throwing a dynamite." — English, 2 h, negative
>
> "bombs do nothing" — Traditional Chinese, 2.4 h, negative (translated)
>
> "Friends leveling up their dynamite up to level 5, is still equivalent to level 1 damage. Leveling up dynamite only affects the host, not the other players." — English, 7.9 h, positive-with-criticism

### 9. The ending, story and missing boss
The story is essentially absent; the 1,000 m ending is a button press and a cutscene nuking the city, which many found baffling. Some early reviews flatly deny that the boss exists.

> "You dig to the bottom, a fighter jet bombs the city, and that's it. Huh?" — Traditional Chinese, 1 h, negative (translated)
>
> "Thanks everyone in the comments for making me work two extra hours like child labor. Where the hell is the boss fight?" — Traditional Chinese, 3.3 h, negative (translated)
>
> "The boss fights are lies, there is no combat system at all" — Simplified Chinese, 0.8 h, negative, 86 upvotes (translated)

### 10. The free 2.0 update split the community
2.0 added crafting, orbs and 5,000 m, but many long-time players say it made the game slower and more stressful, moved tools behind RNG blueprints, removed teleport totems, and hurt the "dumb fun" pacing.

> "I did not buy this to play an actual game, I bought this to dig a hole. 2.0 made it into a Minecraft-esque game with things to do and damage to take. I did not sign up for that. I signed up to dig a hole stress free. 2.0 patched in stress. 1.0 is PHENOMENAL though." — English, 20.5 h, positive, 14 upvotes
>
> "I loved the first version. After the update it is unplayable." — English, 1.5 h, negative
>
> "V2.0 introduces blueprints, which in theory adds more complexity to the gameplay, but coupled with the fact that there's RNG involved… you can no longer purchase tools past Copper in the store" — English, 16 h, negative, 10 upvotes
>
> "2.0 patched in stress. 1.0 is PHENOMENAL though." — English, 20.5 h, positive (same review, condensed)

### 11. Visuals and readability
Blurry textures, forced bloom, extreme darkness and pop-in are common complaints; several reviewers report headaches or motion sickness from the underground sections.

> "Game is extremely blurry and no matter what I do it's still very blurry. Unplayable as is." — English, 1 h, negative
>
> "I just get motion sick." — Japanese, 0.9 h, negative (translated)

---

## The review section itself: refund jokes, meme guides and fake-review fights

This game's review section deserves its own note, because it affected how several reviewers judged the game:

- **Refund jokes are a genre here.** Multiple high-upvote positive reviews are literally "beat it in under 2 hours and refunded" jokes. The top upvoted positive review at one point read: "Amazing game. The best thing about it is that you can finish it in 40 minutes and refund it." (English, 0.8 h, positive, 43 upvotes). Another: "I give this game, 5 steam refunds out of 10." (English, 1.8 h, positive, 9 upvotes). Russian reviewers posted similar lines: "We got through it with the lads in 49 minutes and got a refund. Got almost all the achievements, thanks a lot!" (translated).
- **Fake "boss guide" reviews.** Parts of the review section contain elaborate joke guides: a WoW-style multi-phase T-rex raid guide with aggro phases and elemental resistances, a cosmic "Lost Ark: First Sin" lore rewrite, and a troll "real boss unlock" guide. None of this matches the actual game systems; treat such reviews as memes.
- **Fake-review accusations.** A number of Simplified and Traditional Chinese reviews (including top-voted negatives) accuse the game's Mostly Positive rating of being bought/astroturfed — "Run away, the Very Positive rating is fake and bought" (translated) — and specifically attack the meme/boss-guide reviews as astroturfing. English reviewers make the same accusation more loosely ("These people clearly paid for reviews"). Whether or not any astroturfing occurred, the review section is visibly shaped by joke content and counter-accusations, which is why this document relies on aggregate patterns rather than review-score alone.

---

## Divergent and mixed opinions

| Topic | For | Against |
|---|---|---|
| Co-op | The reason to buy; chaotic fun with 2–8 friends | Broken sync, host-only content, money not shared, some prefer solo |
| Straight-down digging | A fun speedrun / meme in itself; "i am simpl man, i dig hole" | Destroys exploration and progression; devs acknowledged it |
| Length | Fine for $5; "each got our $5 worth" | 30–90 min critical path; refund jokes; "only worth a dollar" |
| v1.0 vs 2.0 | Free update, more content, crafting depth | "Patched in stress", slower, RNG, some say unplayable |
| Performance | Patches improved it; some run it fine | The dominant criticism: low FPS, crashes, shader waits |
| Boss / T-rex | Hidden fight with guides, fossils, dynamite; a great payoff for some | "There is no boss"; many never see it; others call it a lie |
| Asset reuse | Cheapness is upfront; fun matters more | "Asset flip", "rip-off", "no soul" |
| Review score | 80% positive; genuinely liked by many | Accusations of bought/meme positive reviews |

---

## Who the reviews say should buy it

**Recommended for:** a friend group looking for a cheap, funny one-or-two-night co-op game (2–4 players seems to be the sweet spot); fans of A Game About Digging a Hole who want multiplayer; players who enjoy mindless digging with music or podcasts; achievement hunters and anyone who wants an easy 100%.

**Not recommended for:** solo players wanting meaningful progression or a story; anyone with a mid-range or weaker PC (performance complaints are the single biggest theme); players who will optimize the fun out of it by digging straight down; completionists bothered by host-only content; and players sensitive to blur/motion in first-person games. The most common advice is to buy it cheap, play it in one session with friends, and treat it as a party game rather than a long-term sim.

---

## Caveats

- This document summarizes player opinion, not a technical review. Performance and crash reports cluster around launch (September 2025) and around the 2.0 update (2026); the developer shipped patches (performance mode, CPU cap, Y-invert, faster battery recharge) and some reviewers updated their reviews after fixes.
- The sample is every review retrievable via the App ID 3585800 review endpoint on 14 September 2026 (3,266 of 3,267). All quotations were verified against that raw file; translated quotes are marked.
- Review-section culture (refund jokes, meme guides, astroturfing accusations) means individual reviews should not be taken at face value; the aggregate theme counts and the corroboration of themes across English, Japanese, Chinese and Russian reviews are more reliable than any single quote.
- Quotes were lightly cleaned (line breaks, censored profanity, formatting tags) and translated from Japanese, Chinese, Russian, German, French, Czech, Turkish and others where necessary. Attribution gives language, playtime, sentiment, and vote count for the highest-voted quotes.
