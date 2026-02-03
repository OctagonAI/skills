# Skill: SEC 10-Q Analysis

## Purpose

Analyze 10-Q quarterly filings to extract quarterly performance metrics and segment breakdown.

## When to Use

- Quarterly earnings analysis
- Interim period updates
- Tracking intra-year trends
- Identifying emerging issues

## Example Prompt

```
Analyze the latest 10-Q filing for AAPL and extract quarterly performance metrics.
```

## Key Information Returned

| Section | Content |
|---------|---------|
| Quarterly Financials | Revenue, income, EPS for quarter |
| Segment Performance | Quarterly segment breakdown |
| MD&A Updates | Management commentary on quarter |
| Liquidity | Cash position updates |

## Integration with Other Skills

- **Pairs with**: sec-10k-analysis for annual context
- **Feeds into**: sec-cash-flow-review for liquidity trends
- **Validates**: Quarterly earnings announcements

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Financial Analysis | Quarterly metrics |
| Liquidity & Capital | Cash position updates |
| Material Events | Quarter developments |

## Data Source

octagon-sec-agent, octagon-financials-agent
