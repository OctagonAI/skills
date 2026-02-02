# Interpreting 10-K Analysis Results

## Reading the Output

The octagon-agent returns 10-K analysis with financial metrics, risk factors, and source citations:

**Example Output:**
- Total Revenues: $416.161 billion
- Net Income: $112.010 billion
- Total Assets: $359.241 billion
- Total Liabilities: $285.508 billion
- Operating Cash Flow: $111.482 billion
- Risk Factors: Macroeconomic, FX volatility, legal, supply chain, cybersecurity

## Understanding 10-K Sections

### Part I - Business Information

**Item 1 - Business**
- Company overview and history
- Products and services description
- Competitive landscape
- Seasonality and cyclicality
- Key customers and suppliers

**Item 1A - Risk Factors**
- Most critical section for investors
- Ranked roughly by materiality
- New risks = emerging concerns
- Removed risks = resolved issues

**Item 1B - Unresolved Staff Comments**
- SEC questions not yet resolved
- Rare but significant when present

### Part II - Financial Information

**Item 7 - MD&A**
- Management's perspective on results
- Discussion of trends and outlook
- Liquidity and capital resources
- Critical accounting policies

**Item 8 - Financial Statements**
- Audited annual financials
- Income statement
- Balance sheet
- Cash flow statement
- Notes to financials

## Analyzing Financial Metrics

### Revenue Analysis

| Metric | What to Look For |
|--------|------------------|
| Total Revenue | YoY growth rate |
| Revenue by Segment | Mix shift, concentration |
| Geographic Revenue | Regional exposure |
| Recurring vs One-time | Quality of revenue |

### Profitability Analysis

| Metric | What to Look For |
|--------|------------------|
| Gross Margin | Pricing power, cost control |
| Operating Margin | Operational efficiency |
| Net Margin | Bottom-line profitability |
| EPS Growth | Per-share performance |

### Balance Sheet Analysis

| Metric | What to Look For |
|--------|------------------|
| Total Assets | Asset base growth |
| Cash Position | Liquidity buffer |
| Total Debt | Leverage levels |
| Shareholders' Equity | Book value trend |

### Cash Flow Analysis

| Metric | What to Look For |
|--------|------------------|
| Operating CF | Core cash generation |
| CapEx | Investment intensity |
| Free Cash Flow | Cash available for shareholders |
| Financing CF | Debt/equity activity |

## Risk Factor Interpretation

### Severity Indicators

**High Priority Risks:**
- Listed first in Item 1A
- Extensive discussion (multiple paragraphs)
- Specific quantification of potential impact
- New additions from prior year

**Lower Priority Risks:**
- Listed later in section
- Boilerplate/generic language
- Unchanged from prior year
- No specific impact quantification

### Risk Categories

**Operational Risks**
- Supply chain disruptions
- Manufacturing issues
- Key personnel dependence
- Technology failures

**Financial Risks**
- Foreign exchange exposure
- Interest rate sensitivity
- Credit/counterparty risk
- Liquidity constraints

**Strategic Risks**
- Competition intensity
- Market disruption
- Regulatory changes
- Geopolitical factors

**Compliance Risks**
- Legal proceedings
- Regulatory investigations
- Environmental liabilities
- Tax exposure

## Comparing Filings

### Year-over-Year Analysis

When comparing 10-K filings:

1. **New Risk Factors**: What risks were added?
2. **Removed Risk Factors**: What risks were resolved?
3. **Changed Language**: How did risk descriptions evolve?
4. **Metric Changes**: How did financials change?

### Peer Comparison

Compare across competitors:
- Similar risk factors = industry-wide concerns
- Unique risk factors = company-specific issues
- Different financial metrics = competitive positioning

## Source Citations

The agent provides page references to the 10-K filing:

```
Sources:
1. Apple Inc. (10-K) - 2025-FY, Page: 33
2. Apple Inc. (10-K) - 2025-FY, Page: 40
...
```

Use these to:
- Verify extracted information
- Read additional context
- Access original tables/charts

## Red Flags

### Financial Red Flags
1. **Declining revenue with stable costs**: Margin pressure
2. **Cash flow < Net income**: Earnings quality concern
3. **Rising debt with flat EBITDA**: Leverage risk
4. **Negative working capital**: Liquidity stress

### Disclosure Red Flags
1. **Going concern language**: Viability questions
2. **Auditor qualification**: Financial statement issues
3. **Material weakness**: Internal control problems
4. **Significant related party transactions**: Governance concerns

### Risk Factor Red Flags
1. **Many new risk factors**: Emerging problems
2. **Litigation risk expansion**: Legal exposure
3. **Regulatory investigation mention**: Compliance issues
4. **Customer concentration increase**: Revenue risk

## Next Steps After Analysis

1. **Read 10-Q filings**: Get more recent quarterly updates
2. **Review earnings calls**: Management commentary on 10-K items
3. **Compare to peers**: Benchmark metrics and risks
4. **Check 8-K filings**: Material events since 10-K
5. **Analyze proxy (DEF 14A)**: Governance and compensation details
