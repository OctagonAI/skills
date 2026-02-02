# Interpreting Financial Health Scores

## Altman Z-Score

### Overview
Developed by Edward Altman in 1968 to predict bankruptcy probability within 2 years.

### Interpretation Guide

| Z-Score | Zone | Probability | Action |
|---------|------|-------------|--------|
| > 3.0 | Safe | Very low bankruptcy risk | Standard investment analysis |
| 2.7 - 3.0 | Caution | Low risk but monitor | Watch for deterioration |
| 1.8 - 2.7 | Grey | Moderate risk | Deep dive required |
| < 1.8 | Distress | High bankruptcy risk | Avoid or distressed investing |

### Formula Components

```
Z = 1.2×A + 1.4×B + 3.3×C + 0.6×D + 1.0×E
```

| Component | Formula | What It Measures |
|-----------|---------|------------------|
| A | Working Capital / Total Assets | Liquidity |
| B | Retained Earnings / Total Assets | Cumulative profitability |
| C | EBIT / Total Assets | Operating efficiency |
| D | Market Cap / Total Liabilities | Market confidence |
| E | Revenue / Total Assets | Asset utilization |

### Limitations
- Designed for manufacturing companies
- Less reliable for financials, utilities
- Market cap component adds volatility
- May miss rapid deterioration

## Piotroski F-Score

### Overview
Developed by Joseph Piotroski in 2000 for value stock screening.

### Interpretation Guide

| Score | Quality | Interpretation |
|-------|---------|----------------|
| 8-9 | Strong | High-quality value candidate |
| 6-7 | Moderate | Acceptable, monitor closely |
| 4-5 | Weak | Potential value trap |
| 0-3 | Poor | Avoid, serious concerns |

### Nine Criteria (1 point each)

**Profitability (4 points):**

| # | Criterion | Pass Condition |
|---|-----------|----------------|
| 1 | Net Income | Positive current year |
| 2 | Operating Cash Flow | Positive current year |
| 3 | Return on Assets | Higher than prior year |
| 4 | Accruals Quality | OCF > Net Income |

**Leverage & Liquidity (3 points):**

| # | Criterion | Pass Condition |
|---|-----------|----------------|
| 5 | Long-term Debt | Lower ratio than prior year |
| 6 | Current Ratio | Higher than prior year |
| 7 | Share Dilution | No new shares issued |

**Operating Efficiency (2 points):**

| # | Criterion | Pass Condition |
|---|-----------|----------------|
| 8 | Gross Margin | Higher than prior year |
| 9 | Asset Turnover | Higher than prior year |

### Use Case
Best for:
- High book-to-market (value) stocks
- Screening within value universe
- Avoiding value traps

## Combined Analysis

### Matrix Approach

| | High Piotroski (7+) | Low Piotroski (<5) |
|---|---|---|
| **High Z-Score (>3)** | Strong Buy consideration | Monitor operating trends |
| **Low Z-Score (<1.8)** | Leverage concern, investigate | Avoid or distressed only |

### Investment Implications

**Strong Health (Z>3, P>7):**
- Low risk profile
- Quality company
- May command premium valuation

**Mixed Signals:**
- Dig deeper into specific weaknesses
- Understand trend direction
- Compare to industry norms

**Weak Health (Z<2, P<5):**
- High risk profile
- Potential value trap
- Only for distressed specialists

## Follow-up Analysis

```
Break down the individual 9 components of TSLA's Piotroski Score
```

```
Track TSLA's Altman Z-Score over the last 5 years
```

```
Compare TSLA's financial health scores to F and GM
```
