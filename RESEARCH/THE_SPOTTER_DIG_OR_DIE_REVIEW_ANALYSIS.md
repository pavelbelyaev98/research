# The Spotter: Dig or Die — Review Analysis

**What players say is good and bad, based on all 1,859 scraped Steam reviews**

| | |
|---|---|
| **Game** | The Spotter: Dig or Die |
| **Steam App ID** | [3976500](https://store.steampowered.com/app/3976500/The_Spotter_Dig_or_Die/) |
| **Developer / Publisher** | Puppyroar Games / Forklift Interactive, Gamersky Games |
| **Released** | 7 April 2026 |
| **Price at review time** | $12.99 |
| **Steam rating** | Very Positive (~85% of 1,860 reviews) |
| **Reviews analyzed** | 1,859 / 1,860 (1,585 positive, 274 negative) |
| **Scraped on** | 14 September 2026 |
| **Raw data** | `research_data/the_spotter_dig_or_die_reviews_raw.json` (3.1 MB) |

**Method:** Every review in every language was pulled from Steam's public `store.steampowered.com/appreviews/3976500` API via cursor pagination (19 pages; 1 review was no longer retrievable). Themes were quantified by keyword analysis across the whole corpus; all 274 negative reviews were read in full, along with a qualitative deep-dive of the 332 substantive positive reviews (250+ characters) and the highest-voted reviews of each sentiment. Quotes are verbatim (translated where the original was not English) with language, playtime, sentiment and upvotes where useful.

---

## TL;DR

The Spotter: Dig or Die is a first-person digging + tower-defense survival game: dig for scrap and ore under a ruined Nevada gas station by day, then defend it from mutant hordes by night. It sold well on launch (~1,240 reviews in its first month), drew comparisons to Dome Keeper and A Game About Digging a Hole (some reviewers call it a "near-literal clone" of the latter), and remains Very Positive overall.

Reviewers overwhelmingly agree on the shape of their experience:
- **The first 2–4 hours are great.** The day/night loop — greedy digging versus getting home in time to fight — is genuinely addictive, and the underground world of bunkers, easter eggs and secrets is the game's best asset.
- **The middle sags and the back half frustrates.** The stamina/beer system forces constant trips to the surface; upgrades are gated behind tedious resource tiers; the tower-defense side either plays itself via AI turrets or requires babysitting; and the Las Veganos city update is widely disliked.
- **The ending disappoints.** Most reviewers who finish describe the payoff as abrupt, silly or a let-down, with no New Game+ or endgame.
- **Technical trouble is the other big theme:** save loss, crashes, softlocks, broken achievements, and — unusually often — motion sickness/eye strain.

---

## The numbers

| Metric | Value |
|---|---|
| Total reviews scraped | 1,859 (of 1,860 live) |
| Positive / negative | 1,585 (85.3%) / 274 (14.7%) |
| Median playtime at time of review | 7.6 h |
| Median playtime — positive reviews | 7.9 h |
| Median playtime — negative reviews | 5.2 h |
| Reported completion time | ~5–12 h (most 6–10 h; completionists 15–30 h) |
| Median review length | 67 characters |
| Reviews with 100+ characters | 760 |
| Reviews with votes | 404 have at least one upvote |
| Review span | 7 April – 14 September 2026 |

**Language distribution:** English 707; Simplified Chinese 365; Russian 311; Traditional Chinese 62; Spanish 60; French 57; Turkish 54; German 49; Korean 40; Brazilian Portuguese 35; Japanese 35; Polish 23; plus 11 more languages (16–9 reviews each).

**Sentiment by month (all languages):**

| Month | Reviews | Positive share |
|---|---|---|
| April 2026 (launch) | 1,239 | 87% |
| May 2026 | 246 | 85% |
| June 2026 (1.1 "Las Veganos" update) | 175 | 80% |
| July 2026 | 121 | 83% |
| August 2026 | 59 | 78% |
| September 2026 | 19 | 84% |
| **Overall** | **1,859** | **85.3%** |

**Theme frequency — keyword mentions across all 707 English reviews:**

| Theme | Mentions | Positive | Negative |
|---|---|---|---|
| price / value / refund | 115 | 101 | 14 |
| zombies / mutants | 85 | 67 | 18 |
| grind / repetitive / tedious | 80 | 55 | 25 |
| humor / toilet humor | 73 | 66 | 7 |
| devs / updates | 69 | 53 | 16 |
| addictive ("one more") | 66 | 65 | 1 |
| day / night cycle | 60 | 48 | 12 |
| car | 53 | 41 | 12 |
| difficulty / balance | 52 | 44 | 8 |
| tower defense | 50 | 44 | 6 |
| turrets | 48 | 39 | 9 |
| bugs / crashes | 45 | 37 | 8 |
| story / lore | 45 | 41 | 4 |
| ending | 40 | 30 | 10 |
| dog / Frodo | 38 | 32 | 6 |
| relaxing / cozy | 38 | 36 | 2 |
| stamina / beer | 37 | 26 | 11 |
| secrets / artifacts / bunkers | 35 | 27 | 8 |
| replay / procedural | 35 | 27 | 8 |
| performance / FPS | 33 | 22 | 11 |
| achievements | 31 | 23 | 8 |
| respec / locked choices | 28 | 21 | 7 |
| co-op requests | 24 | 23 | 1 |
| UFO / aliens | 21 | 16 | 5 |
| jetpack | 18 | 7 | 11 |
| backpack / inventory | 17 | 12 | 5 |
| parkour / jumping | 17 | 9 | 8 |
| Las Vegas / Las Veganos | 9 | 6 | 3 |

Keyword counts skew low for themes reviewers discussed in Chinese and Russian (most detailed criticism is written in those languages): e.g. motion sickness is mentioned by 10 negative Chinese reviews alone, and guidance problems dominate the Chinese negative reviews.

---

## What the game is (for context)

A first-person post-apocalyptic hybrid. You are the last "Spotter" at a sandstorm-wrecked gas station in Nevada, repairing a radio receiver to hear the President's final message. **By day** you dig a shaft beneath the station, recycle junk and ore (scrap, iron, gold, diamonds) into resources, and buy upgrades. **At night**, mutant waves attack and you either man the roof gun yourself or rely on automated turrets and barricades. Progression runs through five "tiers" gated by receiver/relay repairs, with branching choices for your drill, backpack, stamina, jetpack and health, for turrets (sniper/railgun, gatling/Tesla, artillery) and for the base. Underground it is full of hand-placed points of interest: bunkers, mines, fossils, crashed vehicles, Half-Life-style easter eggs, horror rooms and minigames. There is a slot machine, an arcade cabinet, a basketball hoop, a buildable car, and a dog named Frodo who can be abducted by a UFO and returned as a base defender. It is single-player only. A demo was available before launch; the game shipped without Early Access.

---

## What reviewers praise (the good)

### 1. The day/night loop is genuinely addictive
The dominant praise: dig greedily, watch the clock, race home, fight. Reviewers describe losing entire sessions to it and wanting "one more day."

> "I started playing the game, played my first 2 hours and didn't even know I played that long. It was like I couldn't put the mouse and keyboard down." — English, 3.1 h, positive
>
> "Very addictive. 10 hours in and ive evolved into a cave dwelling goblin." — English, 10.5 h, positive, 21 upvotes
>
> "Digging by day and blasting mutants at night is such a sick loop." — English, 0.3 h, positive
>
> "Every time I unlocked something new I'd think, 'just one more upgrade,' and then two hours would disappear." — English, 29.3 h, positive

### 2. Digging is satisfying and the progression is tangible
The shovel-to-drill power escalation, the resource loop, and the way upgrades feed into each other earn consistent praise — at least for the first several hours.

> "The progression loop is outstanding. You really feel like leveling up makes a difference, while at the same time, it doesn't feel too terribly grindy." — English, 7.6 h, positive
>
> "You start with practically a rusty shovel and the pitiful remains of a base, and gradually get more powerful tools, a jetpack, explosives." — Russian, 23.7 h, positive (translated)
>
> "The digging is a bit therapeutic for me, and even makes me want to get every speck of dirt to see if there are some scrap metal items hidden inside of the clumps." — English, 15.7 h, positive

### 3. Night defense and the FPS layer work
Reviewers like that the tower-defense phase isn't hands-off: you can jump on the main gun and shoot. Headshot feel and the pressure of the countdown are recurring positives.

> "Digging during the day trying to push deeper and deeper while balancing the time it takes to get back up to defend your base in time is actually pretty fun… you're not just placing defenses and watching, you are actively involved in the fights." — English, 7.5 h, positive, 45 upvotes
>
> "Killing zombies is very satisfying. The gun-feel and the death animations are spot on." — English, 19.4 h, positive
>
> "during the day you're calmly digging, planning, being greedy for 'just one more run'… and then night hits and everything turns into chaos" — English, 1.6 h, positive

### 4. The underground world, secrets and easter eggs
Even harsh critics tend to single out the hand-built underground as the game's strongest asset: bunkers, horror rooms, pop-culture references and surprises that keep you digging.

> "It's got quite a lot of depth (pun not intended) and unique areas and secrets to find underground." — English, 4.3 h, positive
>
> "The number of secrets, locations and references goes off the charts." — Russian, 11.2 h, positive (translated)
>
> "The game's single genuine achievement is its underground world… New subterranean structures first appear as unknown metallic forms. Digging around them reveals something genuinely unexpected, and this pattern continues without losing impact until the end." — English, 23.1 h, negative (a critic conceding the point)

### 5. Humor, charm and the dog
The dumb jokes (farts, burps, beer, peeing, a toilet-humor toggle) and Frodo the dog are a hit with a large share of reviewers, and the game's quirky identity is widely called endearing.

> "Yes you can pee in holes. No I won't explain why. Game just lets you. Peak game design honestly." — English, 0.5 h, positive
>
> "Let your dog get abducted at least once, its worth it when you get him back :P" — English, 5.7 h, positive
>
> "My 10 year old had an epic blast laughing at the burps and farts coming randomly from our character, giving endless laughs to the entire family." — English, 17.7 h, positive

### 6. Atmosphere, art and music
The low-poly post-apocalyptic look, lighting and rockabilly radio soundtrack are regularly praised; several reviewers call it a "dieselpunk" vibe that holds the game together.

> "Post-apocalyptic Nevada looks grim, absurd, and cozy at the same time." — Russian, 23.7 h, positive (translated)
>
> "Nice graphics and sound and one of the few soundtracks I didn't mute after an hour." — English, 21.8 h, positive
>
> "its got great graphics with consistent art direction unlike alot of indie asset flips you see now." — English, 5.7 h, positive

### 7. Responsive developers and free updates
Reviewers repeatedly note the developers shipped without Early Access, patched fast, and added substantial free content (including the Las Veganos city) rather than paid DLC — even when they disliked the update itself.

> "Game developers a fkn G and listens to the community, Dropped a patch quick and changed values on stuff that was just lacking hard." — English, 6.8 h, positive
>
> "the devs have recently added a bunch of extra content again - via a free update, not charging the player for DLC or microtransactions" — English, 35.8 h, positive
>
> "I appreciate the devs not putting the game in Early Access for several years like most people do today." — English, 1.3 h, positive

### 8. Value and "chill" appeal
At ~$10–13, most reviewers consider the 5–12 hours fair — though "wait for a sale" is common advice, and many positive reviews still land at 7/10. Some play it purely as a relaxing podcast game.

> "I can say for a fact that for the 10 dollars they are asking for the game, is a steal." — English, 13.3 h, positive
>
> "For the price of a Starbucks Venti drink, this is easily worth the money." — English, 13 h, positive
>
> "It's fun low-fi dig, chill, and kill zombies cycle… just be sure to keep on digging!" — English, 6.3 h, positive

---

## What reviewers criticize (the bad)

### 1. Stamina, beer and the constant trip back to the surface — the #1 complaint
Your character has stamina that drains fast while digging; the only ways to restore it are a fridge on the surface or occasional underground fridges. Combined with a small backpack and a slow-recharging jetpack, reviewers say they spend more time commuting than digging. Even some of the highest-voted positive reviews lead with this.

> "a very cool game with a very dumb mechanic. remove the beer drinking crap please. i want to dig, not stop digging every 30 secs to go to the fridge." — English, 10.6 h, positive, 27 upvotes
>
> "The stamina system is anti-fun, it exists only to disrupt the core gameplay loop." — English, 1.3 h, negative, 14 upvotes
>
> "The stamina system literally just halts progress in a way that does not respect the gamers time, only function is to drag out gameplay time." — English, 7.9 h, negative
>
> "You run out of stamina fast and have to constantly backtrack above ground (or to the nearest fridge) to refill your stamina. It also doesn't help that your backpack is also limited." — English, 4.7 h, negative, 5 upvotes
>
> "Will you let me dig or not?! … the UFO steals my dog, I have to go home. Monsters come, I have to defend. Backpack full again, stamina gone again, all of it means going home. Will you let me dig???" — Simplified Chinese, 1.6 h, negative (translated, condensed)

A Japanese reviewer's summary is typical: after a while the long back-and-forth to restore stamina becomes "here we go again" irritation.

### 2. Grind, slow pacing and weak late-game power
Upgrades across five tiers are gated behind large gold/diamond costs, and the whole game is built around farming resources. Reviewers complain the escalation never delivers a satisfying power spike: the top drill still digs a small radius, dynamite is capped at three sticks with no upgrades, and the last tiers feel like padding.

> "Tier 1: Excellent pacing and a high reward-to-time ratio… Tier 2: The experience becomes a 'grind.' Despite upgrades like the power shovel, the gameplay feels overly labour-intensive." — English, 2.8 h, negative, 23 upvotes
>
> "I got to the 'place where you beat the game' but then it told me I need to buy the expensive tier upgrade two times over to initiate the beat-the-game sequence. That would be at least 40 to 60 more trips to the bottom." — English, 3.1 h, negative, 24 upvotes
>
> "Even the top drill has a criminally small digging radius." — Russian, 10.9 h, positive-with-criticism (translated)
>
> "Dig value-1 trash with a broken shovel during the day, buy a 10-value upgrade; after upgrading the base, dig value-10 trash with a slightly better shovel and buy a 100-value upgrade. At night, shoot 20 monsters with turrets; after upgrading, shoot 40 monsters." — Simplified Chinese, 0.9 h, negative, 52 upvotes (translated, condensed)
>
> "Very addictive… but why not recommend? It can be finished in 5 hours — 2.5 if you don't care about details — and then you never want to play again. Addictive, but extremely low playability." — Simplified Chinese, 35.2 h, negative, 13 upvotes (translated)

### 3. Tower defense: weak AI, forced babysitting, and irreversible choices
Automatic turrets are widely called ineffective until late, so nights require manual attendance; but once upgraded they can trivialize the game. The main-gun branch choice is permanent, meaning you cannot try another turret without restarting the whole game — one of the most-upvoted complaints. Failing a base defense rolls you back to a save, and with no meta-progression, some reviewer call it a softlock risk.

> "I HATE THAT IN ORDER TO TRY NEW TURRET I HAVE TO START COMPLETELY OVER. I SHOULD BE ABLE TO JUST BUY AND SWAP." — English, 9.5 h, positive, 26 upvotes
>
> "Turret AI is frustrating; until mid-game you must keep killing zombies or the house gets destroyed." — Korean, 17.9 h, positive-with-criticism (translated)
>
> "Got softlocked due to not being able to beat the current wave of zombies… Wouldve refunded but was just outside the 2 hour Steam refund window." — English, 2.2 h, negative
>
> "There is no strategy since, if you pace yourself when uptiering, you can just hoard resources while the mutant hoards stay at the same difficulty." — English, 14.6 h, negative

### 4. Poor guidance, maze-like mines and missing quality of life
There is no map, the mine is a near-vertical shaft full of unbreakable obstacles, and quest steps (especially in the city) are vague. One save slot, settings that don't persist, no key rebinding and (despite the store listing) no cloud saves round out a common UX complaint cluster.

> "The main quest line… is not very clear, and players often feel lost about what to do next." — Simplified Chinese, 41.8 h, positive-with-criticism (translated)
>
> "The exit turret key is fixed as 'E' and drop weapon is fixed as 'G' and two more 'C' and 'V' - WHYYYY...." — left-handed player, on fixed keybinds — English, 12.1 h, positive-with-criticism
>
> "No cloud save wtf" — French, 8.6 h, negative
>
> "The game doesn't remember my setting for toilet humor and asks about it every restart." — English, 12.5 h, negative

### 5. Las Veganos and the 1.1 update — the divisive turning point
The free city update added a large quest area but, for many, replaced digging with an unclear, hostile FPS-lite: drones and snipers harass you, healing is scarce, quest items are hard to find, and the car drives poorly. The update also reworked progression in a way that invalidated existing saves and guides, with developers recommending a restart.

> "So I loved this game up until the las vegas portion. That part felt half baked and clunky. It suddenly went from a fun digging game to this awkward FPS that just isn't very fun." — English, 7 h, negative, 13 upvotes
>
> "The required trip to Las Veganos city is the game's weakest section… Players must complete repetitive quests… while contending with scarce ammunition, frequent robot spawns that drain resources, and rare healing stations." — English, 23.1 h, negative
>
> "The new update completely misses the point of the game… I have rarely been so bored, running around in a city just looking for stuff… and finding… money, money, money. booooooooring." — English, 18.4 h, negative
>
> "The 1.1 update… strongly modified progression, to the point that the developers strongly recommend starting a new game… after more than 20 hours and an almost-finished save, having to start from zero is quite frustrating." — French, 23.7 h, negative (translated)

### 6. The ending and the lack of an endgame
The game ends with a reveal that retroactively reframes everything as a joke, and then rolls credits with no New Game+, no boss, and a post-game shovel that (for most) has nothing left to do.

> "Ngl the ending was pretty disappointing… you grind up for a grind finale just to get scammed." — English, 5.1 h, negative, 8 upvotes
>
> "The ending feels like a joke, and a massive let down for all of the time spent on digging." — English, 27 h, negative (spoiler)
>
> "All that time digging? Pointless. All of the excited stuff you find on the way… Means nothing." — English, 27 h, negative (spoiler)
>
> "Getting a reward like that and not being able to actually use it was kind of a bummer." — English, 10.1 h, positive-with-criticism

### 7. Bugs, crashes and save loss
A broad technical cluster: fatal errors and crashes (especially on some Intel CPUs at launch), save files vanishing or corrupting, story softlocks (the President's message and bunker code), the "unstuck" button killing you in a loop, drones you can't exit, terrain clipping and X-ray vision from stacked dynamite, and achievements that stop counting.

> "This is a negative review because I lost whole save twice resulting in ~12 hrs of gameplay lost." — English, 12.5 h, negative
>
> "The game keeps crashing and throwing errors nonstop… after about 10 minutes, the game will crash with an error, and you will lose your progress." — Simplified Chinese, 9.6 h, negative
>
> "Got stuck on a ladder, gyrating up and down, so I used 'unstuck' (which kills you) and repeatedly died in a loop and had to alt+F4 after 3.5 hours." — English, 3.5 h, negative, 4 upvotes
>
> "Saves disappeared?! Saves disappeared?! Saves disappeared?!" — Simplified Chinese, 20.2 h, negative (translated)

### 8. Motion sickness, eye strain and performance
An unusually frequent complaint for a non-VR game: headaches, nausea, vertigo and eye strain, sometimes within 15–30 minutes, even from players who normally don't get motion sick. Drill speed is also tied to frame rate, and several reviewers report worsening FPS as they excavate more terrain or nearly max out their hardware on low settings.

> "I was having fun until it started making me nauseous… I have played 3D games for years and this is the first one that does this." — Simplified Chinese, 2 h, negative (translated)
>
> "it's also the only game that i have played in the last few years that gives me a headache, eye strain and dizzyness after an hour of play." — English, 5 h, negative
>
> "Drill speed changes with fps so you get high speed at 160fps but then gets really slow at 30-60 fps." — English, 10.3 h, negative

### 9. Achievements are hostile, grindy or bugged
Completionists are a vocal share of the reviewers, and they are unhappy: a 12-metre basketball shot with false "no cheating" detection, collect-every-pizza/cheese/hula-doll hunts, "clear all dirt" grinds, and achievements that simply never register. Several describe abandoning 100% plans — or the game — over them.

> "Terrible new achievements. I got it to 100% and had to restart to get the coil cannon one and they added new achievements to 100% clear the dirt? Don't waste your time on this game." — English, 11.3 h, negative, 4 upvotes
>
> "Every time I make a basket it says no cheating even though I did not jump or used the jetpack." — English, 22.8 h, negative
>
> "Hula and Cheese achievements are bugged… knowing I can't get 100% changes it from a good way to kill time to waste of time." — English, 26.5 h, negative

### 10. Forced parkour and horror sections
Mid-game bunkers contain unskippable set-pieces: laser parkour, a serial-killer chase room and button-mashing doors, several with instant death and long walks back. Reviewers who came for a chill digging game resent them, and a few were unpleasantly surprised by the horror content, which is not tagged.

> "you have to do some jump n run stuff, like dodging laser lines and jumping on poles, under time pressure… You cant evade those parts, since they are built into the main quests of the game." — English, 8.6 h, negative
>
> "i liked the game but hated retarded mandatory parkour with clanky controls and instadeath pits" — English, 6 h, negative
>
> "colour me shocked when I find that this game is a horror game in disguise… there's no mention or tag that this has a horror aspect to it." — English, 3.3 h, negative

### 11. Humor backlash
The toilet humor is a selling point for many and an active annoyance for others — especially the peeing mechanic, random fart/burp sounds, and the fact that the toggle does not remove everything (the opening scene and a jarring sound remain).

> "Absolutely pointless and cringeworhy ability to piss with the right mouse button. Now making me take the game even less seriously." — English, 14.6 h, negative
>
> "there is a toilet-humor option at first launch and no it is not a joke… personally I don't find it funny, but I'm forced to enable it for the soil-softening function." — French, 12.9 h, positive-with-criticism (translated)

### 12. Content and price debates
Reviewers who rush the critical path report finishing in ~5 hours; others sink 20–35 hours into full excavation and achievements. "Should have been Early Access", "wait for a sale" and "5 hours for $13" are common refrains in prose — but for every reviewer who says it's too expensive, another calls it a steal.

> "it's fun, you waste some time with it and it will be somewhat satisfying, but in the end you will come out of it a little bit underwhelmed." — English, 16.6 h, negative
>
> "This is not Early Access. Therefore I will review it for what it is right now: you get about 5 hours of fun for your $10… it does give major Early Access vibes, while it is not." — English, 5.6 h, negative
>
> "The game is devastatingly short and… once you're done, it's over." — English, 2.9 h, negative

---

## The ending and post-game (SPOILERS)

At the end of the story you destroy "Las Veganos" as part of a scripted sequence, then discover that the entire game was a **game show hosted by "The President"** — the treasure, the bunkers, the people you met underground, all staged. Reviewers split between finding it a funny meta-twist and feeling that it invalidates every hour spent digging. After the credits there is a post-game laser/auto-digging shovel (which many find has nothing left to use on), no New Game+ and no boss. Several reviewers explicitly ask for a boss mode or an endless mode; one demos that staying on the surface during the nuke changes nothing, breaking the urgency the finale builds.

> "The game ends with it revealing that the entire game was on a game show hosted by 'The President'. So that city you destroy at the end? For the LOLs. All that time digging? Pointless." — English, 27 h, negative (spoiler)
>
> "After finishing the game, just gotta say… 'I KNEW IT!'" — English, 5.4 h, positive (spoiler-adjacent)

---

## Divergent and mixed opinions

| Topic | For | Against |
|---|---|---|
| Stamina / beer system | Beer is funny; survival tension; some accept it early | "Anti-fun"; constant backtracking; biggest refund driver |
| Length | 10–30 h with collectibles and achievements; good value | 5–8 h critical path; "Early Access vibes" at full price |
| Tower defense | Manual turret play is satisfying; nice day/night contrast | AI turrets useless then overpowered; forced babysitting; no respec |
| Las Veganos city update | Free content; breaks up the loop; large new area | Unclear quests, no map, drones/snipers, car; "misses the point" |
| Humor / toilet jokes | Charming, streamable, family laughs | Cringe; toggle incomplete; undermines tone |
| Underground design | Best-in-class handcrafted secrets and set-pieces | Fixed layout (not procedural); no map; maze-like; forced parkour |
| Devs / updates | Fast patches, free content, community engagement | 1.1 broke saves/progression and split the community |
| Difficulty / balance | Easy to learn; hard mode for challenge | Wrong build can dead-end a save; snowballing or walled progression |
| Achievements | Fun goals for completionists | Grindy, buggy, and "no cheating" false positives |
| Cloning | Evolves the digging formula with defense and story | "Near-literal clone of A Game About Digging a Hole" |

---

## Who the reviews say should buy it

**Recommended for:** fans of Dome Keeper, A Game About Digging a Hole and mining/tower-defense hybrids; players who enjoy grind loops with a podcast on; easily amused by toilet humor; completionists with patience for buggy achievements.

**Not recommended for:** players prone to motion sickness or eye strain; anyone who wants a calm, no-pressure digging game (stamina, night attacks and parkour constantly interrupt); players who dislike unskippable action/parkour or horror set-pieces; and anyone who won't tolerate save loss, crashes and missing QoL. The most common closing advice is **wait for a sale** (many suggest 30–50% off) and check the current patch state first.

---

## Caveats

- This document summarizes player opinion, not a technical review. Most reported bugs were addressed in patches (the devs shipped ~8 updates in the first two weeks); some reviewers updated their reviews from negative to positive after fixes. Items like broken achievements and cloud saves were still being reported at the end of the review window.
- Steam review totals change over time; the sample is every review retrievable via the API on 14 September 2026 (1,859 of 1,860 counted by Steam).
- Quotes were lightly cleaned (line breaks, censored profanity, HTML/formatting tags) and translated from Chinese, Russian, Japanese, Korean, German, French, Spanish, Portuguese and Turkish where necessary. Attribution gives language, playtime, sentiment, and vote count for the highest-voted quotes.
- Keyword frequency counts are approximate and English-biased: the same review can touch several themes, and much of the most detailed criticism was written in Chinese and Russian, where keyword matching catches fewer mentions.
