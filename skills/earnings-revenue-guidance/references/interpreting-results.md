# Interpreting Revenue Guidance Results

## Understanding Revenue Guidance Structure

### Guidance Components

| Component | Description | Use Case |
|-----------|-------------|----------|
| Dollar Range | Absolute revenue target | Model input |
| Growth Rate | YoY percentage change | Trend analysis |
| Constant Currency | FX-adjusted growth | Core performance |
| Segment Detail | Business unit breakdown | Mix analysis |
| M&A Contribution | Acquisition impact | Organic growth |

### Guidance Timeframes

| Timeframe | Typical Format | Reliability |
|-----------|----------------|-------------|
| Next Quarter | Specific range | Highest |
| Full Year | Annual target | High |
| Long-term | CAGR targets | Aspirational |

## Analyzing Revenue Ranges

### Range Interpretation Framework

```
Example: $41.15B - $41.25B

Midpoint: $41.20B
Range: $0.10B
Range as % of Midpoint: 0.24%

Classification:
- < 1%: Tight range, high confidence
- 1-2%: Normal range, good visibility
- 2-3%: Wide range, some uncertainty
- > 3%: Very wide, low visibility
```

### What Range Width Signals

| Range Width | Signal | Management View |
|-------------|--------|-----------------|
| Very Tight | High confidence | Clear demand visibility |
| Normal | Standard visibility | Business as usual |
| Wide | Uncertainty | Variable conditions |
| Very Wide | Low confidence | High volatility expected |

## Growth Rate Analysis

### Types of Growth Rates

| Type | Definition | When to Use |
|------|------------|-------------|
| Reported | As-stated in financials | Official results |
| Constant Currency | Excludes FX impact | Core performance |
| Organic | Excludes M&A | Underlying growth |
| Pro Forma | Includes M&A in prior | Apples-to-apples |

### Calculating Different Growth Rates

```
Example Company Data:
- Prior Year Revenue: $37.5B
- Current Year Guidance: $41.2B
- Acquisition Revenue: $1.5B
- FX Impact: +$0.3B

Reported Growth: ($41.2B / $37.5B) - 1 = 9.9%

Organic Growth:
- Adjusted Current: $41.2B - $1.5B = $39.7B
- Organic Growth: ($39.7B / $37.5B) - 1 = 5.9%

Constant Currency:
- FX-Adjusted: $41.2B - $0.3B = $40.9B
- CC Growth: ($40.9B / $37.5B) - 1 = 9.1%
```

## Currency Impact Deep Dive

### Understanding FX Effects

| USD Movement | International Revenue | Reported Growth Impact |
|--------------|----------------------|----------------------|
| Strengthening | Lower when converted | Negative (headwind) |
| Weakening | Higher when converted | Positive (tailwind) |
| Stable | Minimal change | Neutral |

### Quantifying Currency Impact

```
Example:
- Reported Growth: 9.0%
- Constant Currency Growth: 11.0%
- FX Impact: 9.0% - 11.0% = -2.0pp (headwind)

Interpretation: Currency reduced reported growth by 2 percentage points
True underlying growth is 11%, but FX makes it look like 9%
```

### FX Sensitivity Analysis

| International Revenue % | FX Sensitivity |
|-------------------------|----------------|
| < 30% | Low FX impact |
| 30-50% | Moderate FX impact |
| > 50% | High FX impact |

## M&A Contribution Analysis

### Separating Organic from Inorganic

```
Example: Salesforce with Informatica

Total Revenue Growth: 10.0%
Informatica Contribution: +0.8pp
Organic Growth: 10.0% - 0.8% = 9.2%

Key Question: Is 9.2% organic growth acceptable?
Compare to: Historical organic growth, peer organic growth
```

### M&A Integration Phases

| Phase | Revenue Treatment |
|-------|-------------------|
| Year 1 | All inorganic |
| Year 2 | Mostly inorganic (overlaps) |
| Year 3+ | Considered organic |

## Segment Revenue Analysis

### Building Segment Tables

| Segment | Q3 Revenue | Growth | Mix | Mix Change |
|---------|------------|--------|-----|------------|
| Cloud | $25.0B | +15% | 61% | +2pp |
| Services | $10.0B | +5% | 24% | -1pp |
| Other | $6.2B | +2% | 15% | -1pp |
| **Total** | **$41.2B** | **+10%** | **100%** | -- |

### Segment Analysis Framework

| Question | What to Look For |
|----------|------------------|
| Which segment is growing fastest? | Future driver |
| Which segment has highest margin? | Profit driver |
| Is mix shifting favorably? | Improving or deteriorating |
| Any segments declining? | Potential concern |

## Comparing Guidance to Consensus

### Building Comparison Table

| Metric | Company Guidance | Street Consensus | Delta |
|--------|------------------|------------------|-------|
| Revenue | $41.2B | $41.0B | +0.5% |
| Growth | 10.0% | 9.5% | +0.5pp |

### Interpreting the Gap

| Gap | Interpretation | Likely Reaction |
|-----|----------------|-----------------|
| Guidance > Street by 2%+ | Very bullish | Stock rises |
| Guidance > Street by 0-2% | Modestly bullish | Positive |
| Guidance = Street | Neutral | Mixed |
| Guidance < Street | Bearish | Stock falls |

## Historical Guidance Accuracy

### Tracking Beat/Miss History

| Quarter | Guidance Mid | Actual | Variance | Beat/Miss |
|---------|--------------|--------|----------|-----------|
| Q1 FY26 | $40.0B | $40.3B | +0.8% | Beat |
| Q2 FY26 | $40.5B | $40.7B | +0.5% | Beat |
| Q3 FY26 | $41.0B | TBD | TBD | TBD |

### Guidance Credibility Assessment

| Pattern | Interpretation | Adjustment |
|---------|----------------|------------|
| Consistent 1-2% beats | Conservative guidance | Model to high end |
| In-line results | Accurate forecaster | Use midpoint |
| Frequent misses | Optimistic guidance | Model to low end |

## Forward Modeling

### Using Guidance in Models

```
Step 1: Take guidance midpoint as base case
Step 2: Apply historical beat/miss pattern
Step 3: Adjust for known factors (FX, M&A)
Step 4: Create bear/base/bull scenarios

Example:
- Guidance Midpoint: $41.20B
- Historical Beat Pattern: +0.7%
- Expected Result: $41.20B × 1.007 = $41.49B
```

### Scenario Framework

| Scenario | Revenue | Growth | Probability |
|----------|---------|--------|-------------|
| Bull | $41.5B | +11% | 25% |
| Base | $41.2B | +10% | 50% |
| Bear | $40.8B | +9% | 25% |

## Red Flags in Revenue Guidance

| Red Flag | Concern |
|----------|---------|
| Guidance below consensus | Challenges ahead |
| Significantly widened range | Visibility deteriorating |
| Heavy M&A dependence | Organic weakness |
| Large FX caveat | Unstable conditions |
| Segment mix deteriorating | Quality decline |

## Next Steps After Analysis

1. **Update financial models** with new guidance
2. **Compare to consensus** and note gaps
3. **Calculate organic growth** excluding M&A
4. **Assess FX impact** and sensitivity
5. **Track segment trends** quarter-over-quarter
6. **Monitor for revisions** and updates
