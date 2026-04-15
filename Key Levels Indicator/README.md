# Key Intraday Levels

**File:** `KeyLevels.pine`  
Pine Script v6 indicator for TradingView by [@traderdiegox](https://github.com/traderdiegox).

Plots the key intraday price levels most relevant to ICT and SMC trading — session boxes, opening prices, previous day/week highs and lows — all in one clean overlay.

---

## Features

**Session Boxes**
Draws a highlighted range box for up to 5 configurable sessions: Asian Range, London, NY AM, Lunch Hour, and NY PM. Each session has its own color, time range, and border style. Boxes are hidden automatically on timeframes above 1H to avoid distortion.

**Key Liquidity Lines**
After each session closes, horizontal lines extend from the exact candle where the session High or Low was formed. Lines stay visible until price takes the level, then freeze in place — optionally extending a configurable number of candles past the taken bar before stopping. Each session (Asian, London, NY AM, Lunch, NY PM) has an individual visibility checkbox, plus a master toggle to hide all lines at once. Lines remain visible even when session boxes are hidden.

Labels (*AS High*, *LO Low*, *AM High*, etc.) sit above High lines and below Low lines at all times. Label position (Left / Center / Right) controls which edge of the text aligns with the line — Left anchors the text start at x1, Right anchors the text end at the line tip, Center centers it. An optional *Show Price in Label* toggle appends the exact price to each label.

**Opens**
Marks the Midnight Open, 8:30 Open, and CME 9:30 Open with a vertical line and optional horizontal h-line extending forward. Each open has independent color, style, and width settings.

**Daily & Weekly Levels**
Plots Previous Day High/Low (PDH/PDL) and Previous Week High/Low (PWH/PWL) as horizontal lines with labels. Labels are staggered (daily above, weekly below) to avoid overlap when levels coincide. Lines auto-hide after price takes them, with a configurable grace period.

---

## How to Use in TradingView

1. Open TradingView and go to the **Pine Script Editor** (bottom panel).
2. Paste the contents of `KeyLevels.pine`.
3. Click **Add to chart**.
4. Open **Settings** to configure sessions, colors, and behavior.

**Recommended timeframes:** 1m – 1H. Session boxes are automatically hidden on Daily/Weekly charts.

---

## License

MIT License — Copyright (c) 2026 traderdiegox  
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED.
