# Market Analysis Workflow Overview

## Complete Analysis Workflow

This document outlines the end-to-end workflow for comprehensive stock and market analysis.

```
┌─────────────────────────────────────────────────────────────────┐
│                   MARKET ANALYST WORKFLOW                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Phase 1: Stock Snapshot                                         │
│  └─→ Current price, quote, market cap                           │
│                                                                  │
│  Phase 2: Analyst Sentiment                                      │
│  └─→ Price targets, ratings, grades                             │
│                                                                  │
│  Phase 3: Historical Performance                                 │
│  └─→ Price trends, market cap history                           │
│                                                                  │
│  Phase 4: Sector & Industry Context                              │
│  └─→ P/E benchmarks, sector metrics                             │
│                                                                  │
│  Phase 5: Market Context                                         │
│  └─→ Index performance, industry moves                          │
│                                                                  │
│  Phase 6: Asset Class Context (Optional)                         │
│  └─→ Commodities, forex                                         │
│                                                                  │
│  Phase 7: Report Generation                                      │
│  └─→ Synthesize into actionable report                          │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

## Phase 1: Stock Snapshot

### Objective
Get current trading data and valuation snapshot.

### Skills Used
- `stock-quote` - Real-time price data
- `stock-price-change` - Multi-period returns
- `company-market-cap` - Current valuation

### Example Queries

```
Get real-time stock quote for the symbol AAPL
Get stock price change statistics for the symbol AAPL
Get market capitalization data for the symbol AAPL
```

### Expected Output
- Current price, change, volume
- Day range, 52-week range
- Moving averages (50-day, 200-day)
- Returns across all timeframes
- Market cap and size classification

### Key Analysis Points
- Price vs. moving averages (trend)
- Position in day range (momentum)
- Position in 52-week range (strength)
- Short-term vs. long-term returns (consistency)

### Time Estimate
~2 minutes

---

## Phase 2: Analyst Sentiment

### Objective
Understand Wall Street positioning and expectations.

### Skills Used
- `price-target-summary` - Target trends by timeframe
- `price-target-consensus` - Average, median, high, low
- `stock-grades` - Ratings and changes

### Example Queries

```
Retrieve the analysts' price-target summary for the stock symbol AAPL
Retrieve consensus price targets for the stock symbol AAPL
Get the latest stock grades for the symbol AAPL from top analysts
```

### Expected Output
- Price targets by period (month, quarter, year)
- Consensus, median, high, low targets
- Calculated upside/downside
- Recent upgrades/downgrades
- Rating distribution

### Key Analysis Points
- Target vs. current price (upside potential)
- Target trend (rising/falling)
- Range spread (consensus strength)
- Recent rating changes (momentum)

### Time Estimate
~2 minutes

---

## Phase 3: Historical Performance

### Objective
Analyze price and valuation trends over time.

### Skills Used
- `stock-performance` - Daily price data
- `historical-market-cap` - Market cap history

### Example Queries

```
Retrieve the daily closing prices for AAPL over the last 30 days
Retrieve historical market capitalization data for AAPL from 2024-01-01 to 2025-01-31
```

### Expected Output
- Daily closing prices
- Volume patterns
- Market cap peaks and troughs
- Trend identification

### Key Analysis Points
- Price trend direction
- Volume confirmation
- Market cap evolution
- Key support/resistance levels

### Time Estimate
~2 minutes

---

## Phase 4: Sector & Industry Context

### Objective
Benchmark against sector and industry peers.

### Skills Used
- `sector-pe-ratios` - Sector valuation
- `industry-pe-ratios` - Industry valuation
- `sector-performance-snapshot` - Sector metrics

### Example Queries

```
Retrieve the latest sector P/E ratios filtered by exchange NASDAQ and sector Technology
Retrieve the latest industry P/E ratios filtered by exchange NASDAQ and industry Consumer Electronics
Retrieve a snapshot of market sector performance filtered by exchange NASDAQ and sector Technology
```

### Expected Output
- Sector P/E ratio
- Industry P/E ratio
- Sector revenue, EBITDA, market cap
- Competitor landscape

### Key Analysis Points
- Company P/E vs. sector (premium/discount)
- Company P/E vs. industry (peer comparison)
- Sector health (growth, margins)
- Relative positioning

### Time Estimate
~3 minutes

---

## Phase 5: Market Context

### Objective
Understand broader market environment.

### Skills Used
- `stock-historical-index` - Index performance
- `industry-performance-snapshot` - Industry daily moves

### Example Queries

```
Retrieve full historical end-of-day price data for the ^GSPC index from 2025-01-01 to 2025-01-31
Retrieve a daily overview of industry performance filtered by exchange NASDAQ and industry Technology
```

### Expected Output
- S&P 500 / NASDAQ trends
- Major index moves
- Industry daily performance
- Market volatility context

### Key Analysis Points
- Stock vs. index performance (alpha)
- Market trend (risk-on/risk-off)
- Industry relative strength
- Sector rotation signals

### Time Estimate
~2 minutes

---

## Phase 6: Asset Class Context (Optional)

### Objective
Add commodity and currency context for macro-sensitive stocks.

### Skills Used
- `commodities-quote` - Commodity prices
- `commodities-list` - Commodity catalog
- `forex-list` - Currency pairs

### Example Queries

```
Retrieve the real-time price quote for GCUSD
Retrieve the full catalog of tradable commodities
Retrieve a full listing of actively traded currency pairs
```

### Expected Output
- Relevant commodity prices
- Currency pair rates
- Correlation context

### Key Analysis Points
- Commodity exposure (energy, metals)
- Currency sensitivity
- Macro correlations
- Risk factors

### Time Estimate
~2 minutes

---

## Phase 7: Report Generation

### Objective
Synthesize all findings into actionable intelligence.

### Skills Used
All previous skills synthesized

### Report Sections

1. **Stock Snapshot** - Current trading data
2. **Price Performance** - Returns and trends
3. **Analyst Sentiment** - Targets and ratings
4. **Valuation Context** - vs. sector/industry
5. **Market Context** - Broader environment
6. **Investment Implications** - Actionable conclusions

### Output Format
- 3,000-6,000 words
- Tables for data presentation
- Bold key metrics
- Clear section headers
- Source attribution

### Time Estimate
~10 minutes

---

## Total Workflow Time

| Phase | Time |
|-------|------|
| Phase 1: Stock Snapshot | 2 min |
| Phase 2: Analyst Sentiment | 2 min |
| Phase 3: Historical Performance | 2 min |
| Phase 4: Sector Context | 3 min |
| Phase 5: Market Context | 2 min |
| Phase 6: Asset Class (Optional) | 2 min |
| Phase 7: Report Generation | 10 min |
| **Total** | **~25 minutes** |

## Workflow Variations

### Quick Analysis (10 min)
- Phase 1: Stock Snapshot
- Phase 2: Analyst Sentiment (consensus only)
- Brief summary

### Standard Analysis (20 min)
- Phases 1-5
- Standard report

### Comprehensive Analysis (30+ min)
- All phases including Phase 6
- Full report with peer comparison
- Multiple stocks analyzed
