# Skill: SEC Cash Flow Review

## Purpose

Extract and analyze cash flow trends and working capital changes.

## When to Use

- Liquidity assessment
- Free cash flow analysis
- Working capital efficiency
- Cash conversion evaluation

## Example Prompt

```
Extract and analyze cash flow trends and working capital changes from NFLX's latest 10-Q.
```

## Key Information Returned

| Section | Content |
|---------|---------|
| Operating Cash Flow | OCF and drivers |
| Investing Activities | CapEx, investments |
| Financing Activities | Debt, equity, dividends |
| Working Capital | Current asset/liability changes |

## Integration with Other Skills

- **Pairs with**: sec-debt-covenant for liquidity context
- **Feeds into**: Liquidity & Capital section
- **Validates**: Cash position and burn rate

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Liquidity & Capital | Primary source |
| Financial Analysis | Cash flow quality |
| Risk Assessment | Liquidity risk |

## Data Source

octagon-sec-agent, octagon-financials-agent, octagon-web-search-agent
