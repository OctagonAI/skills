# Interpreting 10-Q Analysis Results

## Reading the Output

The octagon-agent returns 10-Q analysis with quarterly metrics and source citations:

**Example Output:**
- Total Revenue: $143.76 billion (up from $124.30 billion YoY)
- Net Income: $42.10 billion
- Basic EPS: $2.85
- Diluted EPS: $2.84
- iPhone Revenue: $85.27 billion (+23.4% YoY)
- Operating Income: $50.85 billion
- Operating Margin: ~35.4%
- Cash Position: $45.32 billion
- Long-term Debt: $76.69 billion

## Understanding Quarterly Comparisons

### Year-over-Year (YoY)

Compare current quarter to same quarter last year:
- Eliminates seasonality effects
- Shows true annual growth rate
- Most common comparison method

**Example**: Q1 2026 vs Q1 2025

### Quarter-over-Quarter (QoQ)

Compare current quarter to prior quarter:
- Shows sequential momentum
- Affected by seasonality
- Useful for trend direction

**Example**: Q1 2026 vs Q4 2025

### Trailing Twelve Months (TTM)

Sum of last four quarters:
- Smooths quarterly volatility
- Annualized view of performance
- Useful for valuation metrics

## Analyzing Quarterly Metrics

### Revenue Analysis

| Metric | What to Analyze |
|--------|-----------------|
| Total Revenue | YoY growth rate |
| Revenue by Segment | Which segments driving growth |
| Geographic Revenue | Regional performance |
| Sequential Change | QoQ momentum |

### Profitability Analysis

| Metric | What to Analyze |
|--------|-----------------|
| Gross Margin | Pricing power, cost trends |
| Operating Margin | Operational efficiency |
| Net Margin | Bottom-line performance |
| EPS vs Estimates | Beat/miss consensus |

### Segment Performance

Track each segment's:
- Revenue contribution (% of total)
- YoY growth rate
- Sequential change
- Margin if disclosed

## Quarterly Patterns

### Seasonality by Industry

| Industry | Strong Quarters | Weak Quarters |
|----------|-----------------|---------------|
| Retail | Q4 (Holiday) | Q1 |
| Tech Hardware | Q4, Q1 | Q2, Q3 |
| Enterprise Software | Q4 | Q1 |
| Advertising | Q4 | Q1 |
| Travel | Q2, Q3 | Q1 |

### Fiscal Year Considerations

Companies have different fiscal year ends:
- **Calendar Year**: Ends Dec 31 (Most companies)
- **AAPL**: Ends late September
- **MSFT**: Ends June 30
- **Retail**: Often ends late January

## Comparing to Expectations

### vs Analyst Estimates

| Result | Implication |
|--------|-------------|
| Beat on Revenue + EPS | Strong quarter, positive reaction |
| Beat EPS, Miss Revenue | Cost cuts, not growth |
| Miss EPS, Beat Revenue | Margin pressure |
| Miss on Both | Weak quarter, negative reaction |

### vs Company Guidance

Check if results are:
- Within guidance range
- Above/below midpoint
- Triggering guidance revision

## Balance Sheet Updates

### Liquidity Metrics

| Metric | What to Check |
|--------|---------------|
| Cash & Equivalents | Liquidity buffer |
| Short-term Investments | Total liquid assets |
| Current Ratio | Short-term solvency |
| Quick Ratio | Immediate liquidity |

### Debt Metrics

| Metric | What to Check |
|--------|---------------|
| Short-term Debt | Near-term obligations |
| Long-term Debt | Total leverage |
| Net Debt | Debt minus cash |
| Debt/EBITDA | Leverage ratio |

## Red Flags in 10-Q

### Revenue Red Flags
1. **Revenue declining QoQ and YoY**: Sustained weakness
2. **Segment concentration increasing**: Dependency risk
3. **Deferred revenue declining**: Future revenue pressure

### Margin Red Flags
1. **Gross margin compression**: Pricing/cost issues
2. **Operating margin decline**: Efficiency problems
3. **SG&A growing faster than revenue**: Cost control issues

### Balance Sheet Red Flags
1. **Cash declining significantly**: Burn rate concern
2. **Debt increasing rapidly**: Leverage risk
3. **Inventory buildup**: Demand weakness
4. **Receivables growing faster than revenue**: Collection issues

## Source Citations

The agent provides page references to the 10-Q filing:

```
Sources:
1. Apple Inc. (10-Q) - 2026-Q1, Page: 9
2. Apple Inc. (10-Q) - 2026-Q1, Page: 4
...
```

Use these to:
- Verify extracted metrics
- Read management commentary
- Access detailed tables

## Sequential Trend Analysis

Track metrics across multiple quarters:

| Metric | Q1 | Q2 | Q3 | Q4 | Trend |
|--------|----|----|----|----|-------|
| Revenue | $X | $X | $X | $X | ↑↓→ |
| Margin | X% | X% | X% | X% | ↑↓→ |
| EPS | $X | $X | $X | $X | ↑↓→ |

Look for:
- Accelerating growth
- Decelerating growth
- Margin expansion/compression
- Consistent vs volatile patterns

## Next Steps After Analysis

1. **Compare to 10-K**: How does quarter track to annual expectations
2. **Review earnings call**: Management commentary on quarterly results
3. **Check 8-K filings**: Any material events since quarter end
4. **Compare to peers**: Relative quarterly performance
5. **Update estimates**: Revise full-year projections based on quarter
