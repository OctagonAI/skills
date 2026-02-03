# Interpreting Company Market Cap Results

## Reading the Output

The octagon-agent returns precise market cap data with date context:

| Date | Market Capitalization (USD) |
|------|----------------------------|
| 2026-02-02 | $3,968,586,877,215.00 |

The response includes:
- Exact dollar value
- Rounded representation (e.g., $3.97 trillion)
- As-of date
- Data source

## Understanding the Number

### Reading Large Numbers

| Value | Abbreviation | Example |
|-------|--------------|---------|
| Billions | B | $50B = $50,000,000,000 |
| Trillions | T | $3.97T = $3,970,000,000,000 |

### Precision Levels

| Use Case | Precision |
|----------|-----------|
| Communication | Rounded (e.g., $3.97T) |
| Calculations | Full value |
| Comparisons | Same precision for all |

## Size Classification

### Determining Category

| If Market Cap Is... | Category |
|---------------------|----------|
| >$200 billion | Mega-cap |
| $10B - $200B | Large-cap |
| $2B - $10B | Mid-cap |
| $300M - $2B | Small-cap |
| $50M - $300M | Micro-cap |
| <$50M | Nano-cap |

### Example Classification

Apple at $3.97T:
- **Category**: Mega-cap
- **Sub-category**: Trillion-dollar club
- **Rank**: Among world's most valuable

## Valuation Context

### Calculating Valuation Ratios

If you have additional data:

| Ratio | Formula | Interpretation |
|-------|---------|----------------|
| P/E | $3.97T / $100B earnings = 39.7x | Earnings multiple |
| P/S | $3.97T / $400B revenue = 9.9x | Revenue multiple |
| P/B | $3.97T / $75B book = 52.9x | Book value multiple |

### Ratio Interpretation

| Level | P/E Range | Meaning |
|-------|-----------|---------|
| Low | <15x | Value, mature, or troubled |
| Moderate | 15-25x | Fairly valued |
| High | 25-40x | Growth expectations |
| Very High | >40x | High growth or speculation |

## Historical Comparison

### Tracking Changes

| Timeframe | What to Look For |
|-----------|------------------|
| Daily | Normal fluctuation |
| Weekly | Short-term trend |
| Monthly | Meaningful moves |
| Yearly | Significant growth/decline |

### Calculating Growth

```
Growth = (Current Cap - Prior Cap) / Prior Cap × 100%
```

Example:
- Current: $3.97T
- 1 Year Ago: $2.85T
- Growth: ($3.97T - $2.85T) / $2.85T = 39.3%

## Peer Comparison

### Relative Size

| Metric | Calculation |
|--------|-------------|
| Ratio to Leader | Company Cap / Leader Cap |
| Rank in Industry | Position by size |
| Gap to Next | Difference to adjacent |

### Industry Context

| Position | Interpretation |
|----------|----------------|
| #1 in industry | Market leader |
| Top 3 | Major player |
| Middle of pack | Competitive position |
| Smaller | Challenger/niche |

## Global Perspective

### Scale Reference

| Comparison | Context |
|------------|---------|
| vs. Country GDP | Economic significance |
| vs. S&P 500 | Index influence |
| vs. Global Top 10 | Elite status |

### Trillion-Dollar Context

| Milestone | Significance |
|-----------|--------------|
| First $1T | Historic achievement |
| $2T+ | Global economic force |
| $3T+ | Among most valuable ever |

## Market Cap Components

### Understanding the Calculation

```
Market Cap = Share Price × Shares Outstanding
```

### Component Analysis

| Component | Check |
|-----------|-------|
| Share Price | Current, real-time or delayed? |
| Shares Outstanding | Basic or diluted? |
| Float | Tradeable portion |

### Float-Adjusted

| Metric | Description |
|--------|-------------|
| Full Market Cap | All shares |
| Float-Adjusted | Excludes insider/restricted |
| Free Float | Only freely tradeable |

## Enterprise Value Consideration

### When to Use EV

| Situation | Use |
|-----------|-----|
| M&A analysis | EV includes debt |
| Capital-intensive | Debt matters |
| Comparing structures | Different leverage |
| Pure market view | Market cap only |

### EV Calculation

```
Enterprise Value = Market Cap + Total Debt - Cash
```

## Data Considerations

### Timing

| Factor | Impact |
|--------|--------|
| Market hours | Real-time updates |
| After hours | May differ from close |
| Weekends | Friday close |
| Holidays | Last trading day |

### Accuracy

| Check | Purpose |
|-------|---------|
| As-of date | Data freshness |
| Source | Reliability |
| Share count | Current or delayed |

## Red Flags

### Unusual Values

1. **Dramatic change** - Major event likely
2. **Doesn't match news** - Verify data
3. **Outlier vs. peers** - Investigate reason
4. **Calculation mismatch** - Check components

## Next Steps After Analysis

### Additional Research

| Finding | Action |
|---------|--------|
| Size classification | Compare to peers |
| Recent change | Research catalyst |
| Valuation context | Calculate ratios |
| Historical perspective | Track trend |

### Related Queries

| Purpose | Skill |
|---------|-------|
| Current price | stock-quote |
| Compare to peers | batch-market-cap |
| Earnings context | income-statement |
| Asset backing | balance-sheet |
