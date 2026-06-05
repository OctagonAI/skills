# Kalshi Trading Bot CLI Skill

Operate the Kalshi Trading Bot CLI for prediction-market research, edge discovery, basket construction, backtesting, portfolio monitoring, and guarded trade execution.

## Installation

```bash
npx skills add OctagonAI/skills --skill kalshi-trading-bot-cli
```

<details>
<summary>bun</summary>

```bash
bunx skills add OctagonAI/skills --skill kalshi-trading-bot-cli
```

</details>

<details>
<summary>pnpm</summary>

```bash
pnpm dlx skills add OctagonAI/skills --skill kalshi-trading-bot-cli
```

</details>

## What This Skill Does

This master skill helps agents operate the Kalshi Trading Bot CLI safely and effectively:

- **Setup and Diagnostics**: Install, initialize, and verify the Bun-based CLI without exposing credentials
- **Market Discovery**: Search markets, scan for edge, browse clusters, inspect peers, themes, events, and catalysts
- **Research and Edge Analysis**: Analyze market probability, price drivers, liquidity, and stale-data risk
- **Portfolio Construction**: Build, validate, correlate, size, and backtest diversified baskets
- **Monitoring**: Review portfolio risk, watch tickers or themes, and use JSON output for automation
- **Guarded Trade Execution**: Apply live-trading safety checks before any buy, sell, or cancel command

## Example Usage

```
Use the Kalshi CLI to find liquid crypto prediction markets with at least 5 percentage points of model edge, then summarize the top candidates.
```

```
Build and validate a diversified Kalshi basket for Fed, CPI, jobs, and GDP themes using a $1,000 bankroll and 0.25 Kelly multiplier.
```

```
Prepare, but do not execute, the safest command sequence for buying 3 YES contracts in KXBTCD-26DEC31-T100000 at 58 cents.
```

---

## Kalshi Trading Bot CLI Setup

This skill requires the [Kalshi Trading Bot CLI](https://github.com/OctagonAI/kalshi-trading-bot-cli) and Bun.

### Run Without Cloning

```bash
bunx kalshi-trading-bot-cli@latest
```

### Install Globally

```bash
bun add -g kalshi-trading-bot-cli
kalshi
```

### Development Clone

```bash
git clone https://github.com/OctagonAI/kalshi-trading-bot-cli.git
cd kalshi-trading-bot-cli
bun install
bun start
```

### Configuration

The setup wizard writes API keys to `~/.kalshi-bot/.env`. A `.env` in the current directory takes precedence for development.

Required for trading:

```bash
KALSHI_API_KEY=<your-kalshi-api-key>
KALSHI_PRIVATE_KEY_FILE=/path/to/private-key.pem
```

Optional:

```bash
KALSHI_USE_DEMO=true
OCTAGON_API_KEY=<your-octagon-api-key>
TAVILY_API_KEY=<your-tavily-api-key>
```

Never paste or print real API keys, private keys, or `.env` contents.

### Core Commands

| Workflow | Example |
|----------|---------|
| Search | `kalshi search "bitcoin price" --category crypto --limit 20` |
| Edge scan | `kalshi search edge --min-edge 5 --limit 10 --sort-by edge_pp` |
| Analyze | `kalshi analyze <ticker> --refresh` |
| Basket build | `kalshi basket build --category crypto -n 8 --max-corr 0.6` |
| Basket size | `kalshi basket size --bankroll 1000 --kelly 0.25 --probs KX-A:0.62` |
| Backtest | `kalshi basket backtest --tickers KX-A,KX-B --timeframe 1y` |
| Portfolio | `kalshi portfolio --performance` |
| Watch | `kalshi watch --theme "Fed Decision" --dry-run` |
| Trade | `kalshi buy <ticker> <count> <price> <yes|no>` |

### Safety Model

The skill defaults to read-only workflows. It requires explicit user confirmation before live `buy`, `sell`, or `cancel` commands and recommends demo mode for execution tests:

```bash
KALSHI_USE_DEMO=true kalshi buy KXBTCD-26DEC31-T100000 1 58 yes
```

### Documentation

- [Kalshi Trading Bot CLI](https://github.com/OctagonAI/kalshi-trading-bot-cli)
- [Octagon](https://app.octagonai.co)
- [Kalshi](https://kalshi.com)
