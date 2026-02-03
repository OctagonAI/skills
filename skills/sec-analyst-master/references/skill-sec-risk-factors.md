# Skill: SEC Risk Factors

## Purpose

Extract and summarize risk factors from SEC filings with categorization.

## When to Use

- Risk assessment in due diligence
- Understanding company's disclosed concerns
- Tracking risk evolution over time
- Comparing risk profiles across peers

## Example Prompt

```
Extract and summarize the risk factors section from AAPL's latest annual report.
```

## Key Information Returned

| Section | Content |
|---------|---------|
| Risk Categories | Business, financial, operational, etc. |
| Risk Descriptions | Summary of each risk |
| Source Pages | Filing page references |
| Priority | Order indicates materiality |

## Integration with Other Skills

- **Pairs with**: sec-annual-comparison for YoY risk changes
- **Feeds into**: Risk Factor Analysis section
- **Validates**: Investment risks with official disclosures

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Risk Factor Analysis | Primary source |
| Executive Summary | Key risks |
| Material Concerns | High priority risks |

## Data Source

octagon-sec-agent
