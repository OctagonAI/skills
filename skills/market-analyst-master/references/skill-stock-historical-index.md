# Stock Historical Index Skill

## Purpose

Retrieve full historical end-of-day price data for market indices (S&P 500, NASDAQ, etc.).

## When to Use

- Analyzing market trends
- Calculating alpha vs. benchmarks
- Understanding market context
- Risk-on/risk-off assessment

## Example Prompt

```
Retrieve full historical end-of-day price data for the ^GSPC index from 2025-01-01 to 2025-04-30.
```

## Key Information Returned

| Data Point | Description |
|------------|-------------|
| Date | Trading day |
| Open, High, Low, Close | OHLC data |
| Volume | Total volume |
| Change | Daily change |
| Change % | Percentage change |

## Common Index Symbols

| Symbol | Index |
|--------|-------|
| ^GSPC | S&P 500 |
| ^DJI | Dow Jones |
| ^IXIC | NASDAQ Composite |
| ^RUT | Russell 2000 |

## Integration with Other Skills

| Combine With | For |
|--------------|-----|
| stock-price-change | Alpha calculation |
| stock-performance | Stock vs. index |
| sector-performance-snapshot | Sector vs. market |

## Report Section Mapping

→ Market Context section
→ Index Performance table
