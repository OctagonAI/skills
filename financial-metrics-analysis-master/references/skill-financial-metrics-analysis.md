# Skill: Financial Metrics Analysis

## Purpose

Analyze year-over-year growth in income statement items including revenue, COGS, gross profit, operating income, and net income.

## When to Use

- Identifying growth trends and inflection points
- Detecting operating leverage
- Comparing growth across metrics
- Building investment thesis with quantitative support

## Example Prompt

```
Retrieve year-over-year growth in key income-statement items for AAPL, limited to 5 records and filtered by period FY
```

## Key Metrics Returned

| Metric | Description |
|--------|-------------|
| Revenue Growth | YoY change in revenue |
| Cost of Revenue Growth | YoY change in COGS |
| Gross Profit Growth | YoY change in gross profit |
| Operating Income Growth | YoY change in operating income |
| Net Income Growth | YoY change in net income |

## Integration with Other Skills

- **Builds on**: income-statement current data
- **Complements**: income-statement-growth, financial-growth
- **Supports**: Investment thesis quantification

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Investment Positives | Growth acceleration evidence |
| Investment Thesis | Quantitative support |
| Peer Analysis | Comparative growth rates |

## Key Patterns

- **Operating leverage**: Op Income Growth > Revenue Growth
- **Margin expansion**: Gross Profit Growth > Revenue Growth
- **Margin compression**: COGS Growth > Revenue Growth

## Data Source

octagon-financials-agent
