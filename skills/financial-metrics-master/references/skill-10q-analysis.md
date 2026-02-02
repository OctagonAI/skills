# Skill: 10-Q Analysis

## Purpose

Analyze 10-Q quarterly filings for public companies to extract quarterly performance metrics, segment breakdown, and interim financial updates.

## When to Use

- Post-earnings deep dive into quarterly results
- Tracking sequential quarter trends
- Comparing quarterly actuals to estimates
- Monitoring segment performance changes
- Analyzing margin trends

## Example Prompt

```
Analyze the latest 10-Q filing for AAPL and extract quarterly performance metrics.
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| Total Revenue | Quarterly revenue with YoY comparison |
| Net Income | Quarterly profit |
| EPS (Basic/Diluted) | Earnings per share |
| Operating Income | Income from operations |
| Operating Margin | Quarterly margin |
| Segment Revenue | Breakdown by product/service |
| Cash Position | Balance sheet update |
| Source Citations | Page references to filing |

## Integration with Other Skills

- **Pairs with**: 10k-analysis for annual context
- **Complements**: analyst-estimates for expectation comparison
- **Supports**: Earnings analysis and trend tracking

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Estimates | Quarterly actual vs estimate |
| Investment Positives | Strong quarter performance |
| Key Risks | Margin compression, segment weakness |

## Data Source

octagon-financials-agent, octagon-sec-agent
