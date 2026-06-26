# Gates of Goonis — Game Notes & Mechanics

A "Gates of Olympus"-style tumble slot, reskinned as an inside joke. Play credits only — no real money.
Live: https://nicolailo50-cmyk.github.io/gates-of-goonis/

## Theme
- **Goonar** (the "victim", real friend Runar) is the Zeus figure — a "Fat Feast God" standing beside the board.
- Symbols are the group's drinks (premiums) and fast food (lows), because Goonar is called fat.

## Layout
- **6 reels × 5 rows** grid (30 cells).
- **Pay-anywhere**: a symbol pays if **8+** of the same kind appear anywhere (not on lines).
- **Tumble mechanic**: winning symbols explode, others fall down, new ones drop in, repeats until no win.

## Symbols & paytable (multiple of total bet)
Tiers: **8–9 / 10–11 / 12+** matching symbols.

| Symbol | Type | 8–9 | 10–11 | 12+ | At 10 kr bet (12+) |
|---|---|---|---|---|---|
| 🥃 Shot+Minttu | SCATTER | — | — | — | triggers free spins |
| Minttu | top | 1.0 | 2.5 | 5.0 | 500 kr |
| Fireball | high | 0.25 | 1.0 | 2.5 | 250 kr |
| Smirnoff Ice | high | 0.20 | 0.50 | 1.5 | 150 kr |
| Isbjørn Lite | high | 0.15 | 0.20 | 1.2 | 120 kr |
| Red Bull | high | 0.10 | 0.15 | 1.0 | 100 kr |
| Pizza | low | 0.08 | 0.12 | 0.8 | 80 kr |
| Hot dog | low | 0.05 | 0.10 | 0.5 | 50 kr |
| Fries | low | 0.04 | 0.09 | 0.4 | 40 kr |
| Burger | low | 0.025 | 0.075 | 0.2 | 20 kr |

## Multiplier orbs (football 🏈)
- Carry a value: **2,3,4,5,8,10,12,20,50,100×** (bigger = rarer).
- **Only apply on a winning tumble** (Gates rule) — orbs on a non-winning spin do nothing.
- **Base game**: orbs are rare; their values multiply that spin's win. Goonar shouts **"Fuck you Goonar!"** on a base-game multidrop.
- **Free spins**: orbs are common and bigger on average.

## Scatters
- **One scatter max per reel/column** (can't stack on the same reel).
- **4 scatters** = trigger free spins (Goonar says **"Free spins!"**).
- **3 scatters during free spins** = retrigger (+5 spins).
- **Anticipation**: once 3 scatters are showing, remaining reels crawl in slowly with a green glow.

## Free spins (bonus)
- **15 spins** awarded.
- **Global multiplier** accumulates from orbs and **persists** the whole feature.
- **Applied ONLY on spins that have a multidrop.** A winning spin with no orb pays at base (×1); the global stays parked and fires next time an orb lands.
- **Balance frozen** during the feature — all winnings shown in the FREE SPINS TOTAL WIN bar and paid out at the **COLLECT** screen.
- Intro "CLICK TO START" screen on every entry (bought or natural).

## Buy Free Spins
- Costs **100× base bet** (e.g. 1000 kr at 10 kr bet).
- Confirmation dialog → presentation spin that lands 4 scatters → click-to-start → 15 spins.

## Betting
- Base-bet denominations: **2, 4, 6, 8, 10, 12, 14, 16, 18, 20 kr** (default 10 kr).
- All values shown in **NOK (kr)**, Norwegian formatting.

## RTP (tuned via Monte Carlo simulation)
- **Base game ≈ 96.5%**
- **Bought bonus ≈ 98%**
- Free-spins trigger ≈ **1 in ~230 spins**.
- High-variance feature: individual sessions swing widely; the % is a long-run average.

## Presentation / UX
- **Big-win pay pages** with count-up: BIG WIN (≥20× bet), MEGA WIN (≥60×), GOOONIS WIN (≥120×).
- **Hit counter** under Goonar shows the last cascade's symbols + kr values.
- **Tumble counter** at top of board tallies the running win per spin.
- **Goonar glows + shakes** on multidrops, retriggers, big wins.
- **Procedural backing music** (Web Audio, looping) with a 🎵 toggle; **🔊 voice** toggle.
- Symbols fall in staggered/smoothly; **drinks rendered bigger/catchier, food smaller**.

## Voice lines
- **"Fuck you Goonar!"** — base-game multidrops only (not free spins).
- **"Free spins!"** — when the 4th scatter lands.
- Browser text-to-speech (natural pitch). For a truly human voice, a real recording of Goonar would need to be wired in.

## Tech / hosting
- Single self-contained `index.html` + `assets/` (PNG symbols sliced from AI art).
- Hosted free on **GitHub Pages**; everyone plays their own independent session (no shared state/backend).
- `sim.py` = Monte Carlo RTP simulator used to tune all weights/payouts.

## Mobile
- Dedicated iPhone layout: everything fits on one screen, no scrolling; board auto-scales, Goonar sized beside it.
