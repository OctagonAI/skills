# Skill: Analyst Estimates

## Purpose

Retrieve analyst revenue and EPS estimates with consensus ranges for public companies.

## When to Use

- Gauging market expectations
- Identifying estimate momentum
- Comparing company guidance to consensus
- Setting up valuation multiples

## Example Prompt

```
Retrieve analyst Revenue and EPS estimates with consensus ranges for NVDA
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| Revenue Estimate | Consensus revenue forecast |
| EPS Estimate | Consensus EPS forecast |
| High/Low Range | Estimate dispersion |
| Number of Analysts | Coverage breadth |
| Revision Trend | Recent estimate changes |

## Integration with Other Skills

- **Validates against**: income-statement actual results
- **Supports**: Valuation with forward multiples
- **Pairs with**: financial-growth for estimate reasonability

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Executive Summary | Consensus expectations |
| Estimates | Model anchoring |
| Valuation | Forward P/E, EV/EBITDA inputs |

## Analysis Tips

- Estimate revisions up = positive momentum
- Wide high/low range = uncertainty
- Beats/misses vs consensus drive stock moves

## Data Source

octagon-financials-agent
