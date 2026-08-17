# Pre-Market Trading Brief — Monday, August 17, 2026, 11:31 AM CDT

**Market status:** U.S. regular session underway. This is the pre-market workflow publication, generated after the open; the extended-hours snapshot below is therefore stale and must not be treated as a live quote feed.

**Agent: Codex**

**Source date:** 2026-08-17 (America/Chicago)

## Data Status

- **Sources used:** TradingView public U.S. scanner (latest completed regular session: Friday, August 14) for OHLC, percent change, volume, market capitalization, 10-day regular-session relative volume, float, and displayed extended-hours fields; AP’s Friday market recap; public economic and earnings calendars.
- **Primary screen:** NYSE/Nasdaq stocks with market cap at least $2B, prior-session gain at least 3%, and volume at least 500K. The close-location gate is exact: `(close-low)/(high-low) >= 0.80`. Dollar volume below is calculated from scanner close × volume.
- **Unavailable/stale:** live index futures, live premarket/regular-hours prints, premarket relative volume, Level II, advance/decline and up/down volume, authenticated TradingView charts, Claude Screeners, and live options chains/Greeks/spreads. Displayed extended-hours price/volume are a **pre-open snapshot and stale after the opening bell**. No live values are inferred.
- **Analysis limitation:** price-chart drawings, confirmed order-block boundaries, and intraday VWAP are unavailable; technical levels use reproducible Friday OHLC and rounded reference levels only. Verify price and volume at execution time.
- Informational/research support only; no trade placement or guarantee.

## Market Regime, News, Calendar, and Internals

**Regime: constructive but selective.** On Friday the S&P 500 fell 0.2% to 7,785.76, Nasdaq fell 0.3%, and the Dow fell 0.2%, after weak retail-sales data; the Russell 2000 gained 0.5%. The prior-session +3% screen nevertheless concentrated in semiconductors, AI infrastructure, optical networking, space, and crypto beta. That is an internally selective risk-on pocket, not broad confirmation.

**Overnight/current-futures status:** live futures and verified overnight headlines were unavailable at generation. Do not substitute Friday’s closing index move for current tape direction; use SPY/QQQ/IWM opening-range and VWAP behavior.

**Calendar (all times CT):** Monday’s Empire State Manufacturing and NAHB Housing Market Index were scheduled after the open. The week’s major risk events are Tuesday housing starts/permits, import prices and industrial production; Wednesday FOMC minutes; Thursday jobless claims and Philadelphia Fed; and Friday flash PMIs. Friday’s soft retail-sales reading remains the key recent growth/rates input.

**Internals:** exact breadth and volume internals are unavailable. The 28-name $2B/+3% scanner population is a breadth proxy only; require sector-ETF and index confirmation rather than treating it as intraday breadth.

## Prior-Session Primary Momentum Universe

These are liquid mid-, large-, and mega-cap names that satisfied the exact close-location gate. `CLV` is close-location within Friday’s daily range; rVol is Friday volume versus the 10-day regular-session baseline. Catalyst language is deliberately limited where independent validation was unavailable.

| Ticker | Company | Gain | CLV | Volume / dollar volume | rVol | Catalyst / context |
|---|---|---:|---:|---:|---:|---|
| MU | Micron Technology | +5.78% | 79.0% | 19.2M / $19.8B | 0.56x | AI-memory leadership; **fails** the exact 80% CLV gate, retained only as a liquid sector read |
| MRVL | Marvell Technology | +6.98% | 79.9% | 12.1M / $2.89B | 0.60x | AI-networking/semiconductor strength; **fails** 80% gate by a fraction |
| LUNR | Intuitive Machines | +8.78% | 97.0% | 11.7M / $243M | 0.93x | Space/contract momentum; tradable but higher-beta than mega-cap names |
| COHR | Coherent | +10.36% | 97.2% | 4.7M / $1.68B | 0.53x | Optical/AI-infrastructure leadership; independent same-day catalyst unavailable |
| AMAT | Applied Materials | +5.23% | 81.6% | 4.3M / $2.32B | 0.57x | Semiconductor-equipment strength; post-earnings reaction must be verified live |
| LITE | Lumentum | +6.92% | 87.0% | 2.9M / $2.91B | 0.52x | Optical networking/AI infrastructure strength |
| SMTC | Semtech | +9.70% | 92.3% | 1.6M / $254M | 0.83x | Connectivity/optical sympathy; relatively smaller liquidity profile |
| CIEN | Ciena | +6.32% | 93.4% | 1.1M / $505M | 0.52x | Optical-networking strength; no fresh company-specific catalyst verified |
| KEEL | Keel Infrastructure | +8.97% | 70.4% | 22.4M / $86M | 0.70x | Excluded from primary list: insufficient close-location and low-priced/high-float profile |
| SNDK | Sandisk | +9.15% | 71.7% | 11.4M / $20.4B | 0.74x | Memory leadership, but fails exact CLV gate; secondary sector confirmation only |

The strongest qualified institutional focus is **COHR, AMAT, LITE, and CIEN**. LUNR and SMTC qualify but have smaller dollar-volume footprints and higher execution volatility. MU/MRVL/SNDK are useful semiconductor leaders but are explicitly not promoted into the primary universe because their Friday closes were below the required top-20%-of-range threshold.

## Premarket Continuation / Gap Update

The table is a **stale displayed extended-hours snapshot** from the public scanner, not current market data. Premarket relative volume was unavailable; “rVol” remains Friday’s regular-session metric. Float is scanner-provided where available.

| Ticker | Displayed pre-open price | Gap vs. Friday close | Displayed pre-open volume | Friday rVol | Float | Read |
|---|---:|---:|---:|---:|---:|---|
| LUNR | $20.28 | -1.9% | 1.17M | 0.93x | 139.8M | Prior strength lacked displayed follow-through; avoid assuming continuation |
| COHR | $332.10 | -7.6% | 126.5K | 0.53x | 186.9M | Large negative indication versus a high-close day; needs opening reclaim before long bias |
| AMAT | $518.64 | -2.8% | 179.1K | 0.57x | 790.0M | Equipment divergence; event-risk / gap-fill watch |
| LITE | $948.09 | -4.3% | 71.8K | 0.52x | 75.9M | Strong Friday close but negative indication; do not chase without reclaim |
| SMTC | $142.31 | -7.6% | 10.7K | 0.83x | 92.7M | Thin displayed volume and large gap: avoid at the open |
| CIEN | $438.38 | -3.8% | 18.0K | 0.52x | 140.1M | Negative indication; wait for range recovery |

## Catalysts, Earnings, and Sector Strength

- **Memory/AI infrastructure:** public market coverage before Friday documented continued AI-memory strength in MU and SNDK. That supports the group context but does not override Friday’s failed exact close-location gate in those individual names.
- **AMAT:** its August 13 earnings timing was independently confirmed by public earnings calendars. Exact results and current reaction were not independently retrieved in this run; label the move **earnings-sensitive**, not a verified positive catalyst.
- **Optical networking:** COHR, LITE, SMTC, and CIEN appeared together in the qualified screen, which is the strongest objective sector-strength signal available. Company-specific Friday catalysts were not independently validated; price/volume, rather than a narrative, must lead.
- **Sector risk:** weak displayed extended-hours indications across COHR/AMAT/LITE/SMTC/CIEN create a gap-and-fade risk. A sector basket can be strong on Friday and still fail at Monday’s open.

## Current Momentum List

1. **LUNR — A watch:** highest-quality Friday close and near-1x rVol, but only after live reclaim/hold of Friday’s high.
2. **COHR — A-/B+ watch:** excellent Friday range close and $1.7B dollar volume; opening gap weakness means no blind continuation.
3. **AMAT — B+ watch:** liquid equipment bellwether; use it as a semiconductor confirmation name, not a chase after earnings.
4. **LITE / CIEN — B pullback-reclaim watches:** qualified high closes; each must reclaim Friday’s close with volume.
5. **SMTC — B-/avoid-until-confirmed:** attractive Friday close but lower dollar volume and adverse displayed gap.

## Technical Map, Support/Resistance, and Chase Risk

Levels are approximate and reproducible from Friday’s OHLC. A bullish order block or 0.500–0.618 retracement pocket is **not confirmed** without visible chart history; therefore no order-block claim is made.

| Ticker | Friday range / close | Support | Resistance / trigger | Gap-fill and chase risk |
|---|---|---|---|---|
| LUNR | $19.49–$20.72 / $20.68 | $20.25 open; $19.49 low | $20.72 high; then $21.00 | High: a break below $20.25 opens a test of the session low; do not chase a failed high break |
| COHR | $330.24–$360.43 / $359.58 | $333.52 open; $330.24 low | $360.43 high | High after a 10.4% day; a live reclaim of $359.58 is required before continuation |
| AMAT | $515.12–$538.00 / $533.73 | $518.00 open; $515.12 low | $538.00 high | Earnings gap risk; failed $518–$515 area invalidates long continuation |
| LITE | $927.00–$999.68 / $990.22 | $948.41 open; $927.00 low | $999.68 high; $1,000 round level | Wide daily range; take only a controlled reclaim, not a late extension |
| CIEN | $427.45–$458.00 / $455.88 | $438.38 open; $427.45 low | $458.00 high | High-close breakout can fail quickly if $438.38 is lost |

## Tiered Opportunities and Risk Plan

### Tier A — live confirmation required

**LUNR bullish continuation:** Trigger only on a live break and acceptance above $20.72 with sustained volume and sector/index confirmation. Entry idea: first orderly retest of $20.72 rather than an extended breakout candle. Invalidation: loss of $20.25 after the trigger. Targets: $21.00 then a measured extension only if it holds above the breakout. The $20.25-to-$20.72 range is narrow; do not force a trade if the opening spread/range makes the stop unrealistic.

**COHR reclaim:** Bias turns constructive only if price reclaims and holds Friday’s $359.58 close, then clears $360.43. Entry idea: reclaim/retest; invalidation: loss of the reclaim level. First target is only a new high/extension, so this is a continuation setup with material chase risk after +10.36%.

### Tier B — conditional sector leaders

**AMAT:** Bias neutral-to-bullish only above $533.73 and then $538.00 with semiconductor confirmation. Below $518/$515, stand aside; a negative earnings response can persist. **LITE and CIEN:** wait for each to reclaim its Friday close and retain VWAP after the opening range; their displayed negative indications make a gap-fill more likely than immediate pursuit.

### Options angle

Only consider options after the underlying trigger is confirmed. No current chain, premium, Greeks, open interest, or bid/ask spread was retrieved, so no contract is selected. For liquid names such as AMAT/COHR/LITE/CIEN, use regular-month expirations with enough time for the underlying thesis and reject wide spreads; shares or no trade are preferable to guessing at option liquidity.

### Avoid / do not chase

- **MU, MRVL, SNDK:** sector leaders but failed the required exact close-location gate; do not let headline strength rewrite the source-universe rule.
- **SMTC:** displayed -7.6% indication on thin pre-open volume; wait for a full live recovery.
- Any name opening far beyond Friday’s high without a VWAP/retest entry. A high close is not a standing buy signal.

## Final Trading Plan

Trade only confirmed strength. Start with **LUNR** for a $20.72 acceptance/retest and **COHR** for a $359.58/$360.43 reclaim sequence; use **AMAT** as the semiconductor decision barometer. If SPY/QQQ weaken, sector ETFs diverge, or candidates lose their opening-range/VWAP support, stand aside. Keep risk defined beyond the stated structural level, reduce size after a large prior-session expansion, and do not use stale extended-hours prices as execution inputs.

**Sources:** [AP Friday index recap](https://apnews.com/article/41b7cf2acc6562758183b1c5eae73635); [weekly economic calendar](https://www.kiplinger.com/investing/economy/this-weeks-economic-calendar); [weekly earnings calendar](https://www.kiplinger.com/investing/stocks/17494/next-week-earnings-calendar-stocks); TradingView public U.S. scanner snapshot captured August 17, 2026.
