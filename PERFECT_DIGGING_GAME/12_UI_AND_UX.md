# 12 — UI and UX

> The missing-map problem is the single most repeated UX complaint in the corpora:
> `[MELT]` — "There's no map… you get very confused because all the corridors are identical" (a
> community hand-drawn map in the guides was the workaround); `[SPOT]` — "no map… players often feel
> lost". Menus also failed: `[KD]` "ESC doesn't close menus", `[SPOT]` "the game doesn't remember
> my setting", `[AGADH]` "no key binding settings, no graphics settings".
> UX is a feature here, with the same production weight as tools.

## 1. The Map (1.0 requirement)

One map, three zooms, zero excuses.

- **Full-screen map (M/Tab):** continuous surface + underground view; layer filter; pan/zoom with
  mouse or sticks; click to place markers.
- **Fog of war:** reveals with vision and scans, not globally.
- **Legend:** player tunnels (visited this session vs prior), ore veins (scanned), POIs, gates
  (locked/unlocked), checkpoints (activated/not), unvisited dead-end ticks, beacons, NPCs.
- **Dead-end audit:** every dead end gets a tick when physically visited; unticked dead ends are
  visible so completionists never wonder "have I checked this?" `[MELT]` "no ability to track 'have
  you checked this bloody passage'".
- **Route tools:** right-click waypoint → compass HUD arrow; auto-route along player tunnels
  (optional); distance + depth readout.
- **Trip overlays:** toggle ore heatmap (from scans), danger zones (if enabled), heat/cold bands.
- **Mini-map HUD (optional):** corner map with rotation lock and opacity; off by default.
- **Scan integration:** scanner pings write temporary icons; upgraded scanner writes permanent
  icons in a radius.
- **Marker typing:** colors + icons + short labels; survives reload; cloud-synced.

## 2. Quest and objective clarity

`[SPOT]`'s vague main quest ("not very clear… players often feel lost") is the failure case.

- **Objective line** always in HUD ("Open the glyph door: 2/3 fragments"), with a "show on map"
  action.
- **Quest cards** include: what, where (map link), why (one sentence), reward preview.
- **No missable-objective dead ends:** if the player lacks a required item, the quest card says
  where to find it (per-layer hint system, not a walkthrough).
- **Optional content clearly marked optional.**
- **A "story so far" recap** in the archive, spoiler-safe, one paragraph per layer.

## 3. HUD design rules

| Element | Rule |
|---|---|
| Trip Meter | One widget: battery, suit comfort, weight, distance-to-checkpoint (`07`) |
| Oxygen/heat/etc. | Contextual: only appears when relevant, then fades |
| Crosshair | Material + shape preview; colorblind-safe; scalable |
| Objectives | Top-left, collapsible, one line max |
| Damage/status | Peripheral, icon-based, no screen-flooding |
| Notifications | Queued, max 3 visible, never over the crosshair; severities |
| Photo mode | Pause-only, with FOV/dof controls; content toggle for streamers |

HUD scalability: 50–200% scale, safe-area sliders, per-element toggles, "Minimal" preset (crosshair
+ objectives only) and "Data-rich" preset.

## 4. Menus that don't fight back

Hard rules learned from the corpora:

1. **ESC closes the current menu**, always; ESC at root opens pause; ESC in pause resumes.
   `[KD]` "ESC button should close the menu".
2. **Back button (B/Circle/right-click)** does the same.
3. **Every setting persists immediately** and is confirmed on screen.
4. **No repeated nag popups.** Ask once, store the answer, expose it in settings (the `[SPOT]`
   toilet-humor prompt every launch is the anti-pattern).
5. **Tutorial prompts** are dismissible, reviewable, and disabled after first completion; a
   "Tutorials" menu page replays any of them.
6. **Search/sort/filter** in inventory, shop, museum, archive; controller-friendly as well as
   type-to-search.
7. **Compare and preview** everywhere: upgrade deltas (+25% radius), tool model preview, skin
   preview, blueprint ghost.
8. **Confirmations only for destructive actions** (sell museum item, reset save, abandon run) and
   they show what will be lost.
9. **Sell All** from the start, with a lock toggle for rare items. `[AGADH]` QoL complaints.
10. **Pause anywhere**, including in menus; timers stop in single-player.

## 5. Tutorial and onboarding

- **Learn by doing, not by wall of text.** First 5 minutes: dig 10 voxels (tooltip), find a coal
  seam (ping), sell (instant), buy tier 1 (visible change). `[AGADH]`'s immediate hook is the bar.
- Every mechanic is introduced in a safe context, then tested with a fair challenge; the handbook
  page unlocks alongside.
- **"I already know how to dig" skip** at first launch; a compact interactive refresher is
  available later for new systems (charges, modules, NG+).
- **The handbook** (F1/controller equivalent) is searchable, illustrated, and includes every
  mechanic and hazard with a screenshot and a short "what to do" line. `[KD]` "no proper tutorial"
  and `[SPOT]` "guidance" complaints are addressed here.

## 6. Shop / upgrade UX

- Tabs: Tools, Capacity, Traversal, Auxiliary, Modules, Cosmetics, Consumables.
- Each row: current state, next tier, **visible delta**, cost, "affordable" highlight, requirement
  if locked.
- **Undo/respec** button prominent and free (`06`).
- Locked-but-visible tiers with requirements ("Unlock at Layer 5") so there is always a next goal.
- Bulk-sell from any storage UI with price totals and rarity filters.
- A "what should I buy?" hint toggle for new players (suggests one sensible purchase, never nags).

## 7. Text, fonts and localization

- Fonts support Cyrillic, CJK, and all shipping locales from day 1; no baked text in textures.
- Subtitle and UI text controls (size, opacity, background) live in `13_SETTINGS.md`.
- All UI strings externalized; pseudolocalization test suite; RTL-ready layout (even if RTL ships
  later).

## 8. UX test checklist

- [ ] A new player reaches their first purchase in ≤ 5 minutes without external help.
- [ ] A returning player can find "where have I been and what did I miss" in ≤ 10 seconds.
- [ ] Every menu closes with ESC/B and never traps input.
- [ ] Settings changed in a session are identical next launch, on any machine (cloud).
- [ ] Controller-only playthrough completes with no mouse-only UI.
- [ ] No popup repeats after being answered.
- [ ] Map legibility passes a colorblind simulation audit.
