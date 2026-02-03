# SEC Filing Analysis Workflow Overview

This document outlines the end-to-end workflow for conducting comprehensive SEC filing analysis using all Octagon SEC skills.

## Workflow Diagram

```
Phase 1: Filing Inventory
    ├── 10-K Annual Report
    ├── 10-Q Quarterly Reports
    ├── 8-K Current Reports
    └── Amendments Review
           │
           ▼
Phase 2: Core Business Analysis
    ├── Business Description
    ├── MD&A Analysis
    └── Segment Reporting
           │
           ▼
Phase 3: Risk Assessment
    ├── Risk Factor Extraction
    ├── YoY Risk Comparison
    └── Risk Categorization
           │
           ▼
Phase 4: Financial Deep Dive
    ├── Footnotes & Policies
    ├── Debt & Covenants
    └── Cash Flow Analysis
           │
           ▼
Phase 5: Governance Review
    ├── Proxy Analysis
    ├── Board Composition
    └── Related Parties
           │
           ▼
Phase 6: Comparative Analysis
    ├── Annual Comparison
    └── Peer Filing Review
           │
           ▼
Phase 7: Report Generation
    └── Due Diligence Report
```

## Phase 1: Filing Inventory

**Objective**: Identify and analyze all relevant SEC filings.

**Skills Used**:
- sec-10k-analysis
- sec-10q-analysis
- sec-8k-analysis
- sec-amendments-review

**Queries**:
```
Analyze the latest 10-K filing for <TICKER>
Analyze the latest 10-Q filing for <TICKER>
Analyze recent 8-K filings for <TICKER>
Review recent amendments to SEC filings for <TICKER>
```

**Output**: Complete filing inventory, key metrics from each filing, material events.

**Time**: 15-20 minutes

---

## Phase 2: Core Business Analysis

**Objective**: Understand the business model and strategic direction.

**Skills Used**:
- sec-business-desc-analysis
- sec-mda-analysis
- sec-segment-reporting

**Queries**:
```
Extract business description and competitive landscape from <TICKER>'s latest 10-K
Analyze the MD&A section from <TICKER>'s latest filing
Analyze business segment performance from <TICKER>'s latest filing
```

**Output**: Business overview, competitive positioning, segment performance, strategic priorities.

**Key Analysis**:
- Business model clarity
- Competitive advantages
- Segment health
- Strategic direction

**Time**: 15-20 minutes

---

## Phase 3: Risk Assessment

**Objective**: Comprehensive risk factor analysis and evolution.

**Skills Used**:
- sec-risk-factors
- sec-annual-comparison

**Queries**:
```
Extract and summarize risk factors from <TICKER>'s latest 10-K
Compare risk factors between current and prior year 10-K for <TICKER>
```

**Output**: Categorized risks, new vs. existing risks, risk severity assessment.

**Key Analysis**:
- Risk prioritization (order matters)
- New/emerging risks
- Removed risks (resolved?)
- Language changes (escalation/de-escalation)

**Time**: 15-20 minutes

---

## Phase 4: Financial Deep Dive

**Objective**: Detailed financial disclosure and accounting analysis.

**Skills Used**:
- sec-footnotes-analysis
- sec-debt-covenant
- sec-cash-flow-review

**Queries**:
```
Analyze footnotes and accounting policies from <TICKER>'s latest filing
Analyze debt covenants and credit agreement terms for <TICKER>
Extract cash flow trends and working capital changes for <TICKER>
```

**Output**: Accounting policies, critical estimates, covenant status, liquidity position.

**Key Analysis**:
- Revenue recognition policies
- Critical accounting estimates
- Debt maturity and covenants
- Working capital trends
- Off-balance sheet items

**Time**: 20-25 minutes

---

## Phase 5: Governance Review

**Objective**: Assess governance quality and compensation practices.

**Skills Used**:
- sec-proxy-analysis
- sec-corp-governance

**Queries**:
```
Extract executive compensation from <TICKER>'s latest proxy statement
Review corporate governance practices and board composition for <TICKER>
```

**Output**: Board composition, compensation details, governance policies, related parties.

**Key Analysis**:
- Board independence
- Pay-for-performance alignment
- Shareholder rights
- Related party transactions

**Time**: 15-20 minutes

---

## Phase 6: Comparative Analysis

**Objective**: Year-over-year and peer comparison.

**Skills Used**:
- sec-annual-comparison
- All skills applied to peers

**Queries**:
```
Compare key metrics between <TICKER>'s current and prior year 10-K
Repeat key analyses for peer companies
```

**Output**: YoY changes, peer comparisons, relative positioning.

**Key Analysis**:
- Metric evolution
- Disclosure changes
- Risk factor evolution
- Governance comparison

**Time**: 25-35 minutes

---

## Phase 7: Report Generation

**Objective**: Synthesize findings into comprehensive due diligence report.

**Template**: See [report-template.md](report-template.md)

**Sections**:
1. Executive Summary
2. Business Overview
3. Risk Factor Analysis
4. Financial Statement Analysis
5. Liquidity & Capital Resources
6. Governance Assessment
7. Material Events
8. Year-over-Year Comparison
9. IPO/Registration Analysis (if applicable)
10. Appendix

**Time**: 45-60 minutes

---

## Total Workflow Time

| Phase | Time Estimate |
|-------|---------------|
| Phase 1: Filing Inventory | 15-20 min |
| Phase 2: Business Analysis | 15-20 min |
| Phase 3: Risk Assessment | 15-20 min |
| Phase 4: Financial Deep Dive | 20-25 min |
| Phase 5: Governance Review | 15-20 min |
| Phase 6: Comparative Analysis | 25-35 min |
| Phase 7: Report Generation | 45-60 min |
| **Total** | **150-200 min** |

---

## Skill-to-Report Section Mapping

| Report Section | Primary Skills | Secondary Skills |
|----------------|----------------|------------------|
| Executive Summary | sec-10k-analysis | sec-business-desc-analysis |
| Business Overview | sec-business-desc-analysis, sec-segment-reporting | sec-mda-analysis |
| Risk Factor Analysis | sec-risk-factors | sec-annual-comparison |
| Financial Statement Analysis | sec-footnotes-analysis, sec-10k-analysis | sec-10q-analysis |
| Liquidity & Capital | sec-cash-flow-review, sec-debt-covenant | sec-10q-analysis |
| Governance Assessment | sec-proxy-analysis, sec-corp-governance | - |
| Material Events | sec-8k-analysis | sec-amendments-review |
| YoY Comparison | sec-annual-comparison | All filing skills |
| IPO Analysis | sec-s1-analysis | - |
| Appendix | All skills | - |

---

## Best Practices

1. **Start with 10-K**: The annual report provides the most comprehensive disclosure.

2. **Check 8-Ks for updates**: Material events between periodic filings.

3. **Read risks first**: Sets priorities for deeper analysis.

4. **Cross-reference MD&A**: Management commentary should align with financials.

5. **Track amendments**: Corrections or restatements signal issues.

6. **Document citations**: Every finding needs filing, date, and page reference.

7. **Peer comparison**: Context matters for evaluating disclosures.
