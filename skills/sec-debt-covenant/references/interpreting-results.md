# Interpreting Debt Covenant Results

## Reading the Output

The octagon-agent returns structured debt covenant analysis with source citations:

**Debt Overview:**
- Total debt amounts
- Facility types and sizes
- Maturity information

**Covenant Details:**
- Financial covenant types
- Threshold requirements
- Current compliance status

## Understanding Covenant Types

### Maintenance vs. Incurrence

| Type | Tested | Purpose |
|------|--------|---------|
| Maintenance | Ongoing (quarterly) | Must always comply |
| Incurrence | When taking action | Only tested on debt/dividend |
| Springing | When triggered | Becomes maintenance if drawn |

### Financial Covenants

| Covenant | Typical Structure |
|----------|-------------------|
| Leverage | Debt/EBITDA ≤ X.Xx |
| Interest Coverage | EBITDA/Interest ≥ X.Xx |
| Fixed Charge | (EBITDA-CapEx)/Fixed Charges ≥ X.Xx |
| Net Worth | Minimum equity level |
| Liquidity | Minimum cash/availability |

### Negative Covenants

| Covenant | Restriction |
|----------|-------------|
| Debt | Limits additional borrowing |
| Liens | Limits secured debt |
| Investments | Limits acquisitions |
| Restricted Payments | Limits dividends |
| Asset Sales | Limits divestitures |

## Evaluating Covenant Cushion

### Cushion Calculation

For leverage covenant:
- Covenant: Debt/EBITDA ≤ 4.0x
- Actual: 3.2x
- Cushion: (4.0 - 3.2) / 4.0 = 20%

### Cushion Assessment

| Cushion | Risk Level | Action |
|---------|------------|--------|
| >30% | Low | Monitor routinely |
| 20-30% | Moderate | Watch closely |
| 10-20% | Elevated | Active monitoring |
| <10% | High | Prepare remediation |

### Stress Testing

| Scenario | EBITDA Impact | New Ratio | Cushion |
|----------|---------------|-----------|---------|
| Base | $0 | X.Xx | Y% |
| -10% EBITDA | -$XM | X.Xx | Y% |
| -20% EBITDA | -$XM | X.Xx | Y% |
| -30% EBITDA | -$XM | X.Xx | Breach |

## Analyzing Credit Facility Terms

### Key Terms to Evaluate

| Term | What to Assess |
|------|----------------|
| Size | Adequate for needs |
| Maturity | Sufficient runway |
| Pricing | Market competitive |
| Covenants | Manageable restrictions |
| Flexibility | Operational room |

### Pricing Grid Analysis

| Leverage | Spread (bps) |
|----------|--------------|
| <2.0x | 150 |
| 2.0-2.5x | 175 |
| 2.5-3.0x | 200 |
| 3.0-3.5x | 225 |
| >3.5x | 250 |

### Revolver Availability

| Component | Amount |
|-----------|--------|
| Commitment | $XM |
| Less: Outstanding | ($YM) |
| Less: Letters of Credit | ($ZM) |
| Available | $WM |

## EBITDA Adjustments

### Common Add-Backs

| Adjustment | What It Is |
|------------|------------|
| One-time charges | Restructuring, severance |
| Stock compensation | Non-cash expense |
| Acquisition costs | Transaction expenses |
| Synergies | Expected savings |
| Pro forma | Full-year acquisitions |

### Adjustment Scrutiny

| Red Flag | Concern |
|----------|---------|
| Large add-backs | EBITDA inflated |
| Growing add-backs | Recurring "one-time" |
| Vague descriptions | Lack of transparency |
| Synergy assumptions | Unproven savings |
| Pro forma estimates | Execution risk |

## Maturity Analysis

### Maturity Profile Assessment

| Profile | Risk Level |
|---------|------------|
| Well-laddered | Low |
| Concentrated | Higher |
| Near-term wall | Elevated |
| Long-dated | Lower |

### Refinancing Considerations

| Factor | Positive | Negative |
|--------|----------|----------|
| Market Access | Investment grade | High yield, stressed |
| Maturities | Far-dated | Near-term |
| Rate Environment | Favorable | Rising rates |
| Credit Trend | Improving | Deteriorating |

## Covenant Violation Assessment

### Violation Consequences

| Consequence | Impact |
|-------------|--------|
| Event of Default | Acceleration possible |
| Cross-Default | Triggers other debt |
| Increased Pricing | Higher interest |
| Restricted Actions | No dividends, etc. |

### Cure Options

| Option | Description |
|--------|-------------|
| Equity Cure | Inject equity |
| Asset Sale | Reduce debt |
| Amendment | Change covenant |
| Waiver | Temporary relief |
| Refinancing | Replace facility |

### Cure Costs

| Cost Type | Impact |
|-----------|--------|
| Amendment Fee | 0.25-0.50% typical |
| Increased Spread | 25-50+ bps |
| Tighter Terms | Less flexibility |
| Equity Dilution | If cure required |

## Red Flags Summary

### Covenant Red Flags

1. **Minimal cushion** - <10% headroom
2. **Covenant holiday** - Testing suspended
3. **Frequent amendments** - Ongoing stress
4. **Large EBITDA add-backs** - Inflated metrics
5. **Downward trend** - Deteriorating ratios

### Liquidity Red Flags

1. **High utilization** - Revolver >80% drawn
2. **Near-term maturities** - Wall approaching
3. **Negative FCF** - Cash burning
4. **Declining EBITDA** - Coverage weakening
5. **Rating downgrades** - Access impacted

### Documentation Red Flags

1. **Vague disclosure** - Limited detail
2. **Missing exhibits** - No filed agreements
3. **Changed definitions** - EBITDA redefined
4. **Affiliate transactions** - Related party debt
5. **Going concern** - Auditor warning

## Cross-Default Analysis

### Cross-Default Triggers

| Trigger | What Happens |
|---------|--------------|
| Payment Default | Miss principal/interest |
| Covenant Default | Breach financial test |
| Acceleration | Debt called due |
| Bankruptcy | Insolvency filing |

### Cross-Default Assessment

| Factor | What to Check |
|--------|---------------|
| Threshold | Minimum amount to trigger |
| Cure Period | Time to remedy |
| Waiver Obtained | From other lenders |
| Cascade Risk | Which debt affected |

## Using Results for Analysis

### Credit Implications

| Finding | Credit Impact |
|---------|---------------|
| Ample cushion | Lower risk |
| Tight cushion | Elevated risk |
| Covenant breach | Distressed |
| Amendment | Watch closely |

### Investment Implications

| Finding | Implication |
|---------|-------------|
| Strong compliance | Financial flexibility |
| Tight covenants | Limited room |
| Breach risk | Equity at risk |
| Cure needed | Dilution possible |

## Next Steps After Analysis

1. **Calculate cushion**: Run sensitivity scenarios
2. **Read agreements**: Review filed exhibits
3. **Track amendments**: Monitor changes
4. **Check ratings**: Agency covenant analysis
5. **Model scenarios**: Stress test compliance
6. **Monitor quarterly**: Track trends
