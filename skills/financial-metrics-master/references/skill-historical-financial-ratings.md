# Skill: Historical Financial Ratings

## Purpose

Retrieve historical financial ratings and key metric scores over time including ROA, ROE, DCF, and debt-to-equity scores.

## When to Use

- Tracking rating evolution over time
- Identifying improvement or deterioration trends
- Long-term financial health assessment
- Historical pattern analysis

## Example Prompt

```
Retrieve historical financial ratings and key metric scores over time for NVDA, limited to 2000 records
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| Overall Score | Composite rating (1-5) |
| Overall Rating | Letter grade (A+ to F) |
| ROA Score | Return on assets efficiency |
| ROE Score | Return on equity efficiency |
| DCF Score | Discounted cash flow score |
| D/E Score | Debt-to-equity health |

## Integration with Other Skills

- **Extends**: financial-health-scores with historical view
- **Pairs with**: ratings-snapshot for current state
- **Supports**: Trend analysis in valuation

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Valuation | Rating trajectory for re-rating thesis |
| Investment Positives | Improving ratings story |
| Key Risks | Deteriorating ratings concern |

## Analysis Tips

- Consistent 5-star ratings = quality premium justified
- Improving trajectory = potential re-rating catalyst
- Recent downgrades = investigate cause

## Data Source

octagon-financials-agent
