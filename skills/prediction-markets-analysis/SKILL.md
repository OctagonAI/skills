---
name: prediction-markets-analysis
description: Generate deep research reports on prediction market events using the Octagon Prediction Markets Agent. Combines real-time Kalshi market data with AI-driven analysis to surface price drivers, compare market vs. model probabilities, and identify potential mispricings across 120+ active markets.
---

# Prediction Markets Analysis

Generate comprehensive research reports on prediction market events using the Octagon Prediction Markets Agent. This skill combines real-time Kalshi market data with AI-driven analysis to identify mispricings, surface price drivers, and provide actionable trading insights.

## Prerequisites

Ensure Octagon MCP is configured in your AI agent (Cursor, Claude Desktop, Windsurf, etc.). See [references/mcp-setup.md](references/mcp-setup.md) for installation instructions.

**Note**: Report generation requires Octagon Plus, Pro, or Enterprise subscription (3 credits per report). Cached reports are free for all users.

## Core Functionality

The Prediction Markets Agent provides:

| Capability | Description |
|------------|-------------|
| Market vs. Model Probability | Computes independent model probability and compares against live market price |
| Event-Driven Research | Identifies key claims, catalysts, and decision-flipping events |
| Historical Resolution Tracking | Surfaces past resolution outcomes for context on base rates |
| Contract Snapshot | Returns live bid/ask spreads, last traded price, volume, and open interest |
| Cross-Category Coverage | 120+ active markets across Politics, Economics, Crypto, Sports, Entertainment, Science & Tech, Climate |

## Model Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `octagon-prediction-markets-agent` | Default. Returns cached report if available, otherwise generates new | General use |
| `octagon-prediction-markets-agent:cache` | Always retrieves cached report | Fastest response, may not be latest |
| `octagon-prediction-markets-agent:refresh` | Always generates fresh report | Most up-to-date, takes several minutes |

## Example Queries

### Federal Reserve Policy
```
Analyze this Fed decision prediction market: https://kalshi.com/markets/kxfeddecision/fed-meeting/kxfeddecision-26jun
```

### Cryptocurrency Price Range
```
Research this Bitcoin price prediction market: https://kalshi.com/markets/kxbtcminy/how-low-will-bitcoin-fall-this-year/kxbtcminy-27jan01
```

### Sports Matchup
```
Analyze this NHL playoff prediction market: https://kalshi.com/markets/kxnhleast/eastern-conference-championship/kxnhleast-26
```

### Entertainment Awards
```
Research this Grammy nomination market: https://kalshi.com/markets/kxgrammynomsoty/grammy-nominees-for-song-of-the-year/kxgrammynomsoty-69
```

### IPO Timing
```
Analyze when SpaceX will IPO: https://kalshi.com/markets/kxipospacex/when-will-spacex-ipo/kxipospacex
```

### Force Fresh Report
```
Generate a fresh report (bypass cache) for: https://kalshi.com/markets/kxbtcminy/how-low-will-bitcoin-fall-this-year/kxbtcminy-27jan01
```

## Example Response Structure

```markdown
## Market Overview
- **Event**: Fed Decision June 2026
- **Resolution Date**: June 18, 2026
- **Current Market Price**: 72% (Hold rates)
- **Model Probability**: 68%
- **Mispricing Signal**: Market slightly overpriced

## Price Drivers
1. **Recent Economic Data**: CPI trending lower, supporting rate hold
2. **Fed Communications**: Dovish tone in recent FOMC minutes
3. **Labor Market**: Unemployment stable at 4.1%

## Key Catalysts
| Date | Event | Potential Impact |
|------|-------|------------------|
| June 10 | CPI Release | High - could shift probabilities 5-10% |
| June 12 | FOMC Statement | Medium - language on future path |

## Historical Resolution Context
- Last 6 meetings: 4 holds, 2 cuts
- Model accuracy on this series: 78%

## Contract Details
| Outcome | Bid | Ask | Last | Volume | OI |
|---------|-----|-----|------|--------|-----|
| Hold | 0.71 | 0.73 | 0.72 | 15,234 | 89,000 |
| Cut 25bp | 0.18 | 0.20 | 0.19 | 8,456 | 45,000 |
| Hike | 0.08 | 0.10 | 0.09 | 2,100 | 12,000 |

## Recommendation
**Slight Sell** on Hold contract. Model sees 4% overpricing. Consider waiting for CPI data before positioning.
```

## Market Categories

The agent covers 120+ active markets across:

| Category | Example Markets |
|----------|-----------------|
| **Politics** | Elections, legislation, executive actions |
| **Economics** | Fed decisions, inflation, employment data |
| **Crypto** | Bitcoin/Ethereum price ranges, ETF approvals |
| **Sports** | Championship outcomes, playoff matchups |
| **Entertainment** | Awards shows, box office, streaming |
| **Science & Tech** | Space launches, AI milestones, IPO timing |
| **Climate** | Temperature records, hurricane landfalls |

## Use Cases

### Identify Mispricings
Compare crowd consensus against model-derived probability to find trading opportunities.

### Pre-Trade Research
Research key drivers behind a prediction market price before placing a trade.

### Catalyst Monitoring
Monitor upcoming events that could move contract prices.

### Event Analysis
Get structured, sourced research on fast-moving events in politics, finance, and beyond.

## Historical Data Access

Use the `prediction_markets_history` tool to fetch historical data:

```
Fetch historical data for prediction market ticker KXFEDDECISION-26JUN from January to June 2026
```

Parameters:
- `ticker`: Market ticker symbol
- `captured_from`: Start date filter
- `captured_to`: End date filter
- `limit`: Number of records
- `cursor`: Pagination cursor

## Integration with Other Skills

Combine with other Octagon skills for comprehensive analysis:

| Skill | Integration Use |
|-------|-----------------|
| `earnings-call-analysis` | Analyze CEO comments relevant to prediction market events |
| `sec-8k-analysis` | Track material events that could impact market outcomes |
| `stock-performance` | Correlate stock moves with prediction market probabilities |

## Analysis Tips

1. **Check model vs. market spread**: Larger spreads suggest potential mispricings

2. **Monitor catalyst calendar**: Know when decision-flipping events are scheduled

3. **Review resolution history**: Past accuracy provides context for current probabilities

4. **Consider liquidity**: Check volume and open interest before sizing positions

5. **Use cache wisely**: Use `:cache` for quick checks, `:refresh` before trading

6. **Cross-reference sources**: Combine prediction market analysis with fundamental research

## Supported Platforms

- **Kalshi**: Full support for all active markets
- **Polymarket**: Coming soon

## For More Markets

Browse the full list of supported markets at [octagonai.co/markets](https://octagonai.co/markets).
