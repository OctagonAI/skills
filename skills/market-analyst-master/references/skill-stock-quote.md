# Stock Quote Skill

## Purpose

Retrieve real-time stock quotes with current price, volume, day range, 52-week range, and moving averages.

## When to Use

- Getting current trading data
- Checking price vs. moving averages
- Analyzing day range position
- Evaluating 52-week range position

## Example Prompt

```
Get real-time stock quote for the symbol AAPL.
```

## Key Information Returned

| Data Point | Description |
|------------|-------------|
| Current Price | Last traded price |
| Change | Dollar and percent change |
| Volume | Shares traded today |
| Day Range | Low - High today |
| 52-Week Range | Annual low - high |
| 50-Day MA | Short-term average |
| 200-Day MA | Long-term average |
| Market Cap | Current valuation |

## Integration with Other Skills

| Combine With | For |
|--------------|-----|
| price-target-consensus | Price vs. target |
| sector-pe-ratios | Valuation context |
| company-market-cap | Detailed valuation |

## Report Section Mapping

→ Stock Snapshot section
→ Technical Position analysis
