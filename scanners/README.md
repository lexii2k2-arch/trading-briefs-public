# Scanners

Pine Script scanners and TradingView Screener presets.

| Scanner | Source | Primary TF | File |
|---|---|---|---|
| Qullamaggie Breakout | YouTube: *I Tested The Qullamaggie Breakout on Top 100 Gainers — Here's What Happened* (`chCg-Q_lOfY`) | Daily | [`qullamaggie-breakout-scanner.pine`](qullamaggie-breakout-scanner.pine) |

---

## Qullamaggie Breakout Scanner

### What the setup is

Three things in sequence:

1. **Momentum leg** — the stock has already made a big move (30%+ over roughly 1–3 months). The scanner requires the leg *low* to occur before the leg *high*, so it rejects V-shaped recoveries that merely look like an advance.
2. **Consolidation** — price then pauses in a tight, shallow range that holds near the highs and sits on rising short-term moving averages. Volatility contracts.
3. **Breakout** — price clears the top of that range on a volume surge. That is the entry.

The scanner scores every setup **0–10** and flags the best ones as **5★**.

### Which timeframe — and why not monthly

You asked for daily, weekly and monthly. Here is the honest split:

| TF | Role | Verdict |
|---|---|---|
| **Daily** | **Primary — the timeframe the setup is defined on.** A 2–8 week base is 10–40 daily bars, which is where consolidations are actually readable. | **Use this to scan.** |
| **Weekly** | Slower variant for position-trade horizons, *and* a trend gate for the daily scan. Real but rarer — a weekly base means several months of chop. | Secondary. |
| **Monthly** | A 2–8 week consolidation does not exist in monthly bars — it is 0.5–2 bars. Monthly cannot express this setup. | **Use as a long-term trend gate only, not for entries.** |

So the script runs on all three, but the intended workflow is: **scan Daily → weekly and monthly act as trend gates → drop to 1H/15M for entry timing** (which is how you already trade).

Turn `Auto-adapt parameters to chart timeframe` on and the presets switch automatically:

| Parameter | Daily | Weekly | Monthly |
|---|---:|---:|---:|
| Leg lookback | 60 bars | 13 bars | 6 bars |
| Min leg gain | 30% | 40% | 60% |
| Consolidation length | 10 bars | 4 bars | 3 bars |
| Max consolidation depth | 15% | 20% | 25% |

### Install

1. TradingView → **Pine Editor** → paste the contents of `qullamaggie-breakout-scanner.pine` → **Add to chart**.
2. Set the chart to **1D**.
3. Leave `Use confirmed HTF bars only (no repaint)` **on** — the weekly/monthly gates then read the last *closed* higher-timeframe bar, so signals never repaint on you mid-week.

### Scanning your watchlist

Pine indicators evaluate one symbol at a time, so run it two ways:

**A — Alerts across the watchlist.** Right-click chart → **Add alert** → Condition: `QBO Scan` → pick `Setup Ready`, `Breakout`, or `5-Star Breakout` → *Once per bar close*. Repeat per symbol, or apply to a watchlist-wide alert if your plan supports it. `Setup Ready` is the useful one — it fires while the stock is still coiled under the trigger, before the move.

**B — Pre-filter with the built-in Screener** to cut the universe down first, then chart the survivors. Presets are in [`qullamaggie-screener-filters.md`](qullamaggie-screener-filters.md).

### Webhook / bot output

Set the alert condition to **Any `alert()` function call** and every confirmed breakout emits JSON:

```json
{"strategy":"qullamaggie_breakout","ticker":"NVDA","tf":"1D","action":"buy","rating":9,
 "entry":184.20,"stop":178.55,"target_2r":195.50,"target_3r":201.15,
 "shares":44,"adr_pct":4.12,"vol_x":2.31}
```

That drops straight into the webhook bot in your build spec (`C:\Users\Kenny\Claude.Builds\trading_bot`) without reshaping.

### Risk handling built in

- **Stop** — consolidation low, breakout-bar low, or 1× ADR (your choice), and **capped at 1× ADR** by default. That is Qullamaggie's own rule: never risk more than one average daily range.
- **Size** — computed from your equity and risk-per-trade %. Shown on the dashboard and in the breakout label.
- **Targets** — 2R and 3R plotted. This clears your 1:2 minimum R:R rule automatically.
- **Exit management** — Qullamaggie rides the 10-day MA (fast movers) or 20-day MA (slower). Both are plotted; the trailing exit is discretionary, not automated by this script.

### How it fits your existing stack

This is a **new setup type for you** — everything in your current suite (VWAP Band Pullback, EMA Tri-Band, MACD-V reversals, NR4/NR7) is intraday-to-swing on 1H/4H/15M. This is a *daily* momentum-continuation scan. It finds candidates; your existing tools time the entry:

- **PAC / BOS** — a BOS in the breakout direction on the 1H confirms the daily break is real.
- **Vol Spectrum Pro** — require ≥60% buy-side pressure on the breakout bar, same as your NR4/NR7 rule.
- **VWAP Institutional PRO** — after the daily breakout, a pullback to the Rolling VWAP band on 15M is a lower-risk entry than chasing the daily close.

Your standing rules still apply and are **not** enforced by the script: max 2 open positions, no entries in the first 15 minutes of the NY open, stop for the day after 2 consecutive losses.

### Settings worth tuning

| Input | Default | Note |
|---|---|---|
| Min ADR % | 3.0 | Raise to 4–5 to bias toward faster movers. Most of your small caps clear this easily; AAPL/MSFT/GOOGL often will not. |
| Min avg $ volume | 10M | Your liquidity floor. Lower it to ~2M if you want ONDS/AREC/TMQ-type names to qualify. |
| Max consolidation depth | 15% | Tighter (10%) = fewer, higher-quality bases. |
| Breakout volume surge | 1.5× | Matches the 1.5× threshold you already use elsewhere. |
| Minimum rating to signal | 0 (off) | Set to 7–8 if the scan returns too much. |
| Episodic pivots | off | Qullamaggie's companion setup (10%+ gap on 3×+ volume). Separate trade type — turn on deliberately. |

---

**Not trading advice.** These are research tools. Nothing here places trades or guarantees results.
