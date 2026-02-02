# Skill: ESG Benchmark Comparison

## Purpose

Retrieve ESG benchmark comparison metrics by sector using MSCI, S&P, CDP, and other frameworks.

## When to Use

- Contextualizing company ESG vs sector
- Identifying ESG leaders/laggards by industry
- Setting ESG investment thresholds
- Regulatory framework alignment

## Example Prompt

```
Retrieve ESG benchmark comparison metrics by sector for the fiscal year 2024
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| Sector Average | ESG score by sector |
| Top Quartile Threshold | Leader threshold |
| Bottom Quartile Threshold | Laggard threshold |
| Framework Sources | MSCI, S&P, CDP, etc. |
| Regional Variations | EU vs US vs APAC |

## Integration with Other Skills

- **Pairs with**: esg-ratings for company-specific scores
- **Contextualizes**: Company ESG relative to peers
- **Supports**: Sector allocation decisions

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| ESG Assessment | Sector comparison |
| Peer Analysis | ESG positioning vs competitors |
| Investment Thesis | ESG differentiation |

## Analysis Tips

- Sector context critical (60 = good in Energy, average in Tech)
- EU benchmarks typically higher than US
- Material ESG factors vary by sector

## Data Source

octagon-companies-agent, octagon-web-search-agent
