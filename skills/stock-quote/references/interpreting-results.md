# Interpreting Stock Quote Results

## Reading the Output

The octagon-agent returns a comprehensive quote with multiple data points:

| Metric | Example |
|--------|---------|
| Current Price | $270.01 |
| Change | +$10.53 (+4.06%) |
| Volume | 72,890,096 |
| Day Range | $259.21 - $270.48 |
| 52-Week Range | $169.21 - $288.62 |
| Market Cap | $3.97T |
| 50-Day MA | $268.30 |
| 200-Day MA | $236.65 |

## Understanding Price Changes

### Daily Change

| Change Type | Interpretation |
|-------------|----------------|
| Large positive (>3%) | Strong buying, possible catalyst |
| Small positive (0-1%) | Normal fluctuation |
| Small negative (0-1%) | Normal fluctuation |
| Large negative (>3%) | Strong selling, possible catalyst |

### Percentage vs. Dollar

| Metric | Use Case |
|--------|----------|
| Dollar Change | Absolute move size |
| Percent Change | Relative significance |

A $10 move means different things for a $100 stock (10%) vs. a $1000 stock (1%).

## Analyzing Volume

### Volume Significance

| Volume Level | Meaning |
|--------------|---------|
| 2x+ Average | Exceptional interest |
| 1.5x Average | Above normal interest |
| Average | Normal trading |
| 0.5x Average | Low interest |

### Volume Context

| Scenario | Interpretation |
|----------|----------------|
| High volume + price up | Strong buying conviction |
| High volume + price down | Strong selling pressure |
| Low volume + price up | Weak rally, may not sustain |
| Low volume + price down | Orderly decline |

## Day Range Analysis

### Range Position

Calculate where price sits in the day's range:

```
Position = (Current - Low) / (High - Low) × 100%
```

| Position | Interpretation |
|----------|----------------|
| >80% | Near day high, bullish |
| 50% | Middle of range |
| <20% | Near day low, bearish |

### Range Width

| Width | Indicates |
|-------|-----------|
| Wide range | High volatility day |
| Narrow range | Consolidation |

## 52-Week Range Analysis

### Range Position

```
Position = (Current - 52-Week Low) / (52-Week High - 52-Week Low) × 100%
```

| Position | Interpretation |
|----------|----------------|
| >90% | Near 52-week high |
| 50-90% | Upper half of range |
| 10-50% | Lower half of range |
| <10% | Near 52-week low |

### Example Calculation

From the AAPL quote:
- Current: $270.01
- 52-Week Low: $169.21
- 52-Week High: $288.62

Position = ($270.01 - $169.21) / ($288.62 - $169.21) = 84.4%

AAPL is in the upper portion of its 52-week range.

## Market Cap Context

### Size Categories

| Market Cap | Category |
|------------|----------|
| >$200B | Mega-cap |
| $10B-$200B | Large-cap |
| $2B-$10B | Mid-cap |
| $300M-$2B | Small-cap |
| <$300M | Micro-cap |

### Size Implications

| Size | Characteristics |
|------|-----------------|
| Larger | More stable, less volatile |
| Smaller | More volatile, growth potential |

## Moving Average Analysis

### Price vs. Moving Averages

| Condition | Interpretation |
|-----------|----------------|
| Price > 50-day > 200-day | Strong uptrend |
| Price > 200-day > 50-day | Recovering uptrend |
| Price < 200-day < 50-day | Downtrend starting |
| Price < 50-day < 200-day | Strong downtrend |

### Key Signals

| Signal | Description |
|--------|-------------|
| Golden Cross | 50-day crosses above 200-day (bullish) |
| Death Cross | 50-day crosses below 200-day (bearish) |
| Support | Price bounces off moving average |
| Resistance | Price rejected at moving average |

### Distance from Averages

| Distance | Interpretation |
|----------|----------------|
| Far above | Potentially extended, pullback risk |
| Slightly above | Healthy uptrend |
| At average | Testing support/resistance |
| Slightly below | Weakness |
| Far below | Oversold, bounce potential |

## Exchange Information

### Major Exchanges

| Exchange | Characteristics |
|----------|-----------------|
| NYSE | Traditional, large-cap focus |
| NASDAQ | Tech-heavy, electronic |
| AMEX | Smaller companies, ETFs |
| OTC | Less regulated, higher risk |

## Quote Timing Considerations

### Market Hours

| Period | Quote Type |
|--------|------------|
| Pre-market | May differ from open |
| Regular hours | Most liquid, accurate |
| After-hours | Less liquid, wider spreads |
| Closed | Previous close |

### Data Freshness

| Quote Type | Delay |
|------------|-------|
| Real-time | Live |
| Delayed | 15-20 minutes |
| End of day | Previous close |

## Red Flags in Quotes

### Warning Signs

1. **Extreme moves** - >10% without news
2. **Unusual volume** - 5x+ normal without catalyst
3. **Trading halted** - Regulatory concern
4. **Wide bid-ask** - Low liquidity
5. **Gap from close** - Overnight news

## Using Quotes Effectively

### Quick Assessment Checklist

1. **Price direction**: Up or down today?
2. **Magnitude**: Normal or unusual move?
3. **Volume**: Confirming or diverging?
4. **Range position**: Near highs or lows?
5. **Trend**: Above or below averages?
6. **Valuation**: Reasonable market cap?

### Next Steps After Quote

| Finding | Action |
|---------|--------|
| Large move | Research catalyst |
| High volume | Investigate news |
| Near 52-week high | Check resistance |
| Near 52-week low | Check support |
| Below moving averages | Analyze trend |
