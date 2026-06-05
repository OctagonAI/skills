# Kalshi CLI Command Cookbook

Use these recipes when exact Kalshi Trading Bot CLI syntax is needed. Prefer `--json` for agent parsing where supported.

## Install, Setup, and Help

Run without cloning:

```
bunx kalshi-trading-bot-cli@latest
```

Install globally:

```
bun add -g kalshi-trading-bot-cli
kalshi
```

Run from a clone:

```
cd /Users/andresgodoy/Documents/dev/kalshi-trading-bot-cli
bun install
bun start
```

Re-run setup:

```
kalshi init
```

Get help:

```
kalshi help
kalshi help search
kalshi help basket
```

Clear cache only when explicitly requested:

```
kalshi clear-cache
```

## Environment

Required for Kalshi trading:

```
KALSHI_API_KEY=<key>
KALSHI_PRIVATE_KEY_FILE=/path/to/private-key.pem
```

or:

```
KALSHI_API_KEY=<key>
KALSHI_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----..."
```

Demo mode:

```
KALSHI_USE_DEMO=true kalshi portfolio
```

Optional research keys:

```
OCTAGON_API_KEY=<key>
TAVILY_API_KEY=<key>
OPENAI_API_KEY=<key>
ANTHROPIC_API_KEY=<key>
GOOGLE_API_KEY=<key>
XAI_API_KEY=<key>
OPENROUTER_API_KEY=<key>
```

Do not print real values in chat or logs.

## Discovery

Search by text:

```
kalshi search "bitcoin price" --category crypto --min-volume 10000 --limit 20
kalshi search "fed decision" --series-prefix KXFED --limit 20 --json
```

Scan for model edge:

```
kalshi search edge --min-edge 5 --limit 10 --sort-by edge_pp
kalshi search edge --category politics --min-volume 1000 --sort-by total_volume --json
```

Find semantic neighbors:

```
kalshi similar KXBTCD-26DEC31-T100000 --top-k 25
kalshi similar -q "Will Bitcoin pierce six figures" --category crypto --min-volume 10000
```

Browse clusters:

```
kalshi clusters
kalshi clusters --label fed
kalshi clusters 42
kalshi clusters --behavioral
kalshi clusters --ranked --timeframe 1y --min-return 0.20 --top-k 5
```

Find peers:

```
kalshi peers KXBTCD-26DEC31-T100000 --limit 50
kalshi peers KXBTCD-26DEC31-T100000 --behavioral
kalshi peers KXBTCD-26DEC31-T100000 --show-cluster
```

Events, series, catalysts, and themes:

```
kalshi events
kalshi events KXFEDCHAIRNOM-29
kalshi series
kalshi series KXBTCD
kalshi series events KXIPO
kalshi catalysts upcoming --days 14
kalshi themes
kalshi themes show "AI Race Milestones"
kalshi themes report
kalshi themes audit
kalshi themes overlap
```

## Research

Analyze one ticker:

```
kalshi analyze KXBTCD-26DEC31-T100000
```

Force a fresh report before trading:

```
kalshi analyze KXBTCD-26DEC31-T100000 --refresh
```

Interpret outputs:
- `model_probability`: independent probability estimate.
- `market_price`: live or latest market-implied probability.
- `edge`: model probability minus market price, usually in percentage points.
- `confidence`: quality or conviction indicator, not a profit guarantee.
- Kelly sizing: suggested risk sizing input, not automatic authorization.

## Correlation and Basket Construction

Correlation matrix:

```
kalshi correlate KX-A KX-B KX-C --window-days 90
kalshi correlate KX-A KX-B --sides yes,no --cells
```

Build a diversified basket:

```
kalshi basket build --category crypto --min-volume 10000 -n 8 --max-per-cluster 2 --max-corr 0.6 --bankroll 1000 --kelly 0.25
```

Build by theme labels:

```
kalshi basket build --label fed,cpi,fomc,gdp,jobs -n 5 --max-per-cluster 1 --max-corr 0.4
```

Size selected legs with explicit probabilities:

```
kalshi basket size --bankroll 1000 --kelly 0.25 --probs KX-A:0.62,KX-B:0.55
```

Auto-fetch model probabilities:

```
kalshi basket size --auto-probs --tickers KX-A,KX-B,KX-C --bankroll 1000 --kelly 0.25
kalshi basket size --auto-probs --theme "AI Race Milestones" --bankroll 1000 --kelly 0.25
```

Validate portfolio diagnostics:

```
kalshi basket validate --tickers KX-A,KX-B,KX-C --bankroll 1000
kalshi basket validate --theme "Iran Escalation" --bankroll 1000
```

## Backtesting

Model scorecard and edge scanner:

```
kalshi backtest --days 30 --min-edge 5 --resolved
kalshi backtest --days 15 --unresolved --min-volume 100 --min-price 5 --max-price 95 --json
```

Export per-market details:

```
kalshi backtest --days 30 --min-edge 5 --export ./kalshi-backtest.csv
```

Basket NAV backtest:

```
kalshi basket backtest --tickers KX-A,KX-B,KX-C --weights 0.4,0.4,0.2 --timeframe 1y
kalshi basket backtest --theme "AI Race Milestones" --timeframe 6m
```

Basket candles:

```
kalshi basket candles --tickers KX-A,KX-B --timeframe 6m
kalshi series candles KXBTCD --timeframe 3m
```

## Portfolio and Monitoring

Portfolio:

```
kalshi portfolio
kalshi portfolio --performance
kalshi portfolio --json
```

Live watch:

```
kalshi watch KXBTCD-26DEC31-T100000
kalshi watch --theme "AI Race Milestones" --interval 30 --dry-run
kalshi watch --theme "Fed Decision" --live --dry-run
```

Use `--dry-run` for scans that should not persist edges or make state changes.

## Trading Operations

Before any live command in this section, apply `safety-checklist.md`.

Buy YES contracts:

```
kalshi buy KXBTCD-26DEC31-T100000 3 58 yes
```

Buy NO contracts:

```
kalshi buy KXBTCD-26DEC31-T100000 3 42 no
```

Sell YES contracts:

```
kalshi sell KXBTCD-26DEC31-T100000 3 60 yes
```

Sell NO contracts:

```
kalshi sell KXBTCD-26DEC31-T100000 3 40 no
```

Cancel an order:

```
kalshi cancel <order_id>
```

Demo-mode execution test:

```
KALSHI_USE_DEMO=true kalshi buy KXBTCD-26DEC31-T100000 1 58 yes
```

Trading notes:
- Prices are cents, not dollars.
- Prefer explicit limit prices.
- The CLI should prompt for confirmation before execution, but agents must still get explicit user confirmation before running live commands.
- Missing side may default in ways the user does not expect; specify `yes` or `no`.

## Scriptability Tips

Use JSON for automation when available:

```
kalshi search edge --min-edge 5 --limit 25 --json
kalshi portfolio --json
kalshi backtest --days 30 --json
```

Capture outputs into files only when the user asks:

```
kalshi backtest --days 30 --export ./kalshi-backtest.csv
```

For long-running watch loops, state the interval, dry-run/live behavior, and stop conditions before starting.
