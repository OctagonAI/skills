# Stock Price Change Skill

## Purpose

Retrieve price change statistics across multiple time periods from 1 day to 10 years.

## When to Use

- Analyzing short-term vs. long-term performance
- Evaluating momentum and trend consistency
- Comparing returns across timeframes
- Calculating alpha vs. benchmarks

## Example Prompt

```
Get stock price change statistics for the symbol AAPL.
```

## Key Information Returned

| Period | Description |
|--------|-------------|
| 1 Day | Daily return |
| 5 Days | Weekly return |
| 1 Month | Monthly return |
| 3 Months | Quarterly return |
| 6 Months | Half-year return |
| YTD | Year-to-date return |
| 1 Year | Annual return |
| 3 Years | 3-year cumulative |
| 5 Years | 5-year cumulative |
| 10 Years | 10-year cumulative |
| All-Time High | Return from inception |

## Integration with Other Skills

| Combine With | For |
|--------------|-----|
| stock-historical-index | Alpha calculation |
| stock-quote | Current price context |
| batch-market-cap | Peer comparison |

## Report Section Mapping

→ Price Performance section
→ Multi-Period Returns table
