# Key Intraday Levels

**File:** `KeyLevels.pine`  
Pine Script v6 indicator for TradingView by [@traderdiegox](https://github.com/traderdiegox).

Plots the key intraday price levels most relevant to ICT and SMC trading — session boxes, opening prices, previous day/week highs and lows — all in one clean overlay.

---

## Features

**Session Boxes**
Draws a highlighted range box for up to 5 configurable sessions: Asian Range, London, NY AM, Lunch Hour, and NY PM. Each session has its own color, time range, and border style. Boxes are hidden automatically on timeframes above 1H to avoid distortion.

After the daily session rolls at 6pm ET, boxes from the closed day are automatically hidden. The **Show Previous Sessions** setting controls how many prior trading days remain visible (0 = today only, 1 = today + yesterday, etc.).

**Key Liquidity Lines**
After each session closes, horizontal lines extend from the exact candle where the session High or Low was formed. Lines stay visible until price takes the level, then freeze in place — optionally extending a configurable number of candles past the taken bar before stopping. Each session (Asian, London, NY AM, Lunch, NY PM) has an individual visibility checkbox, plus a master toggle to hide all lines at once. Lines respect the same day-based visibility as session boxes.

Labels (*AS High*, *LO Low*, *AM High*, etc.) sit above High lines and below Low lines at all times. Label position (Left / Center / Right) controls which edge of the text aligns with the line — Left anchors the text start at x1, Right anchors the text end at the line tip, Center centers it. An optional *Show Price in Label* toggle appends the exact price to each label.

**Opens**
Marks the Midnight Open, 8:30 Open, and 9:30am Open with a vertical line and optional horizontal h-line extending forward. Each open has independent color, style, and width settings.

Opens are hidden after the daily session rolls at 6pm ET, controlled by the **Show Previous Opens** setting (same day-count logic as session boxes). Labels (*Midnight*, *8:30am*, *9:30am*) float above each open level with configurable position (Left / Center / Right), optional price display, and size. Label color matches the open's configured color.

**Daily & Weekly Levels**
Plots Previous Day High/Low (PDH/PDL) and Previous Week High/Low (PWH/PWL) as horizontal lines with labels. Lines start at the exact bar where the session extreme was formed. Lines auto-freeze after price takes them, with a configurable grace period extending the line a set number of candles past the take. Label position, price display, and size follow the same settings as Key Liquidity Lines.

---

## Settings Reference

### ⚙ General
| Setting | Description |
|---|---|
| Timezone | Chart timezone for session detection |
| Show Previous Sessions | Days of prior session boxes/lines to keep visible (0 = today only) |
| Show Previous Opens | Days of prior open lines/labels to keep visible |
| Box Border Style | Solid / Dashed / Dotted |
| Box Border Width | 1–4 px |
| H-Line Extension (bars) | How far forward untaken lines extend |

### 📊 Daily & Weekly Levels
Individual toggles, color, style, width, and custom label text for PDH, PDL, PWH, PWL. Shared settings for label visibility, show price, label position, and extend-after-taken.

### 📌 Opens
Individual toggles, color, style, width, and H-Line toggle for Midnight, 8:30, and 9:30am opens. Shared label settings: Open Labels toggle, Show Price, Label Position, Label Size.

### 🔑 Key Liquidity Boxes
Session enable/disable, color, and time range (start–end) for each of the 5 sessions. Box label settings (show, position, color, size).

### 📐 Key Liquidity Lines
Master toggle plus per-session checkboxes (Asian, London, NY AM, Lunch, NY PM). Line style, thickness, extend-after-taken candles, label position, show price, label size.

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
