# Hyperliquid Whale Intelligence Tracker

Analyse smart money and rekt money positioning on Hyperliquid for: **$ARGUMENTS**

Run the following searches IN PARALLEL using WebSearch:

1. Search: "$ARGUMENTS Hyperliquid long short ratio top traders 2026"
2. Search: "$ARGUMENTS Hyperliquid funding rate June 2026"
3. Search: "$ARGUMENTS Hyperliquid liquidations open interest 2026"
4. Search: "coinglass $ARGUMENTS long short ratio top accounts"
5. Also attempt WebFetch on: https://www.coinglass.com/currencies/$ARGUMENTS/futures (extract long/short data if accessible)

---

## What to Look For

### Top Profitable Traders (Smart Money)
- On Hyperliquid, the "top traders" leaderboard shows accounts with highest cumulative PnL
- Are the majority of these accounts LONG or SHORT on $ARGUMENTS?
- Source: CoinGlass Hyperliquid long/short ratio, Coinalyze, or Hyperscreener

### Rekt Traders (Dumb Money / Contrarian Signal)
- Recently liquidated traders represent crowded, wrong-side positions
- If rekt traders were majority LONG → market was crowded long → bearish contrarian signal
- If rekt traders were majority SHORT → market was crowded short → bullish contrarian signal

### Funding Rate as Proxy
- Positive funding rate = longs are paying shorts = market is net long (bullish bias)
- Negative funding rate = shorts are paying longs = market is net short (bearish bias)
- For a SHORT entry: we WANT positive funding (longs paying us) or negative funding confirming bearish smart money

---

## Pass/Fail Logic

PASS if ANY of these are true:
- Top profitable traders are majority SHORT on $ARGUMENTS (>50% short by position count or volume)
- Recently liquidated/rekt traders were majority LONG (crowded long = contrarian short signal)
- Both signals align: smart money short + rekt money long simultaneously (STRONG signal)
- Funding rate is significantly positive (longs crowded, paying to stay long = squeeze risk for longs)

FAIL if:
- Smart money (top profitable traders) is majority LONG on $ARGUMENTS
- Funding rate is significantly negative and rekt traders were short (momentum is genuinely upward)

INCONCLUSIVE if:
- Data is unavailable or mixed signals (treat as neither pass nor fail — note clearly)

---

## Output Format

After researching, output EXACTLY this structure:

```
HYPERLIQUID WHALE TRACKER — [ASSET NAME] ([TICKER])

Top Traders Positioning: [MAJORITY LONG / MAJORITY SHORT / UNKNOWN]
Source: [where you found this data, or "unavailable"]

Rekt Traders Positioning: [MAJORITY LONG / MAJORITY SHORT / UNKNOWN]  
Source: [where you found this data, or "unavailable"]

Funding Rate: [positive X% / negative X% / unknown]
Interpretation: [what this means for positioning]

Smart Money Signal: [BEARISH / BULLISH / NEUTRAL / UNKNOWN]
Contrarian Signal:  [BEARISH / BULLISH / NEUTRAL / UNKNOWN]

FILTER 3 RESULT: PASS / FAIL / INCONCLUSIVE
Reason: [1-2 sentences explaining the decision]
```

If data is completely unavailable from all sources, output INCONCLUSIVE and explain what was attempted.
