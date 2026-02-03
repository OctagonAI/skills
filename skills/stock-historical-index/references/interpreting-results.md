# Interpreting Stock Historical Index Results

## Reading the Output

The octagon-agent returns comprehensive daily index data:

| Date | Open | High | Low | Close | Volume | Change | Change % | VWAP |
|------|------|------|-----|-------|--------|--------|----------|------|
| 2025-04-30 | 5,499.44 | 5,581.84 | 5,433.24 | 5,569.07 | 5.45B | +69.63 | +1.27% | 5,520.90 |

Key observations provided:
- Period closing value
- Highest volume day
- Largest daily gain
- Largest daily loss
- Trading days covered

## Understanding Each Field

### Price Fields

| Field | Description |
|-------|-------------|
| Open | First price at market open |
| High | Highest price during session |
| Low | Lowest price during session |
| Close | Final price at market close |

### Volume

| Aspect | Description |
|--------|-------------|
| What it is | Total shares traded across all index components |
| Unit | Shares (billions for major indices) |
| Use | Participation, conviction indicator |

### Change Fields

| Field | Description |
|-------|-------------|
| Change | Point difference from prior close |
| Change % | Percentage difference from prior close |

### VWAP

| Aspect | Description |
|--------|-------------|
| What it is | Volume-weighted average price |
| Calculation | Sum(Price × Volume) / Total Volume |
| Use | Average execution price |

## Calculating Returns

### Daily Return

```
Daily Return = (Close - Prior Close) / Prior Close × 100%
```

Already provided as "Change %"

### Period Return

```
Period Return = (End Close - Start Close) / Start Close × 100%
```

Example from data:
- Start (Jan 2): 5,868.56
- End (Apr 30): 5,569.07
- Return: -5.10%

### Cumulative Return

```
Cumulative = Product of (1 + daily return) - 1
```

## Analyzing Price Trends

### Trend Identification

| Pattern | Signal |
|---------|--------|
| Higher closes | Uptrend |
| Lower closes | Downtrend |
| Sideways | Consolidation |
| Pattern break | Reversal |

### Support and Resistance

| Level | How to Find |
|-------|-------------|
| Support | Repeated lows |
| Resistance | Repeated highs |
| Breakout | Move through level |
| Breakdown | Fall through level |

## Volume Analysis

### Volume Interpretation

| Volume + Price | Meaning |
|----------------|---------|
| High vol + up | Strong buying |
| High vol + down | Strong selling |
| Low vol + up | Weak rally |
| Low vol + down | Weak decline |

### Volume Patterns

| Pattern | Signal |
|---------|--------|
| Volume spike | Significant event |
| Rising volume | Increasing interest |
| Falling volume | Declining interest |
| Volume divergence | Potential reversal |

### Example

From the data:
- Highest volume: 9.49B on Apr 9
- Paired with: +9.90% gain
- **Interpretation**: Major buying conviction

## Identifying Significant Days

### Big Move Days

| Move | Significance |
|------|--------------|
| >3% | Major move |
| 2-3% | Significant |
| 1-2% | Notable |
| <1% | Normal |

### From Example Data

| Event | Date | Value |
|-------|------|-------|
| Largest gain | Apr 9 | +9.90% |
| Largest loss | Apr 4 | -4.12% |
| Highest volume | Apr 9 | 9.49B |

### What Big Days Tell You

| Pattern | Interpretation |
|---------|----------------|
| Big up, high volume | Strong rally |
| Big down, high volume | Capitulation |
| Big up, low volume | Short covering |
| Big down, low volume | Light selling |

## Volatility Assessment

### Daily Volatility

| Metric | Calculation |
|--------|-------------|
| Daily range % | (High - Low) / Close |
| Average range | Mean of daily ranges |
| Range expansion | Above average range |

### Period Volatility

| Metric | What It Shows |
|--------|---------------|
| Max-min spread | Total range |
| Std deviation | Return dispersion |
| Beta | vs. benchmark |

### Volatility Classification

| Daily Range % | Classification |
|---------------|----------------|
| <1% | Low volatility |
| 1-2% | Normal |
| 2-3% | Elevated |
| >3% | High volatility |

## OHLC Analysis

### Candlestick Interpretation

| Pattern | Meaning |
|---------|---------|
| Close > Open | Bullish day |
| Close < Open | Bearish day |
| Long upper wick | Selling pressure |
| Long lower wick | Buying pressure |
| Small body | Indecision |

### Gap Analysis

| Gap Type | Description |
|----------|-------------|
| Gap up | Open > Prior Close |
| Gap down | Open < Prior Close |
| Gap fill | Return to gap level |

## Benchmarking Applications

### Stock Comparison

```
Alpha = Stock Return - Index Return
```

### Example

If your stock returned +10% and S&P returned -5.1%:
- Alpha: +15.1% outperformance

### Sector Comparison

| Comparison | Purpose |
|------------|---------|
| Sector vs. S&P | Sector strength |
| Industry vs. Sector | Industry strength |
| Stock vs. Industry | Stock strength |

## Calendar Patterns

### Day of Week

| Day | Historical Tendency |
|-----|---------------------|
| Monday | Often volatile |
| Friday | Position squaring |
| Month end | Rebalancing |

### Seasonality

| Period | Pattern |
|--------|---------|
| January | Often positive |
| September | Often weak |
| Q4 | Holiday rally |

## Red Flags

### Data Quality Issues

1. **Missing dates** - Holidays, weekends
2. **Gaps** - Data issues
3. **Extreme values** - Verify accuracy
4. **Zero volume** - Holiday or error

### Interpretation Cautions

1. **One day** - Could be noise
2. **Low volume moves** - Less reliable
3. **Pre/post market** - Not included
4. **Index changes** - Composition shifts

## Practical Application

### Investment Decisions

| Finding | Implication |
|---------|-------------|
| Index uptrend | Bullish backdrop |
| Index downtrend | Bearish backdrop |
| High volatility | Risk management |
| Volume confirmation | Signal strength |

### Timing Context

| Use | Purpose |
|-----|---------|
| Entry timing | Market conditions |
| Exit timing | Market stress |
| Risk sizing | Volatility context |

## Next Steps After Analysis

### Follow-Up Research

| Finding | Action |
|---------|--------|
| Big move day | Research catalyst |
| Trend change | Verify with other data |
| Volume spike | Check news |
| Volatility spike | Review VIX |

### Related Skills

| Skill | Purpose |
|-------|---------|
| stock-performance | Stock vs. index |
| sector-performance-snapshot | Sector context |
| stock-quote | Current levels |
| industry-performance-snapshot | Industry context |
