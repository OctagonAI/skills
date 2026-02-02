# Skill: Ratings Snapshot

## Purpose

Retrieve current financial ratings overview for quick assessment of a company's financial position.

## When to Use

- Quick initial screening
- Current state assessment before deep dive
- Executive summary preparation
- Rapid comparison across companies

## Example Prompt

```
Retrieve current financial ratings snapshot for AAPL
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| Overall Rating | Current letter grade |
| Overall Score | Current composite score |
| Key Metric Scores | Current ROA, ROE, etc. |
| Rating Date | As-of date for ratings |

## Integration with Other Skills

- **Starting point for**: Comprehensive analysis
- **Pairs with**: historical-financial-ratings for context
- **Validates**: financial-health-scores

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Executive Summary | Quick rating reference |
| Factor Profile | Rating component |
| Investment Thesis | Quality positioning |

## Analysis Tips

- Use as first skill in analysis workflow
- Compare snapshot to historical for trend
- Cross-reference with peer snapshots

## Data Source

octagon-financials-agent
