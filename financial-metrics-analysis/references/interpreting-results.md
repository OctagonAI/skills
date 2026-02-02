# Interpreting Financial Metrics Results

## Reading the Output Table

The octagon-agent returns YoY growth data in tabular format:

| Year | Revenue Growth | Cost of Revenue Growth | Gross Profit Growth | Operating Income Growth | Net Income Growth |
|------|----------------|------------------------|---------------------|-------------------------|-------------------|
| 2024 | 2.0%           | 1.5%                   | 3.1%                | 5.2%                    | 4.8%              |
| 2023 | -2.8%          | -1.2%                  | -4.5%               | -8.1%                   | -10.2%            |

**Positive percentages** = Growth compared to prior year
**Negative percentages** = Decline compared to prior year

## Key Patterns to Identify

### 1. Operating Leverage (Positive Signal)

When Operating Income Growth > Revenue Growth:
- Fixed costs spread over larger revenue base
- Scalable business model
- Example: Revenue +5%, Operating Income +12%

### 2. Margin Expansion (Positive Signal)

When Gross Profit Growth > Revenue Growth:
- Pricing power or cost efficiencies
- Strong competitive position
- Example: Revenue +3%, Gross Profit +6%

### 3. Margin Compression (Warning Signal)

When Cost of Revenue Growth > Revenue Growth:
- Rising input costs not passed to customers
- Competitive pressure on pricing
- Example: Revenue +2%, Cost of Revenue +5%

### 4. Profitability Acceleration (Strong Signal)

When Net Income Growth > Operating Income Growth > Revenue Growth:
- All metrics improving simultaneously
- Indicates strong execution
- Example: Revenue +4%, Operating +8%, Net Income +12%

### 5. Revenue Deceleration (Watch Signal)

When Revenue Growth is declining year-over-year:
- 2024: +10%, 2023: +15%, 2022: +22%
- May indicate market saturation
- Compare to industry growth rates

## Trend Analysis Framework

### Multi-Year Consistency

Look for companies with:
- 3+ consecutive years of positive Revenue Growth
- Stable or improving Operating Income Growth
- Net Income Growth matching or exceeding Revenue Growth

### Inflection Points

Identify when metrics switch from negative to positive:
- Signals potential turnaround
- Confirm with qualitative analysis (earnings calls, management commentary)

### Cyclical vs Structural

Distinguish between:
- **Cyclical decline**: Industry-wide, temporary
- **Structural decline**: Company-specific, potentially permanent

## Comparative Analysis

### Peer Comparison

Request peer data using additional queries:
```
Retrieve year-over-year growth in key income-statement items for <PEER_TICKER>, limited to 5 records and filtered by period FY.
```

Compare:
- Is Revenue Growth above or below peers?
- Are margins expanding faster than competitors?
- Is Net Income Growth outpacing the sector?

### Industry Benchmarks

General benchmarks by sector:

| Sector | Typical Revenue Growth | Typical Net Income Growth |
|--------|------------------------|---------------------------|
| Tech   | 10-20%                 | 15-25%                    |
| Consumer Staples | 2-5%        | 3-8%                      |
| Financials | 5-10%             | 8-15%                     |
| Healthcare | 5-12%             | 8-18%                     |

## Red Flags

1. **Revenue declining, Net Income rising**: Unsustainable cost cuts
2. **All metrics negative for 2+ years**: Structural issues
3. **Volatile swings**: Inconsistent execution or accounting concerns
4. **Gross Profit growing slower than Cost of Revenue**: Pricing power erosion

## Next Steps After Analysis

1. **Deep dive on outliers**: Use octagon-agent to query earnings call transcripts for explanation
2. **Validate with filings**: Request 10-K/10-Q analysis for context
3. **Peer comparison**: Run same analysis on 2-3 direct competitors
4. **Forward estimates**: Query for analyst estimates and guidance
