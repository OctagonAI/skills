# Interpreting Prediction Markets Analysis Results

## Understanding the Report Structure

### Market Overview Section

| Field | Interpretation |
|-------|----------------|
| **Event** | The specific outcome being predicted |
| **Resolution Date** | When the market settles and pays out |
| **Current Market Price** | Implied probability from crowd consensus (e.g., 0.72 = 72%) |
| **Model Probability** | Octagon's independent probability estimate |
| **Mispricing Signal** | Direction and magnitude of potential opportunity |

### Interpreting Mispricing Signals

| Signal | Market Price vs. Model | Action |
|--------|------------------------|--------|
| **Overpriced** | Market > Model | Consider selling/shorting |
| **Underpriced** | Market < Model | Consider buying |
| **Fair Value** | Market ≈ Model (within 2%) | No clear edge |

### Confidence Levels

| Spread | Confidence | Interpretation |
|--------|------------|----------------|
| 0-2% | Low | Market fairly priced, no clear edge |
| 2-5% | Moderate | Potential opportunity, validate with research |
| 5-10% | High | Strong mispricing signal |
| >10% | Very High | Significant divergence, check for news/catalyst |

## Price Drivers Analysis

### Driver Categories

| Category | Examples | Impact Assessment |
|----------|----------|-------------------|
| **Economic Data** | CPI, jobs reports, GDP | Quantifiable, often immediate |
| **Policy Signals** | Fed speeches, legislation | Directional, timing uncertain |
| **Market Sentiment** | Polls, surveys, forecasts | Leading indicators |
| **Technical Factors** | Liquidity, positioning | Can cause short-term moves |

### Weighting Drivers

Not all drivers are equal. Consider:

1. **Proximity to resolution**: Closer events have higher impact
2. **Uncertainty reduction**: Does the driver resolve key unknowns?
3. **Consensus vs. surprise**: Expected events are often priced in

## Catalyst Calendar Interpretation

### Impact Classifications

| Impact Level | Description | Price Move Potential |
|--------------|-------------|---------------------|
| **High** | Decision-flipping event | 5-15% probability shift |
| **Medium** | Incremental information | 2-5% probability shift |
| **Low** | Background context | <2% probability shift |

### Timing Considerations

- **Pre-catalyst**: Volatility often increases, spreads widen
- **Post-catalyst**: Rapid repricing, improved liquidity
- **Between catalysts**: Gradual drift toward model probability

## Contract Details Analysis

### Key Metrics

| Metric | What It Tells You |
|--------|-------------------|
| **Bid** | Highest price buyers will pay |
| **Ask** | Lowest price sellers will accept |
| **Spread** | Bid-Ask difference; wider = less liquid |
| **Last** | Most recent trade price |
| **Volume** | Trading activity; higher = more interest |
| **Open Interest (OI)** | Total outstanding contracts; higher = more liquidity |

### Liquidity Assessment

| Volume/OI | Spread | Liquidity | Trading Implication |
|-----------|--------|-----------|---------------------|
| High | Tight (<2¢) | Excellent | Easy entry/exit, minimal slippage |
| High | Wide (>5¢) | Moderate | Active but inefficient |
| Low | Tight | Fair | Can trade, size limited |
| Low | Wide | Poor | Difficult to execute, avoid large positions |

## Historical Resolution Context

### Base Rate Analysis

| Historical Pattern | Interpretation |
|-------------------|----------------|
| **High resolution rate** | Outcome more likely than base rate suggests |
| **Low resolution rate** | Outcome less likely than base rate suggests |
| **Volatile history** | Higher uncertainty, wider probability ranges appropriate |

### Model Accuracy Tracking

| Model Accuracy | Interpretation |
|----------------|----------------|
| >80% | Strong track record, trust model signals |
| 60-80% | Good but not perfect, use as input not gospel |
| <60% | Model struggles with this market type, weight less |

## Recommendation Framework

### Signal Strength Matrix

| Model Edge | Liquidity | Catalyst Timing | Recommendation |
|------------|-----------|-----------------|----------------|
| Strong (>5%) | High | Near-term | Strong trade |
| Strong | Low | Any | Trade small, be patient |
| Strong | High | Far out | Partial position, add later |
| Moderate (2-5%) | High | Near-term | Consider trade |
| Moderate | Low | Any | Pass or small position |
| Weak (<2%) | Any | Any | No trade |

### Position Sizing Guidelines

| Edge Confidence | Suggested Position |
|-----------------|-------------------|
| Very High | Up to 5% of portfolio |
| High | 2-3% of portfolio |
| Moderate | 1-2% of portfolio |
| Speculative | <1% of portfolio |

## Red Flags to Watch

### Report Quality Concerns

| Red Flag | Potential Issue |
|----------|-----------------|
| Model probability = market price | Model may be overfitting to market |
| No catalysts identified | May be missing key events |
| Thin volume, wide spreads | Execution risk high |
| Recent major price move | Report may not reflect latest info |

### When to Request Fresh Report

- Major news event since last report
- Resolution date approaching
- Key catalyst just occurred
- Market price moved >5% since report
- Need latest contract details for execution

## Combining with Fundamental Analysis

| Skill | How It Helps |
|-------|--------------|
| `earnings-call-analysis` | CEO/CFO comments on topics related to prediction markets |
| `sec-8k-analysis` | Material corporate events affecting outcomes |
| `stock-performance` | Price action correlation with event probability |
| `financial-guidance` | Forward guidance relevant to economic predictions |

## Common Pitfalls

1. **Overweighting model probability**: It's an input, not truth
2. **Ignoring liquidity**: Can't profit if you can't exit
3. **Chasing moved markets**: The edge may be gone
4. **Ignoring resolution mechanics**: Know exactly how the market settles
5. **Position sizing errors**: Even high-edge trades can lose
