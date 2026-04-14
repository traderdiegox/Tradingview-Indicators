# NWOG + ORG

**File:** `NWOG.pine`  
Pine Script v6 indicator for TradingView by [@traderdiegox](https://github.com/traderdiegox).

Plots the **New Week Opening Gap (NWOG)** and **Opening Range Gap (ORG)** — two key institutional reference zones used in ICT-based trading.

---

## Features

**New Week Opening Gap (NWOG)**
The gap between Friday's closing price and Sunday's opening price on futures markets. Plotted as a shaded box with an optional midpoint line (equilibrium). Previous NWOGs can be displayed and extended forward.

**Opening Range Gap (ORG)**
The gap between the previous day's close and the current day's open (or the regular session open). Plotted as a shaded box with an optional midpoint line. Previous ORGs can also be displayed.

Both zones include configurable colors, border styles, labels, and midpoint lines.

---

## How to Use in TradingView

1. Open TradingView and go to the **Pine Script Editor** (bottom panel).
2. Paste the contents of `NWOG.pine`.
3. Click **Add to chart**.
4. Open **Settings** to toggle NWOG and ORG zones independently.

**Recommended timeframes:** 1m – 1H on instruments with a Sunday futures open (ES, NQ, GC, etc.).

---

## License

Mozilla Public License 2.0 — Copyright (c) 2026 traderdiegox  
Portions derived from [cryptonnnite](https://www.tradingview.com/u/cryptonnnite/) (NWOG/NDOG), © cryptonnnite, MPL 2.0  
https://mozilla.org/MPL/2.0/
