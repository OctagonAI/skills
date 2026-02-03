# Interpreting Stock Price Change Results

## Reading the Output

The octagon-agent returns price change statistics across multiple timeframes:

| Time Period | Percentage Change |
|-------------|-------------------|
| 1 Day | 4.06% |
| 5 Days | 4.80% |
| 1 Month | -0.37% |
| 3 Months | -0.13% |
| 6 Months | 33.42% |
| YTD | -0.37% |
| 1 Year | 18.42% |
| 3 Years | 79.03% |
| 5 Years | 100.02% |
| 10 Years | 1,043.14% |
| All-Time High | 210,270.08% |

## Understanding Each Period

### 1 Day

| Aspect | Description |
|--------|-------------|
| What it is | Today's change |
| Use | Daily momentum |
| Context | Normal range ±2-3% |

### 5 Days (1 Week)

| Aspect | Description |
|--------|-------------|
| What it is | Past trading week |
| Use | Weekly trend |
| Context | Normal range ±5% |

### 1 Month

| Aspect | Description |
|--------|-------------|
| What it is | Past 21 trading days |
| Use | Short-term trend |
| Context | Normal range ±10% |

### 3 Months (Quarter)

| Aspect | Description |
|--------|-------------|
| What it is | Past 63 trading days |
| Use | Quarterly performance |
| Context | Earnings cycle relevant |

### 6 Months

| Aspect | Description |
|--------|-------------|
| What it is | Half-year performance |
| Use | Medium-term trend |
| Context | Market cycle relevant |

### YTD (Year-to-Date)

| Aspect | Description |
|--------|-------------|
| What it is | From Jan 1 to now |
| Use | Calendar year performance |
| Context | Common reporting period |

### 1 Year

| Aspect | Description |
|--------|-------------|
| What it is | Rolling 12 months |
| Use | Annual performance |
| Context | Standard comparison period |

### 3 Years

| Aspect | Description |
|--------|-------------|
| What it is | Rolling 36 months |
| Use | Business cycle |
| Context | Medium-term track record |

### 5 Years

| Aspect | Description |
|--------|-------------|
| What it is | Rolling 60 months |
| Use | Full market cycle |
| Context | Investment horizon |

### 10 Years

| Aspect | Description |
|--------|-------------|
| What it is | Rolling 120 months |
| Use | Long-term performance |
| Context | Secular trend |

### All-Time High

| Aspect | Description |
|--------|-------------|
| What it is | Return from first trading day |
| Use | Total historical return |
| Context | Inception to date |

## Evaluating Performance

### Short-Term Classification

| 1-Month Return | Classification |
|----------------|----------------|
| >10% | Exceptional |
| 5-10% | Strong |
| 0-5% | Moderate |
| -5 to 0% | Weak |
| <-5% | Poor |

### Annual Classification

| 1-Year Return | Classification |
|---------------|----------------|
| >50% | Exceptional |
| 25-50% | Very strong |
| 10-25% | Strong |
| 0-10% | Moderate |
| -10 to 0% | Weak |
| <-10% | Poor |

### Long-Term Classification

| 10-Year Return | Classification |
|----------------|----------------|
| >500% | Exceptional |
| 200-500% | Very strong |
| 100-200% | Strong |
| 50-100% | Moderate |
| 0-50% | Below average |

## Momentum Analysis

### Reading Momentum

| Pattern | Meaning |
|---------|---------|
| Short-term > Long-term | Accelerating |
| Short-term < Long-term | Decelerating |
| All positive | Consistent strength |
| Mixed signs | Transitioning |

### Example Analysis

From AAPL data:
- 1 Day: +4.06% (strong)
- 1 Month: -0.37% (slight weakness)
- 1 Year: +18.42% (solid)

**Interpretation**: Strong day, mild recent consolidation, healthy annual return.

### Momentum Signals

| Signal | Pattern |
|--------|---------|
| Strong momentum | 1D > 5D > 1M (positive) |
| Weakening momentum | 1D < 5D < 1M |
| Recovery | 1D positive after negative 1M |
| Breaking down | 1D negative after positive 1M |

## Trend Consistency

### Healthy Uptrend

| Check | Expected |
|-------|----------|
| 1 Year | Positive |
| 6 Months | Positive |
| 3 Months | Positive |
| 1 Month | Positive |

### Pullback in Uptrend

| Check | Expected |
|-------|----------|
| 1 Year | Positive |
| 6 Months | Positive |
| 3 Months | Mixed |
| 1 Month | Negative |

### Downtrend

| Check | Expected |
|-------|----------|
| 1 Year | Negative |
| 6 Months | Negative |
| 3 Months | Negative |
| 1 Month | Negative |

## Annualizing Returns

### Calculation

```
Annualized = (1 + Total Return)^(1/Years) - 1
```

### Examples

| Period | Return | Annualized |
|--------|--------|------------|
| 3 Years | 79.03% | 21.4%/year |
| 5 Years | 100.02% | 14.9%/year |
| 10 Years | 1,043.14% | 27.3%/year |

### Benchmark Comparison

| Annualized | vs. Market (7-10%) |
|------------|-------------------|
| >15% | Significant outperformance |
| 10-15% | Slight outperformance |
| 7-10% | Market-like |
| <7% | Underperformance |

## All-Time High Context

### Distance from ATH

If ATH gain is 210,270% from inception, calculate distance from current ATH:

```
% from ATH = (ATH Price - Current) / ATH Price × 100%
```

### ATH Position

| Position | Meaning |
|----------|---------|
| At ATH | Maximum strength |
| 5% below | Minor pullback |
| 10% below | Correction territory |
| 20% below | Bear market |

## Comparing Stocks

### Side-by-Side

| Period | AAPL | MSFT | GOOGL |
|--------|------|------|-------|
| 1 Year | 18% | 25% | 15% |
| 5 Year | 100% | 150% | 80% |

### Ranking

| Metric | Use |
|--------|-----|
| 1-Year rank | Recent winner |
| 5-Year rank | Consistent performer |
| Risk-adjusted | Sharpe ratio |

## Red Flags

### Warning Signs

1. **All negative periods** - Fundamental issues
2. **Long-term negative** - Secular decline
3. **Extreme short-term** - Unsustainable move
4. **Inconsistent pattern** - High volatility

### Data Quality

1. **Stock splits** - Should be adjusted
2. **Dividends** - Price vs. total return
3. **Corporate actions** - May distort history

## Practical Application

### Investment Signals

| Finding | Implication |
|---------|-------------|
| Strong all periods | Consistent winner |
| Strong long, weak short | Pullback opportunity? |
| Weak long, strong short | Mean reversion risk |
| All negative | Avoid or short |

### Position Sizing

| Pattern | Suggested Approach |
|---------|-------------------|
| Consistent strength | Full position |
| Mixed signals | Reduced position |
| Weakness | Wait or avoid |

## Next Steps After Analysis

### Follow-Up Research

| Finding | Action |
|---------|--------|
| Strong returns | Verify fundamentals support |
| Weak short-term | Check for catalysts |
| Exceptional long-term | Sustainable? |
| Poor performance | Why? Investigate |

### Related Skills

| Skill | Purpose |
|-------|---------|
| stock-quote | Current price |
| stock-performance | Daily data |
| stock-historical-index | vs. market |
| financial-metrics-analysis | Fundamentals |
