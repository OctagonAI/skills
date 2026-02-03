# Interpreting Price Target Consensus Results

## Reading the Output

The octagon-agent returns consensus price target metrics:

| Metric | Value |
|--------|-------|
| Consensus Target | $303.11 |
| Median Target | $315.00 |
| Target High | $350.00 |
| Target Low | $220.00 |

## Understanding Each Metric

### Consensus Target (Average)

| Aspect | Description |
|--------|-------------|
| What it is | Mean of all analyst targets |
| Calculation | Sum / Count |
| Best for | General expectation |
| Weakness | Affected by outliers |

### Median Target

| Aspect | Description |
|--------|-------------|
| What it is | Middle value when sorted |
| Calculation | 50th percentile |
| Best for | Central tendency |
| Strength | Resistant to outliers |

### Target High

| Aspect | Description |
|--------|-------------|
| What it is | Highest analyst target |
| Represents | Most bullish view |
| Use | Maximum upside potential |
| Reality check | May require best-case scenario |

### Target Low

| Aspect | Description |
|--------|-------------|
| What it is | Lowest analyst target |
| Represents | Most bearish view |
| Use | Downside risk assessment |
| Reality check | May be overly pessimistic |

## Calculating Upside/Downside

### Step-by-Step

1. Get current price (e.g., $270.01)
2. Calculate potential for each target:

```
Potential = (Target - Current) / Current × 100%
```

### Example Calculations

| Target Type | Value | Current | Calculation | Result |
|-------------|-------|---------|-------------|--------|
| Consensus | $303.11 | $270.01 | (303.11-270.01)/270.01 | +12.3% |
| Median | $315.00 | $270.01 | (315.00-270.01)/270.01 | +16.7% |
| High | $350.00 | $270.01 | (350.00-270.01)/270.01 | +29.6% |
| Low | $220.00 | $270.01 | (220.00-270.01)/270.01 | -18.5% |

## Analyzing the Range

### Spread Metrics

| Metric | Formula |
|--------|---------|
| Range | High - Low |
| Spread % | (High - Low) / Consensus × 100% |
| Upside Range | High - Consensus |
| Downside Range | Consensus - Low |

### Example

- High: $350.00
- Low: $220.00
- Range: $130.00
- Consensus: $303.11
- Spread: 42.9%

### Spread Interpretation

| Spread % | Meaning |
|----------|---------|
| <20% | Strong agreement |
| 20-30% | Good consensus |
| 30-50% | Moderate disagreement |
| >50% | High uncertainty |

## Consensus vs. Median Comparison

### Reading the Relationship

| Condition | Interpretation |
|-----------|----------------|
| Consensus > Median | Bullish outliers pulling up average |
| Consensus < Median | Bearish outliers pulling down average |
| Consensus ≈ Median | Symmetric distribution |

### Which to Use

| Situation | Prefer |
|-----------|--------|
| Large gap between them | Median |
| Similar values | Either |
| Want conservative | Lower of the two |
| Want aggressive | Higher of the two |

## Position Relative to Range

### Price Position Analysis

```
Position = (Current - Low) / (High - Low) × 100%
```

### Interpretation

| Position | Current Price Is... |
|----------|---------------------|
| 0% | At analyst low |
| 25% | Lower quarter |
| 50% | Middle of range |
| 75% | Upper quarter |
| 100% | At analyst high |
| >100% | Above all targets |
| <0% | Below all targets |

### Example

- Current: $270.01
- Low: $220.00
- High: $350.00
- Position: (270.01 - 220) / (350 - 220) = 38.5%

**Interpretation**: Price is in the lower half of the analyst range, suggesting potential upside.

## Risk/Reward Analysis

### Calculating Risk/Reward

```
Upside = (Consensus - Current) / Current
Downside = (Current - Low) / Current
Risk/Reward Ratio = Upside / Downside
```

### Example

- Upside: +12.3%
- Downside: -18.5%
- Ratio: 12.3 / 18.5 = 0.66

### Interpretation

| Ratio | Meaning |
|-------|---------|
| >2.0 | Favorable risk/reward |
| 1.0-2.0 | Balanced |
| 0.5-1.0 | Moderate risk |
| <0.5 | Unfavorable risk/reward |

## Identifying Outliers

### Signs of Outlier Impact

| Indicator | Suggests |
|-----------|----------|
| Large consensus-median gap | Outliers present |
| Extreme high or low | One analyst very different |
| Range > 60% of consensus | Wide dispersion |

### Adjusting for Outliers

| Approach | Method |
|----------|--------|
| Use median | Ignore outliers |
| Trimmed mean | Exclude extremes |
| Focus on cluster | Where most targets are |

## Analyst Agreement Signals

### Strong Agreement

| Indicator | Value |
|-----------|-------|
| Spread | <25% |
| Consensus-Median gap | <5% |
| Range | Narrow |

### Weak Agreement

| Indicator | Value |
|-----------|-------|
| Spread | >50% |
| Consensus-Median gap | >10% |
| Range | Wide |

## Red Flags

### Warning Signs

1. **Price above high target** - All analysts see downside
2. **Price below low target** - Something analysts are missing?
3. **Very wide range** - High uncertainty
4. **Stale targets** - May be outdated
5. **Few analysts** - Less reliable consensus

## Practical Decision Framework

### Investment Signals

| Finding | Implication |
|---------|-------------|
| Strong upside, tight consensus | Potentially attractive |
| Strong upside, wide range | Higher risk opportunity |
| Limited upside, tight consensus | Fairly valued |
| Downside indicated | Caution warranted |

### Position Sizing Guide

| Consensus View | Suggested Approach |
|----------------|-------------------|
| >25% upside, tight range | Consider overweight |
| 10-25% upside, normal range | Standard weight |
| <10% upside | Neutral or underweight |
| Downside risk | Reduce or avoid |

## Next Steps After Analysis

### Follow-Up Research

| Finding | Action |
|---------|--------|
| Wide range | Understand bull/bear cases |
| Consensus-median gap | Identify outliers |
| Near targets | Monitor for revisions |
| Strong upside | Verify with fundamentals |

### Related Skills

| Skill | Use For |
|-------|---------|
| stock-quote | Get current price |
| price-target-summary | Historical trends |
| analyst-estimates | Earnings expectations |
| income-statement | Fundamental check |
