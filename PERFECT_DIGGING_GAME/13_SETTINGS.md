# 13 — Settings

> `[AGADH]`: "No key binding settings. No graphics settings. No cloud saves." `[MELT]`: "no settings
> to reduce motion sickness" / "no way to disable motion blur". `[OMT]`: no FOV slider. `[KD]`:
> settings reset every session. This game ships **every option below at 1.0**, all persisted and
> cloud-synced. Settings are not polish; they are the difference between a purchase and a refund.

## 1. Display

| Setting | Options / range | Default |
|---|---|---|
| Resolution | list + borderless/windowed/fullscreen | Native, borderless |
| VSync | Off / On / Adaptive | On |
| Frame cap | 30 / 60 / 90 / 120 / 144 / unlimited | 120 (uncapped option) |
| Dynamic resolution / upscaling | Off / FSR / DLSS / XeSS / TAAU + quality | On (FSR Balanced if supported) |
| FOV | 60–110°, with horizontal/vertical unit toggle | 90° |
| Brightness | slider + calibration screen | Calibrated default |
| Gamma | slider | 2.2 |
| HDR | Off/On + calibration (if display supports) | Off |

## 2. Graphics

| Setting | Options | Default |
|---|---|---|
| Preset | Low / Medium / High / Ultra / Custom | Auto-detect → High |
| Shadows | Off / Low / Med / High | High |
| View distance (surface + underground) | sliders separately | High |
| Foliage / clutter density | slider | High |
| Voxel mesh quality | Low/High | High |
| Particles | slider | High |
| Water reflections | Off/Low/High | Low |
| Lighting / AO | Off/On/High | High |
| Bloom | Off / Low / High | Low |
| Motion blur | **Off** / Low / High | Off |
| Depth of field | Off / On | Off |
| Film grain | Off / On | Off |
| Chromatic aberration | Off / On | Off |
| Camera shake | 0–100% | 40% |
| Head bob | 0–100% | 30% |
| Vignette / "tunnel vision" effect | Off / Subtle / On | Subtle |
| FSR frame generation | Off/On | Off |
| Resolution scale | 50–200% | 100% |

**Rule:** every post-process effect defaults to its comfort-safe value, and none can be re-enabled
by an update. `[MELT]` forced bloom / `[KD]` forced blur are anti-patterns.

## 3. Audio

| Setting | Options | Default |
|---|---|---|
| Master / Music / Ambience / SFX / UI | 0–100% each | 80% |
| Dynamic range | Full / Night / Headphones | Full |
| Mono audio | Off/On | Off (but available) |
| Subtitles | Off / Dialogue / All sounds | All sounds |
| Subtitle size / background / speaker labels | zoom + styles | 100%, translucent |
| Digging loop volume | independent (some players mute it) | 100% |
| Mute on focus loss | Off/On | Off |

## 4. Gameplay

| Setting | Options | Default |
|---|---|---|
| Mode | Cozy / Standard / Challenge / Creative | Cozy (recommended at first launch) |
| Creatures | Off / Ambient / Light / Active | Ambient |
| Horror intensity | Off / Spooky / Full | Off |
| Environmental hazards | Cosmetic / Soft / Damaging / Deadly | Soft |
| Fall damage | Off / Forgiving / Classic | Forgiving (Cozy: Off) |
| Battery & suit pressure | Off / Soft / Standard | Soft |
| Weight system | Off / Soft / Standard | Soft |
| Auto-dig assist | Off/On | On if hold-to-dig enabled |
| Clean Cut dig assist | Off/On | On |
| Auto-pickup radius boost | Off/On | On |
| Quest markers | Off / Minimal / Full | Full |
| Map fog of war | Off/On | On |
| Tutorial prompts | Full / Minimal / Off | Full |
| Handbook hints | On/Off | On |
| Pause when window loses focus | On/Off | On |
| Confirm destructive actions | Always / Default | Default |
| Photo mode | On/Off | On |
| Toilet humor / slapstick sounds | On/Off (independent of content) | Off |
| Flashing effects | Normal / Reduced / Off | Reduced if photosensitivity risk detected on first launch |

## 5. Controls

Everything from `11_CONTROLS_AND_INPUT.md`: full rebinding per device, sensitivity, invert, toggle
vs hold, deadzones/curves, vibration strength, gyro, glyph style, left-handed preset, one-hand
presets, profiles (save/load/export), reset.

## 6. Accessibility

Full list in `14_ACCESSIBILITY.md`, surfaced in the same Settings menu under an "Accessibility" tab:
UI scale, font scale, colorblind modes, screen reader, text-to-speech, timing assists, aim/placement
assists, reduced motion preset, photosensitivity mode, content toggles, one-hand mode, hold-to-dig
toggle, auto-walk, subtitle options, high-contrast modes.

## 7. Language and region

- Text language and subtitle language can differ.
- Number/keyboard layouts: AZERTY/QWERTZ detection; metric/imperial depth units (meters default,
  feet option).
- Regional pricing and per-locale release of content updates.

## 8. Data and saves

| Setting | Options | Default |
|---|---|---|
| Autosave interval | 1/5/10 min + on major events | 5 min + milestones |
| Save slots | 5 manual + autosave ring (≥ 10) | — |
| Steam Cloud | On/Off | On |
| Cloud conflict behavior | Ask / Keep newest / Keep local / Keep cloud | Ask |
| Export/import save | file-based, versioned | Available |
| Reset progress | per-slot, with warning + typed confirmation | — |
| Save format version | shown for support | — |

## 9. Settings behavior requirements

1. **Persist immediately and survive crashes, updates and machine changes** (Cloud). `[KD]`
   "settings don't persist" is a named anti-pattern.
2. **Per-save vs global separation:** gameplay difficulty is per-save; display/audio/controls are
   global. Changing either is explained in the UI.
3. **Settings search** (type "blur") and a "Reset to defaults" per tab.
4. **Profile presets:** Performance / Balanced / Quality / Comfort (accessibility-oriented).
5. **First-launch setup wizard:** detects hardware, asks about motion sensitivity, offers Comfort
   preset, shows mode/horror consent screen with clear language.
6. **Any change applies live where possible** with before/after preview (FOV, brightness).
