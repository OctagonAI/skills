# Kalshi CLI Workflow Overview

This document outlines the end-to-end workflow for using the Kalshi Trading Bot CLI as a research, sizing, monitoring, and guarded execution terminal.

## Workflow Diagram

```
Phase 1: Intent Classification
    ├── Setup or diagnostics
    ├── Market discovery
    ├── Research and edge analysis
    ├── Basket construction
    ├── Backtesting
    ├── Portfolio monitoring
    └── Trading operations
           │
           ▼
Phase 2: Runtime and Credential Check
    ├── Bun and CLI availability
    ├── Kalshi API configuration
    ├── Demo vs live mode
    └── Optional Octagon and LLM keys
           │
           ▼
Phase 3: Discovery and Research
    ├── Search, edge scans, clusters, peers
    ├── Analyze market probability and catalysts
    └── Check liquidity and stale data
           │
           ▼
Phase 4: Sizing and Portfolio Validation
    ├── Correlations
    ├── Basket construction
    ├── Kelly sizing
    └── Risk diagnostics
           │
           ▼
Phase 5: Guarded Execution
    ├── Safety checklist
    ├── Exact command review
    └── Explicit live confirmation
           │
           ▼
Phase 6: Monitoring and Audit
    ├── Portfolio
    ├── Orders and cancellations
    ├── Watch loops
    └── JSON/scriptable output
```

## Phase 1: Intent Classification

**Objective**: Decide whether the user request is read-only, local-state-changing, or live-trading-state-changing.

**Common intents**:
- Setup: install, initialize, configure, or troubleshoot the CLI.
- Discovery: find Kalshi markets by query, category, theme, cluster, or series.
- Research: analyze a ticker, refresh a report, compare model probability to market price.
- Portfolio construction: build, validate, size, or backtest a basket.
- Monitoring: inspect portfolio, open orders, live price, or theme scans.
- Trading: buy, sell, or cancel orders.

**Output**: A command path and any missing inputs that must be confirmed.

**Time**: 1-3 minutes.

---

## Phase 2: Runtime and Credential Check

**Objective**: Confirm the environment supports the requested workflow without exposing secrets.

**Checks**:
```
bun --version
bunx kalshi-trading-bot-cli@latest --version
kalshi help
```

**Configuration facts**:
- Config, cache, and SQLite DB live in `~/.kalshi-bot/`.
- The setup wizard writes keys to `~/.kalshi-bot/.env`.
- A local `.env` in the current directory takes precedence for development.
- `KALSHI_USE_DEMO=true` should be preferred for execution tests.

**Key handling**:
- Check whether required variables are configured, but never print values.
- For trading, require `KALSHI_API_KEY` and either `KALSHI_PRIVATE_KEY_FILE` or `KALSHI_PRIVATE_KEY`.
- For Octagon-backed workflows, require `OCTAGON_API_KEY` or explain that only limited local fallback is available.

**Output**: Ready, blocked, or ready with degraded capabilities.

**Time**: 2-5 minutes.

---

## Phase 3: Market Discovery

**Objective**: Build a candidate set before doing detailed research.

**Commands**:
```
kalshi search "bitcoin price" --category crypto --min-volume 10000 --limit 20 --json
kalshi search edge --min-edge 5 --limit 10 --sort-by edge_pp --json
kalshi similar KXBTCD-26DEC31-T100000 --top-k 25
kalshi similar -q "Will Bitcoin pierce six figures" --category crypto
kalshi clusters --label fed
kalshi peers KXBTCD-26DEC31-T100000 --limit 50
kalshi catalysts upcoming --days 14
```

**Key analysis**:
- Prefer liquid markets with narrow spreads.
- Use `search edge` to find model-vs-market dislocations.
- Use clusters and peers to avoid duplicated exposure.
- Use catalysts and close dates to understand path dependency.

**Output**: Ranked candidate tickers with liquidity, category, edge, and close-time context.

**Time**: 5-15 minutes.

---

## Phase 4: Research and Edge Analysis

**Objective**: Convert candidate markets into decision-ready research.

**Commands**:
```
kalshi analyze <ticker>
kalshi analyze <ticker> --refresh
kalshi events <event_ticker>
kalshi series <series_ticker>
kalshi series candles <series_ticker> --timeframe 3m
```

**Key analysis**:
- Market price vs independent model probability.
- Edge in percentage points and expected return.
- Confidence level and data freshness.
- Price drivers, decision-flipping catalysts, and resolution rules.
- Liquidity, open interest, and bid/ask spread.

**Output**: A concise trade thesis or pass decision with missing-data notes.

**Time**: 10-30 minutes depending on refresh depth.

---

## Phase 5: Basket Construction and Sizing

**Objective**: Size risk and manage correlation before any order.

**Commands**:
```
kalshi correlate KX-A KX-B KX-C --window-days 90 --cells
kalshi basket build --category crypto -n 8 --max-per-cluster 2 --max-corr 0.6 --bankroll 1000 --kelly 0.25
kalshi basket size --bankroll 1000 --kelly 0.25 --probs KX-A:0.62,KX-B:0.55
kalshi basket size --auto-probs --tickers KX-A,KX-B,KX-C --bankroll 1000 --kelly 0.25
kalshi basket validate --tickers KX-A,KX-B,KX-C --bankroll 1000
```

**Key analysis**:
- Kelly output is a sizing input, not a trade command.
- Use fractional Kelly for uncertainty and tail risk.
- Apply cluster caps and pairwise correlation caps.
- Watch calendar clashes and same-event duplicates.

**Output**: Proposed allocation, risk gates, max loss, and exposure warnings.

**Time**: 5-20 minutes.

---

## Phase 6: Backtesting and Scenario Review

**Objective**: Understand historical behavior before allocating capital.

**Commands**:
```
kalshi backtest --days 30 --min-edge 5 --resolved --json
kalshi basket backtest --tickers KX-A,KX-B,KX-C --weights 0.4,0.4,0.2 --timeframe 1y
kalshi basket backtest --theme "AI Race Milestones" --timeframe 6m
kalshi basket candles --tickers KX-A,KX-B --timeframe 6m
```

**Key analysis**:
- Win rate, Brier score, Sharpe, max drawdown, total return.
- Resolved vs unresolved market selection.
- Sensitivity to lookback period and stale predictions.
- Whether the backtest universe matches the intended live strategy.

**Output**: Historical support, limitations, and whether the strategy warrants monitoring or execution.

**Time**: 5-20 minutes.

---

## Phase 7: Guarded Execution

**Objective**: Execute only after explicit user confirmation and safety checks.

**Commands**:
```
kalshi buy <ticker> <count> [price] [yes|no]
kalshi sell <ticker> <count> [price] [yes|no]
kalshi cancel <order_id>
```

**Required confirmation**:
- Exact ticker
- Buy or sell
- YES or NO side
- Contract count
- Limit price in cents
- Demo or live mode
- Maximum loss and expected cost

**Output**: If confirmed, the exact command and the resulting order status. If not confirmed, stop.

**Time**: 2-5 minutes after research is complete.

---

## Phase 8: Monitoring and Audit

**Objective**: Track positions, orders, and price movement after research or execution.

**Commands**:
```
kalshi portfolio
kalshi portfolio --performance
kalshi watch <ticker>
kalshi watch --theme "<theme>" --dry-run
kalshi cancel <order_id>
```

**Key analysis**:
- Open exposure, cash, P&L, and concentration.
- Open orders and stale resting orders.
- New catalysts or resolution updates.
- Whether the original thesis has changed.

**Output**: Monitoring summary with next actions and conditions for review, hold, cancel, or exit.

**Time**: Ongoing.
