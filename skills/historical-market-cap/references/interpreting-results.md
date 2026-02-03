# Interpreting Historical Market Cap Results

## Reading the Output

The octagon-agent returns historical market cap data:

| Date | Market Cap (USD) |
|------|------------------|
| 2025-04-30 | $3.17 trillion |
| 2025-02-25 | $3.70 trillion |
| 2025-04-08 | $2.57 trillion |

Summary provided:
- Highest value and date
- Lowest value and date
- Most recent value
- Missing data notes

## Understanding the Data

### Data Components

| Component | Description |
|-----------|-------------|
| Date | Trading day |
| Market Cap | Price × Shares Outstanding |
| Currency | USD |
| Frequency | Daily (trading days only) |

### Data Quality Notes

| Issue | Consideration |
|-------|---------------|
| Missing dates | Weekends/holidays excluded |
| Gaps | Data availability issues |
| Adjustments | Split-adjusted |

## Calculating Key Metrics

### Period Change

```
Change = End Market Cap - Start Market Cap
Change % = (End - Start) / Start × 100%
```

### Example

- Start (Jan 2): $3.50T
- End (Apr 30): $3.17T
- Change: -$0.33T
- Change %: -9.4%

### Growth Rates

| Period | Formula |
|--------|---------|
| Daily | (Today - Yesterday) / Yesterday |
| Weekly | (This Week - Last Week) / Last Week |
| Monthly | (This Month - Last Month) / Last Month |
| Annual | (This Year - Last Year) / Last Year |
| CAGR | (End/Start)^(1/years) - 1 |

## Analyzing Peaks and Troughs

### Identifying Maximum

| Metric | From Example |
|--------|--------------|
| Peak Value | $3.70 trillion |
| Peak Date | 2025-02-25 |
| Context | All-time high? Period high? |

### Identifying Minimum

| Metric | From Example |
|--------|--------------|
| Trough Value | $2.57 trillion |
| Trough Date | 2025-04-08 |
| Context | All-time low? Period low? |

### Drawdown Analysis

```
Drawdown = (Trough - Peak) / Peak × 100%
```

Example:
- Peak: $3.70T
- Trough: $2.57T
- Drawdown: -30.5%

### Recovery Analysis

```
Recovery = (Current - Trough) / Trough × 100%
```

Example:
- Trough: $2.57T
- Current: $3.17T
- Recovery: +23.3%

## Trend Analysis

### Trend Identification

| Pattern | Characteristics |
|---------|-----------------|
| Uptrend | Higher peaks, higher troughs |
| Downtrend | Lower peaks, lower troughs |
| Consolidation | Sideways movement |
| Reversal | Trend direction change |

### Trend Strength

| Indicator | Strong Trend | Weak Trend |
|-----------|--------------|------------|
| Slope | Steep | Shallow |
| Consistency | Few counter-moves | Many pullbacks |
| Duration | Extended | Brief |

## Volatility Assessment

### Calculating Volatility

| Metric | Formula |
|--------|---------|
| Range | High - Low |
| Range % | (High - Low) / Average |
| Daily Vol | Std dev of daily changes |

### Example

- High: $3.70T
- Low: $2.57T
- Range: $1.13T
- Average: ~$3.14T
- Range %: 36%

### Volatility Classification

| Range % | Classification |
|---------|----------------|
| <15% | Low volatility |
| 15-30% | Normal volatility |
| 30-50% | High volatility |
| >50% | Very high volatility |

## Period Comparisons

### Month-over-Month

| Month | Market Cap | Change |
|-------|------------|--------|
| Jan | $3.50T | - |
| Feb | $3.60T | +2.9% |
| Mar | $3.00T | -16.7% |
| Apr | $3.17T | +5.7% |

### Year-over-Year

```
YoY Change = (This Year - Last Year) / Last Year × 100%
```

### Quarter-over-Quarter

| Quarter | Calculation |
|---------|-------------|
| Q1 vs Q4 | End of Q1 / End of Q4 - 1 |
| Q2 vs Q1 | End of Q2 / End of Q1 - 1 |

## Milestone Tracking

### Key Thresholds

| Milestone | Significance |
|-----------|--------------|
| $1 Trillion | Rare, elite status |
| $2 Trillion | Very select group |
| $3 Trillion | World's most valuable |

### First-Time Events

| Event | How to Find |
|-------|-------------|
| First $1T | First date above threshold |
| Held above | Consecutive days above |
| Lost status | First date below after above |

## Comparative Analysis

### Multiple Stocks

| Date | AAPL | MSFT | GOOGL |
|------|------|------|-------|
| Jan 1 | $3.5T | $3.0T | $2.0T |
| Apr 30 | $3.2T | $3.2T | $2.1T |

### Relative Performance

```
Relative = Stock Cap Change % - Benchmark Change %
```

## Time-Weighted Analysis

### Smoothing

| Method | Purpose |
|--------|---------|
| 7-day average | Reduce daily noise |
| 30-day average | Monthly trend |
| 90-day average | Quarterly trend |

### Rate of Change

| Timeframe | Calculation |
|-----------|-------------|
| 1-week | (Today - 5 days ago) / 5 days ago |
| 1-month | (Today - 21 days ago) / 21 days ago |
| 3-month | (Today - 63 days ago) / 63 days ago |

## Red Flags

### Data Quality Issues

1. **Large gaps** - Missing significant periods
2. **Extreme jumps** - May indicate errors
3. **Inconsistent adjustments** - Split issues
4. **Stale data** - Not updated recently

### Analysis Concerns

1. **Short timeframe** - May not be representative
2. **One-time events** - Distort trends
3. **Corporate actions** - Mergers, spin-offs
4. **Share count changes** - Dilution, buybacks

## Practical Application

### Investment Signals

| Finding | Implication |
|---------|-------------|
| Near all-time high | Momentum or resistance |
| Near period low | Support or breakdown |
| Breaking trend | Potential reversal |
| Expanding range | Increasing volatility |

### Valuation Context

| Historical Position | Consideration |
|---------------------|---------------|
| Above historical avg | Premium valuation |
| At historical avg | Fair value |
| Below historical avg | Discount or concerns |

## Next Steps After Analysis

### Follow-Up Research

| Finding | Action |
|---------|--------|
| Major peak | What drove it? |
| Major trough | What caused it? |
| Trend change | Identify catalyst |
| Unusual move | Verify data accuracy |

### Related Skills

| Skill | Purpose |
|-------|---------|
| company-market-cap | Current snapshot |
| stock-performance | Price context |
| income-statement | Earnings evolution |
| financial-metrics-analysis | Valuation trends |
