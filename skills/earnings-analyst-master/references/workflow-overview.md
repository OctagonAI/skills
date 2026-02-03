# Earnings Analysis Workflow Overview

## Complete Analysis Workflow

This document outlines the end-to-end workflow for comprehensive earnings call analysis.

```
┌─────────────────────────────────────────────────────────────────┐
│                   EARNINGS ANALYST WORKFLOW                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Phase 1: Guidance Extraction                                    │
│  └─→ Revenue, margin, EPS guidance with segment detail          │
│                                                                  │
│  Phase 2: Management Commentary                                  │
│  └─→ Executive quotes, strategic priorities, tone               │
│                                                                  │
│  Phase 3: Analyst Sentiment                                      │
│  └─→ Key concerns, recurring questions, unresolved issues       │
│                                                                  │
│  Phase 4: Strategic Deep Dives                                   │
│  └─→ Competition, capital allocation, expansion, costs, R&D     │
│                                                                  │
│  Phase 5: Peer Comparison                                        │
│  └─→ Compare guidance and sentiment across competitors          │
│                                                                  │
│  Phase 6: Report Generation                                      │
│  └─→ Synthesize into actionable earnings digest                 │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

## Phase 1: Guidance Extraction

### Objective
Extract all forward-looking financial guidance from the earnings call.

### Skills Used
- `earnings-financial-guidance` - Full guidance with caveats
- `earnings-revenue-guidance` - Detailed revenue projections
- `earnings-call-insights` - Key future guidance highlights

### Example Queries

```
Extract and analyze financial guidance and forward-looking statements from AAPL's latest earnings transcript
Extract specific revenue guidance and growth projections from AAPL's latest earnings call
Analyze AAPL's latest earnings call transcript and extract key insights about future guidance
```

### Expected Output
- Revenue guidance range and growth rate
- Segment-level revenue breakdown
- Margin guidance (gross, operating)
- EPS expectations
- Key assumptions and risk factors

### Time Estimate
~3 minutes

---

## Phase 2: Management Commentary Analysis

### Objective
Analyze qualitative management commentary for strategic insights.

### Skills Used
- `earnings-conf-call-sentiment` - Overall tone and confidence
- `earnings-mgmt-comments` - Topic-specific commentary
- `earnings-call-analysis` - Full call analysis

### Example Queries

```
Analyze the overall sentiment and tone of management during AAPL's earnings call
Extract management's commentary about product development from AAPL's earnings call
Analyze AAPL's earnings call Q&A for management responses on key topics
```

### Expected Output
- Sentiment classification (confident/cautious/defensive)
- Key executive quotes with attribution
- Topic-by-topic breakdown
- Changes from prior quarter tone

### Time Estimate
~3 minutes

---

## Phase 3: Analyst Sentiment

### Objective
Understand Street concerns and areas of focus.

### Skills Used
- `earnings-analyst-questions` - Key themes raised by analysts
- `earnings-qa-analysis` - Q&A section analysis

### Example Queries

```
Identify key themes and concerns raised by analysts during AAPL's earnings call
Analyze the Q&A section of AAPL's earnings call for insights about analyst concerns
```

### Expected Output
- Top analyst concerns
- Most frequently asked topics
- Questions that weren't fully answered
- Response quality assessment

### Time Estimate
~2 minutes

---

## Phase 4: Strategic Deep Dives

### Objective
Conduct targeted analysis on key strategic areas.

### Skills Used
- `earnings-competitive-review` - Competition and positioning
- `earnings-capital-allocation` - Investment priorities
- `earnings-market-expansion` - Geographic growth
- `earnings-cost-mgmt` - Efficiency initiatives
- `earnings-product-pipeline` - R&D and product updates

### Example Queries

```
Analyze competitive landscape and market positioning from AAPL's earnings call
Extract capital allocation and investment priorities from AAPL's earnings transcript
Identify market expansion and geographic growth plans from AAPL's earnings call
Analyze cost reduction initiatives from AAPL's earnings transcript
Extract product development and pipeline updates from AAPL's earnings call
```

### Expected Output
- Competitive positioning updates
- CapEx, buyback, dividend plans
- New market entry plans
- Cost savings initiatives
- Product launch timelines

### Time Estimate
~5 minutes

---

## Phase 5: Peer Comparison

### Objective
Compare earnings themes across competitors.

### Skills Used
- All Phase 1-4 skills applied to peer companies

### Example Queries

```
Analyze the overall sentiment and tone of management during MSFT's earnings call
Extract revenue guidance from GOOGL's latest earnings call
Compare guidance changes across AAPL, MSFT, GOOGL
```

### Expected Output
- Comparative guidance table
- Sentiment comparison
- Strategic focus differences
- Relative positioning

### Time Estimate
~5 minutes

---

## Phase 6: Report Generation

### Objective
Synthesize all findings into actionable earnings analysis.

### Skills Used
- All previous skills synthesized

### Report Sections

1. **Executive Summary** - Beat/miss, guidance change, key takeaways
2. **Guidance Analysis** - Detailed financial outlook
3. **Management Commentary** - Key quotes and themes
4. **Q&A Analysis** - Analyst concerns and responses
5. **Sentiment Assessment** - Tone and confidence
6. **Strategic Updates** - Competition, allocation, expansion, costs, R&D
7. **Investment Implications** - Actionable conclusions

### Output Format
- 3,000-6,000 words
- Tables for comparative data
- Bold key metrics
- Source citations

### Time Estimate
~10 minutes

---

## Total Workflow Time

| Phase | Time |
|-------|------|
| Phase 1: Guidance Extraction | 3 min |
| Phase 2: Management Commentary | 3 min |
| Phase 3: Analyst Sentiment | 2 min |
| Phase 4: Strategic Deep Dives | 5 min |
| Phase 5: Peer Comparison | 5 min |
| Phase 6: Report Generation | 10 min |
| **Total** | **~30 minutes** |

## Workflow Variations

### Quick Earnings Summary (10 min)
- Phase 1: Guidance highlights only
- Phase 2: Sentiment only
- Brief summary

### Standard Earnings Analysis (20 min)
- Phases 1-4
- Single company focus
- Standard report

### Comprehensive Earnings Report (35+ min)
- All phases including peer comparison
- Full report with all sections
- Multiple companies analyzed
