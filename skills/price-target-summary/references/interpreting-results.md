# Interpreting Price Target Summary Results

## Reading the Output

The octagon-agent returns price target data across multiple timeframes:

| Timeframe | Number of Analysts | Average Price Target |
|-----------|-------------------|---------------------|
| Last Month | 9 | $305.72 |
| Last Quarter | 16 | $312.80 |
| Last Year | 48 | $282.91 |
| All Time | 229 | $219.71 |

## Understanding the Data

### Key Components

| Component | Description |
|-----------|-------------|
| Timeframe | Period for target aggregation |
| Number of Analysts | Count of unique analysts |
| Average Price Target | Mean of all targets |

### Data Sources

Targets aggregated from:
- StreetInsider
- TheFly
- Benzinga
- Investment bank research
- Independent analysts

## Analyzing Trends

### Timeframe Comparison

| Comparison | What It Shows |
|------------|---------------|
| Month vs. Quarter | Recent momentum |
| Quarter vs. Year | Medium-term trend |
| Recent vs. All-Time | Historical evolution |

### Trend Patterns

| Pattern | Interpretation |
|---------|----------------|
| Rising over time | Increasing optimism |
| Falling over time | Growing concern |
| Stable | Consensus maintained |
| Volatile | Uncertainty |

### Example Analysis

From the AAPL data:
- Last Month: $305.72
- Last Quarter: $312.80 (highest)
- Last Year: $282.91
- All Time: $219.71

**Interpretation**: Strong upward trend, with most recent quarter showing peak optimism. The all-time average is significantly lower, indicating substantial appreciation in expectations.

## Calculating Upside/Downside

### Basic Formula

```
Potential = (Target - Current Price) / Current Price × 100%
```

### Using Different Targets

| Target | Purpose |
|--------|---------|
| Average | Consensus expectation |
| High | Maximum upside |
| Low | Worst case |
| Median | Central tendency |

### Example Calculation

If AAPL trades at $270.01:

| Target | Potential |
|--------|-----------|
| $312.80 (Quarter Avg) | +15.8% upside |
| $305.72 (Month Avg) | +13.2% upside |
| $282.91 (Year Avg) | +4.8% upside |

## Evaluating Analyst Coverage

### Coverage Levels

| Analysts | Level | Reliability |
|----------|-------|-------------|
| 30+ | Heavy | High confidence |
| 15-30 | Good | Solid consensus |
| 5-15 | Moderate | Useful guidance |
| <5 | Light | Less reliable |

### Coverage Trends

| Change | Interpretation |
|--------|----------------|
| Increasing analysts | Growing interest |
| Decreasing analysts | Reduced coverage |
| Stable count | Maintained interest |

## Consensus Strength

### Indicators of Strong Consensus

| Factor | Strong | Weak |
|--------|--------|------|
| Range (high-low) | <20% spread | >50% spread |
| Analyst count | Many (30+) | Few (<5) |
| Recent revisions | Same direction | Mixed |
| Timeframe alignment | Consistent trend | Volatile |

### Range Analysis

If you have high and low targets:

```
Spread = (High - Low) / Average × 100%
```

| Spread | Interpretation |
|--------|----------------|
| <15% | Strong agreement |
| 15-30% | Normal range |
| 30-50% | Moderate disagreement |
| >50% | High uncertainty |

## Revision Analysis

### Reading Revision Trends

| Pattern | Signal |
|---------|--------|
| Upgrades > Downgrades | Improving sentiment |
| Downgrades > Upgrades | Deteriorating outlook |
| Balanced | Status quo |
| Surge of changes | New information |

### Catalyst Impact

| Event | Typical Response |
|-------|------------------|
| Beat earnings | Target increases |
| Miss earnings | Target decreases |
| Raised guidance | Upgrades |
| Lowered guidance | Downgrades |
| M&A news | Reassessment |

## Comparing to Current Price

### Position Analysis

| Position | Current vs. Target |
|----------|-------------------|
| Below all targets | Strong buy signal |
| Near low target | Cautious |
| Near average | Fair value |
| Near high target | Limited upside |
| Above all targets | Overvalued |

### Time Consideration

| Factor | Weight More |
|--------|-------------|
| Recent targets | Current view |
| Post-earnings | Updated info |
| Multiple revisions | Refined estimate |
| Senior analysts | Institutional view |

## Red Flags

### Warning Signs

1. **Few analysts** - Limited coverage, less reliable
2. **Wide range** - High disagreement
3. **Stale targets** - Old data, may be outdated
4. **Rapid downgrades** - Deteriorating outlook
5. **Price above all targets** - Potential overvaluation
6. **Declining coverage** - Reduced institutional interest

### Data Quality Issues

| Issue | Concern |
|-------|---------|
| Mixed sources | Different methodologies |
| Outdated targets | Pre-event data |
| Survivorship bias | Failed calls removed |
| Conflicts | Investment banking ties |

## Practical Application

### Investment Decision Framework

| Finding | Action |
|---------|--------|
| >20% upside, strong consensus | Consider buying |
| 10-20% upside, moderate consensus | Monitor |
| Near target | Fairly valued |
| Below targets | Potential concerns |

### Risk Adjustment

| Factor | Adjustment |
|--------|------------|
| Low coverage | Discount reliability |
| Wide range | Use median, not average |
| Stale data | Seek recent revisions |
| Sector volatility | Widen expected range |

## Next Steps After Analysis

### Additional Research

| Finding | Action |
|---------|--------|
| Strong upside | Verify with fundamentals |
| Recent upgrades | Check catalyst |
| Divergent targets | Understand bear/bull cases |
| Limited coverage | Find why |

### Related Skills

| Skill | Purpose |
|-------|---------|
| stock-quote | Current price comparison |
| analyst-estimates | Earnings expectations |
| income-statement | Fundamental check |
| stock-performance | Price trend context |
