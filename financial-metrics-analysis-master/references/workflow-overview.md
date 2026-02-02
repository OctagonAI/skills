# Equity Research Workflow Overview

This document outlines the end-to-end workflow for conducting comprehensive financial analysis using all Octagon skills.

## Workflow Diagram

```
Phase 1: Data Collection
    ├── Income Statement
    ├── Balance Sheet
    ├── Cash Flow Statement
    └── Current Ratings
           │
           ▼
Phase 2: Growth & Trend Analysis
    ├── YoY Income Growth
    ├── Balance Sheet Growth
    ├── Cash Flow Growth
    └── Historical Ratings
           │
           ▼
Phase 3: Segmentation
    ├── Product Segments
    └── Geographic Segments
           │
           ▼
Phase 4: Forward Estimates
    ├── Analyst Estimates
    └── Financial Health Scores
           │
           ▼
Phase 5: ESG Assessment
    ├── ESG Ratings
    └── Sector Benchmarks
           │
           ▼
Phase 6: Peer Comparison
    └── Repeat Phases 1-5 for peers
           │
           ▼
Phase 7: Report Generation
    └── Synthesize into IC Report
```

## Phase 1: Data Collection

**Objective**: Gather current financial snapshot of the company.

**Skills Used**:
- income-statement
- balance-sheet
- cash-flow-statement
- ratings-snapshot

**Queries**:
```
Retrieve real-time income statement data for <TICKER>
Retrieve detailed balance sheet data for <TICKER>
Retrieve cash flow statement data for <TICKER>
Retrieve current financial ratings snapshot for <TICKER>
```

**Output**: Current financial position including revenue, profitability, assets, liabilities, cash flows, and ratings.

**Time**: 5-10 minutes

---

## Phase 2: Growth & Trend Analysis

**Objective**: Understand historical performance and trajectory.

**Skills Used**:
- financial-metrics-analysis
- income-statement-growth
- balance-sheet-growth
- cash-flow-growth
- financial-growth
- historical-financial-ratings

**Queries**:
```
Retrieve year-over-year growth in key income-statement items for <TICKER>, limited to 5 records and filtered by period FY
Retrieve YoY growth in Total Assets, Liabilities, Equity, Cash for <TICKER>
Retrieve YoY growth in Operating Cash Flow, Free Cash Flow for <TICKER>
Retrieve historical financial ratings for <TICKER>, limited to 2000 records
```

**Output**: Multi-year growth trends, margin evolution, rating trajectory.

**Key Analysis**:
- Revenue growth acceleration/deceleration
- Margin expansion/compression
- Operating leverage signals
- Rating improvements/deteriorations

**Time**: 10-15 minutes

---

## Phase 3: Segmentation Analysis

**Objective**: Understand business mix and geographic exposure.

**Skills Used**:
- revenue-product-segmentation
- revenue-geographic-segmentation

**Queries**:
```
Retrieve revenue breakdown by product segment for <TICKER>
Retrieve revenue breakdown by geographic segment for <TICKER>
```

**Output**: Product mix, segment growth rates, geographic concentration, regional trends.

**Key Analysis**:
- Revenue concentration risk
- High-growth vs mature segments
- Geographic diversification
- Currency exposure implications

**Time**: 5-10 minutes

---

## Phase 4: Forward Estimates & Financial Health

**Objective**: Assess forward expectations and financial stability.

**Skills Used**:
- analyst-estimates
- financial-health-scores

**Queries**:
```
Retrieve analyst Revenue and EPS estimates with consensus ranges for <TICKER>
Retrieve Altman Z-Score and Piotroski Score for <TICKER>
```

**Output**: Consensus estimates, estimate revisions, financial health indicators.

**Key Analysis**:
- Estimate momentum (revisions up/down)
- Consensus vs company guidance
- Bankruptcy risk (Z-Score)
- Financial strength (Piotroski)

**Time**: 5-10 minutes

---

## Phase 5: ESG Assessment

**Objective**: Evaluate sustainability positioning and risks.

**Skills Used**:
- esg-ratings
- esg-benchmark-comparison

**Queries**:
```
Retrieve ESG ratings and scores, including risk rating and industry rank, for <TICKER>
Retrieve ESG benchmark comparison metrics for <SECTOR> for fiscal year <YEAR>
```

**Output**: ESG scores, ratings, industry comparison, material ESG factors.

**Key Analysis**:
- ESG leader or laggard vs peers
- Material ESG risks for sector
- Rating trajectory
- Regulatory exposure

**Time**: 5-10 minutes

---

## Phase 6: Peer Comparison

**Objective**: Contextualize company performance vs competitors.

**Skills Used**: All skills from Phases 1-5, applied to 2-3 peer companies.

**Queries**: Repeat key queries for each peer ticker.

**Output**: Comparative tables for growth, margins, multiples, ESG.

**Key Analysis**:
- Relative growth rates
- Margin differential
- Valuation premium/discount
- ESG positioning

**Time**: 20-30 minutes (for 2-3 peers)

---

## Phase 7: Report Generation

**Objective**: Synthesize all findings into a decision-ready report.

**Template**: See [report-template.md](report-template.md)

**Sections**:
1. Executive Summary & Snapshot
2. Investment Thesis
3. Investment Positives
4. Competitive/Peer Analysis
5. Estimates & Operating Assumptions
6. Valuation
7. Key Risks
8. ESG Assessment
9. Appendix

**Time**: 30-60 minutes

---

## Total Workflow Time

| Phase | Time Estimate |
|-------|---------------|
| Phase 1: Data Collection | 5-10 min |
| Phase 2: Growth Analysis | 10-15 min |
| Phase 3: Segmentation | 5-10 min |
| Phase 4: Estimates & Health | 5-10 min |
| Phase 5: ESG | 5-10 min |
| Phase 6: Peer Comparison | 20-30 min |
| Phase 7: Report Generation | 30-60 min |
| **Total** | **80-145 min** |

---

## Skill-to-Report Section Mapping

| Report Section | Primary Skills | Secondary Skills |
|----------------|----------------|------------------|
| Executive Summary | ratings-snapshot, analyst-estimates | financial-health-scores |
| Investment Thesis | financial-growth, revenue-product-segmentation | income-statement-growth |
| Investment Positives | income-statement-growth, cash-flow-growth | financial-metrics-analysis |
| Peer Analysis | All growth skills | esg-benchmark-comparison |
| Estimates | analyst-estimates | income-statement, balance-sheet |
| Valuation | historical-financial-ratings | financial-health-scores |
| Key Risks | balance-sheet, cash-flow-statement | esg-ratings |
| ESG Assessment | esg-ratings, esg-benchmark-comparison | - |
| Appendix | All financial statement skills | All growth skills |

---

## Best Practices

1. **Run skills in parallel when possible**: Data collection queries can run simultaneously.

2. **Cache results**: Save skill outputs for reference during report writing.

3. **Cross-validate**: Use multiple skills to confirm key findings.

4. **Document gaps**: Note any "DATA NEEDED" items for follow-up.

5. **Iterate**: Initial analysis may reveal areas needing deeper investigation.

6. **Peer selection**: Choose 2-3 most comparable competitors, not tangential players.

7. **Time management**: Spend 60% on analysis, 40% on report writing.
