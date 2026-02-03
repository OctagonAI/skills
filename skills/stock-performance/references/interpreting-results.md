# Interpreting Stock Performance Results

## Reading the Output

The octagon-agent returns structured price data with dates and metrics:

| Date | Closing Price | Volume |
|------|---------------|--------|
| 2026-02-02 | $270.01 | 73,677,607 |
| 2026-01-30 | $259.48 | 92,443,408 |

## Understanding Price Data

### Price Components

| Component | Description |
|-----------|-------------|
| Date | Trading day |
| Open | First trade price |
| High | Highest price of day |
| Low | Lowest price of day |
| Close | Last trade price |
| Volume | Shares traded |

### Adjusted vs. Unadjusted

| Type | Adjusts For |
|------|-------------|
| Raw Close | Nothing |
| Adjusted Close | Dividends, splits |

Use adjusted close for return calculations over longer periods.

## Analyzing Price Trends

### Trend Identification

| Pattern | How to Identify |
|---------|-----------------|
| Uptrend | Series of higher lows |
| Downtrend | Series of lower highs |
| Consolidation | Prices in a range |
| Reversal | Trend direction change |

### Trend Strength

| Factor | Strong Trend | Weak Trend |
|--------|--------------|------------|
| Slope | Steep | Shallow |
| Duration | Extended | Brief |
| Volume | Confirming | Diverging |
| Pullbacks | Shallow | Deep |

## Calculating Returns

### Period Return

```
Return = (End Price - Start Price) / Start Price × 100%
```

### Example

- Start: $259.37 (Jan 9)
- End: $270.01 (Feb 2)
- Return: ($270.01 - $259.37) / $259.37 = 4.1%

### Annualized Return

```
Annualized = (1 + Period Return) ^ (365 / Days) - 1
```

## Evaluating Volume

### Volume Context

| Volume Level | Interpretation |
|--------------|----------------|
| Above Average | High interest |
| Average | Normal trading |
| Below Average | Low interest |
| Spike | Unusual activity |

### Volume-Price Relationship

| Combination | Meaning |
|-------------|---------|
| Price Up + Volume Up | Strong buying |
| Price Up + Volume Down | Weak rally |
| Price Down + Volume Up | Strong selling |
| Price Down + Volume Down | Lack of sellers |

## Key Price Levels

### 52-Week Range

| Level | Significance |
|-------|--------------|
| 52-Week High | Resistance, breakout point |
| 52-Week Low | Support, breakdown point |
| Near High | Bullish territory |
| Near Low | Bearish territory |

### Psychological Levels

| Level Type | Examples |
|------------|----------|
| Round Numbers | $100, $250, $500 |
| Prior Highs | Previous resistance |
| Prior Lows | Previous support |
| Gap Levels | Unfilled gaps |

## Volatility Assessment

### Measuring Volatility

| Measure | Calculation |
|---------|-------------|
| Range | High - Low |
| Average True Range | Average daily range |
| Standard Deviation | Price dispersion |
| Beta | vs. market volatility |

### Volatility Interpretation

| Level | Characteristic |
|-------|----------------|
| High | Large daily swings |
| Low | Stable, small moves |
| Increasing | Growing uncertainty |
| Decreasing | Stabilizing |

## Comparing Performance

### Relative Strength

| Comparison | What It Shows |
|------------|---------------|
| vs. Market | Alpha generation |
| vs. Sector | Industry position |
| vs. Peers | Competitive standing |

### Calculating Relative Performance

```
Relative = Stock Return - Benchmark Return
```

## Common Patterns

### Bullish Patterns

| Pattern | Characteristics |
|---------|-----------------|
| Breakout | Price exceeds resistance |
| Higher Lows | Accumulation |
| Volume Surge Up | Buying interest |

### Bearish Patterns

| Pattern | Characteristics |
|---------|-----------------|
| Breakdown | Price falls below support |
| Lower Highs | Distribution |
| Volume Surge Down | Selling pressure |

## Red Flags

### Price Red Flags

1. **Sharp drop** - Investigate cause
2. **Gap down** - News, earnings miss
3. **Break of support** - Trend change
4. **Extreme volatility** - Uncertainty

### Volume Red Flags

1. **Volume spike + price drop** - Heavy selling
2. **Declining volume rally** - Weak momentum
3. **Unusual volume no news** - Insider activity?
4. **Volume dry-up** - Lack of interest

## Using Results for Analysis

### Investment Decisions

| Finding | Implication |
|---------|-------------|
| Uptrend + volume | Consider entry |
| Near 52-week high | Resistance ahead |
| Near 52-week low | Support or breakdown? |
| Outperforming peers | Relative strength |

### Risk Assessment

| Factor | Higher Risk | Lower Risk |
|--------|-------------|------------|
| Volatility | High | Low |
| Trend | Against position | With position |
| Volume | Declining | Stable/increasing |
| Beta | >1 | <1 |

## Next Steps After Analysis

1. **Contextualize**: Check for news, earnings
2. **Compare**: Peers and benchmarks
3. **Extend timeframe**: Longer-term perspective
4. **Fundamentals**: Price vs. value
5. **Technicals**: Chart patterns, indicators
6. **Risk assess**: Position sizing
