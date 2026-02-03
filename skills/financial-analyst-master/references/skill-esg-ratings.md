# Skill: ESG Ratings

## Purpose

Retrieve ESG ratings and scores including MSCI ratings, Sustainalytics risk ratings, and industry rank for public companies.

## When to Use

- ESG due diligence
- Sustainability assessment
- ESG-focused investment screening
- Regulatory and reputational risk analysis

## Example Prompt

```
Retrieve ESG ratings and scores, including risk rating and industry rank, for MSFT
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| MSCI ESG Rating | AAA to CCC scale |
| Sustainalytics Risk | 0-100 risk score |
| ESG Score | Composite sustainability score |
| Environmental Score | E component |
| Social Score | S component |
| Governance Score | G component |
| Industry Rank | Position vs sector peers |

## Integration with Other Skills

- **Pairs with**: esg-benchmark-comparison for context
- **Supports**: Risk section of report
- **Complements**: financial-health-scores for full picture

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| ESG Assessment | Primary ESG analysis |
| Key Risks | ESG-related risks |
| Investment Thesis | ESG as differentiator |

## Analysis Tips

- AAA/AA = ESG leader, potential premium
- High Sustainalytics risk = ESG laggard
- Component imbalance warrants investigation

## Data Source

octagon-companies-agent, octagon-financials-agent, octagon-web-search-agent
