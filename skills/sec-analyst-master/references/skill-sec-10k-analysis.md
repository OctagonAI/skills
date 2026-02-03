# Skill: SEC 10-K Analysis

## Purpose

Analyze 10-K annual filings to extract key financial metrics, risk factors, and business insights.

## When to Use

- Starting comprehensive company analysis
- Annual review of company disclosures
- Understanding business model and strategy
- Baseline for year-over-year comparison

## Example Prompt

```
Analyze the latest 10-K filing for AAPL and extract key financial metrics and risk factors.
```

## Key Information Returned

| Section | Content |
|---------|---------|
| Financial Metrics | Revenue, net income, assets, liabilities |
| Risk Factors | Item 1A risk disclosures |
| Business Description | Item 1 company overview |
| MD&A Highlights | Item 7 key points |

## Integration with Other Skills

- **Pairs with**: sec-10q-analysis for quarterly updates
- **Feeds into**: sec-annual-comparison for YoY analysis
- **Validates**: Financial metrics skills with SEC data

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Executive Summary | Company overview |
| Business Overview | Item 1 extraction |
| Financial Analysis | Core metrics |
| Appendix | Detailed disclosure |

## Data Source

octagon-sec-agent, octagon-financials-agent
