# TradingView Stock Screener presets — Qullamaggie Breakout

Use these to cut the universe down before charting. The built-in Screener cannot
see consolidation shape or the breakout trigger — it only finds stocks that have
made the **momentum leg** and are **liquid and volatile enough**. Steps 2 and 3
of the setup still have to be confirmed on the chart with the Pine scanner.

Screener → **Stock Screener** (US, Common Stock) → set filters → save as a preset.

---

## Preset 1 — `QBO Daily` (primary)

Finds names that made the leg in the last 1–3 months and are still holding up.

| Filter | Value |
|---|---|
| Exchange | NYSE, NASDAQ, AMEX |
| Market cap | ≥ $300M |
| Average volume (30D) | ≥ 500,000 |
| Price | ≥ $5 |
| Performance % 3M **or** 1M | ≥ 30% |
| Price vs SMA(20) | Price above |
| Price vs EMA(10) | Price above |
| Volatility (D) | ≥ 3% |
| Perf % 1W | between −8% and +8% *(the pause)* |

That last row is what does the real work: it keeps names that ran hard over
1–3 months but went **quiet this week** — the volatility contraction the setup needs.

**Then** chart each survivor on 1D with the Pine scanner and keep only those
showing `READY` or `BO` on the dashboard.

---

## Preset 2 — `QBO Weekly` (position-trade horizon)

| Filter | Value |
|---|---|
| Exchange | NYSE, NASDAQ, AMEX |
| Market cap | ≥ $1B |
| Average volume (30D) | ≥ 1,000,000 |
| Price | ≥ $10 |
| Performance % 6M | ≥ 40% |
| Perf % 1M | between −10% and +10% |
| Price vs SMA(20) | Price above |
| Volatility (D) | ≥ 3% |

Chart survivors on **1W** with the scanner set to auto-adapt.

---

## Preset 3 — `QBO Monthly gate` (regime filter, not an entry scan)

Not a setup scan. Run it to answer one question: *is the long-term trend still
intact?* Anything that fails this is a lower-quality daily breakout.

| Filter | Value |
|---|---|
| Performance % 1Y | ≥ 0% |
| Price vs SMA(50) | Price above |
| Price vs SMA(200) | Price above |

The Pine scanner already applies this automatically as **Gate 2** when
`Use higher-timeframe trend gates` is on.

---

## Running it against your 61-name watchlist

The Screener presets scan the whole market. To check only your list, skip the
Screener and add the Pine scanner as a `Setup Ready` alert on each symbol —
that is a one-time setup and then it watches all 61 for you.

Realistically, most of your watchlist will fail the liquidity or ADR gate at any
given time. Names most likely to produce this setup: **NVDA, AMD, MU, PLTR,
RKLB, OKLO, SMR, NBIS, CRWV, APLD, HIMS, SOFI, CIFR, NNE**. The mega caps
(AAPL, MSFT, GOOGL) rarely clear a 3% ADR and will mostly screen out — that is
the filter working, not a bug.
