# Interpreting Commodities Quote Results

## Reading the Output

The octagon-agent returns comprehensive commodity quote data:

| Metric | Value |
|--------|-------|
| Current Price | $4,864.20 |
| Change | +$211.60 (+4.55%) |
| Day Low | $4,690.20 |
| Day High | $4,871.00 |
| 50-Day Avg | $4,559.45 |
| 200-Day Avg | $3,888.90 |
| Year Low | $2,837.40 |
| Year High | $5,626.80 |
| Trading Volume | 18,846 |
| Previous Close | $4,652.60 |

## Understanding Each Metric

### Current Price

| Aspect | Description |
|--------|-------------|
| What it is | Last traded price |
| Timing | Real-time or slight delay |
| Unit | USD per unit (oz, barrel, etc.) |

### Change

| Aspect | Description |
|--------|-------------|
| Dollar change | Absolute move from prior close |
| Percent change | Relative move |
| Context | Typical daily range varies |

### Day Range

| Field | Meaning |
|-------|---------|
| Day Low | Lowest price today |
| Day High | Highest price today |
| Range | High - Low (volatility) |

### Moving Averages

| Average | Meaning |
|---------|---------|
| 50-Day | Short-term trend |
| 200-Day | Long-term trend |
| Relationship | Trend direction |

### Year Range

| Field | Meaning |
|-------|---------|
| Year Low | 52-week low |
| Year High | 52-week high |
| Position | Where in range |

### Volume

| Aspect | Meaning |
|--------|---------|
| Value | Contracts/units traded |
| Context | vs. average volume |
| Signal | Participation level |

## Analyzing Price Movements

### Daily Change Context

| Change % | For Commodities |
|----------|-----------------|
| >5% | Very large move |
| 2-5% | Significant move |
| 1-2% | Moderate move |
| <1% | Normal fluctuation |

### Example Analysis

From GCUSD data:
- Change: +$211.60 (+4.55%)
- **Interpretation**: Significant positive move for gold

## Day Range Analysis

### Calculating Position

```
Position = (Current - Day Low) / (Day High - Day Low) × 100%
```

### Example

- Current: $4,864.20
- Day Low: $4,690.20
- Day High: $4,871.00
- Position: 96.2%

### Position Interpretation

| Position | Meaning |
|----------|---------|
| >80% | Near day high (strong) |
| 50-80% | Upper half |
| 20-50% | Lower half |
| <20% | Near day low (weak) |

## 52-Week Range Analysis

### Calculating Position

```
Position = (Current - Year Low) / (Year High - Year Low) × 100%
```

### Example

- Current: $4,864.20
- Year Low: $2,837.40
- Year High: $5,626.80
- Position: 72.6%

### Position Interpretation

| Position | Meaning |
|----------|---------|
| >90% | Near 52-week high |
| 70-90% | Upper range |
| 30-70% | Mid-range |
| 10-30% | Lower range |
| <10% | Near 52-week low |

## Moving Average Analysis

### Trend Identification

| Pattern | Meaning |
|---------|---------|
| Price > 50-Day > 200-Day | Strong uptrend |
| Price > 200-Day > 50-Day | Recovery |
| 50-Day > Price > 200-Day | Pullback in uptrend |
| 200-Day > Price > 50-Day | Bounce in downtrend |
| 200-Day > 50-Day > Price | Strong downtrend |

### Example

From GCUSD data:
- Price: $4,864.20
- 50-Day: $4,559.45
- 200-Day: $3,888.90

Order: Price > 50-Day > 200-Day = **Strong uptrend**

### Distance from Averages

| Calculate | Formula |
|-----------|---------|
| vs. 50-Day | (Price - 50-Day) / 50-Day |
| vs. 200-Day | (Price - 200-Day) / 200-Day |

### Example

- vs. 50-Day: (4,864.20 - 4,559.45) / 4,559.45 = +6.7%
- vs. 200-Day: (4,864.20 - 3,888.90) / 3,888.90 = +25.1%

## Volume Analysis

### Volume Context

| Level | Interpretation |
|-------|----------------|
| 2x+ average | Exceptional interest |
| 1.5x average | Above normal |
| 1x average | Normal |
| 0.5x average | Low interest |

### Volume-Price Signals

| Combination | Signal |
|-------------|--------|
| Price up + high volume | Strong buying conviction |
| Price up + low volume | Weak rally |
| Price down + high volume | Strong selling |
| Price down + low volume | Lack of sellers |

## Commodity-Specific Insights

### Gold (GCUSD)

| Factor | Current Implication |
|--------|---------------------|
| +4.55% day | Large move, likely catalyst |
| Near day high | Strong buying |
| Above 200-day | Long-term uptrend |
| Upper 52-week | Near highs |

### Key Gold Drivers

| Driver | Direction |
|--------|-----------|
| Dollar weakness | Bullish for gold |
| Lower rates | Bullish for gold |
| Inflation fears | Bullish for gold |
| Risk-off sentiment | Bullish for gold |

## Comparing to Prior Close

### Gap Analysis

| If Open vs. Prior Close | Signal |
|-------------------------|--------|
| Gap up | Bullish overnight |
| Gap down | Bearish overnight |
| Near prior close | Neutral open |

### From GCUSD

- Prior Close: $4,652.60
- Current: $4,864.20
- Move: +$211.60

## Red Flags

### Warning Signs

1. **Extreme move** (>10%) - Verify data, check news
2. **Very low volume** - Less reliable quote
3. **Large gap from averages** - Mean reversion risk
4. **At year extremes** - Support/resistance

### Data Quality

| Check | Why |
|-------|-----|
| Timestamp | Data freshness |
| Volume | Market activity |
| Bid-ask | Liquidity |

## Practical Application

### Trading Signals

| Finding | Implication |
|---------|-------------|
| Above both MAs + high volume | Bullish continuation |
| Below both MAs + high volume | Bearish continuation |
| Near year high | Potential resistance |
| Near year low | Potential support |

### Position Management

| Context | Approach |
|---------|----------|
| Strong trend | Follow momentum |
| Extended from MA | Consider profit-taking |
| At extremes | Watch for reversal |

## Next Steps After Analysis

### Follow-Up Research

| Finding | Action |
|---------|--------|
| Big move | Research catalyst |
| Trend change | Verify with fundamentals |
| Volume spike | Check for news |
| At resistance/support | Monitor price action |

### Related Skills

| Skill | Purpose |
|-------|---------|
| commodities-list | Market context |
| stock-historical-index | Broader market |
| sector-performance-snapshot | Energy sector |
| stock-price-change | Compare to equities |
