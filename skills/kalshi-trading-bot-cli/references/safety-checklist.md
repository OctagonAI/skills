# Kalshi CLI Safety Checklist

Apply this checklist before any command that can affect live trading state: `buy`, `sell`, `cancel`, setup changes, credential changes, or cache-clearing when it could affect an active workflow.

## Default Stance

Use read-only commands until the user explicitly asks for execution.

Prefer:
- `KALSHI_USE_DEMO=true` for execution tests
- `--dry-run` for watch or scan workflows
- `--json` for automation and auditability
- Explicit limit prices and explicit `yes` or `no` side

Never:
- Print `.env` values, private keys, API keys, order tokens, or credential file contents
- Place a live order from model output alone
- Treat Kelly sizing as authorization to trade
- Run live commands when the user asked only for a plan, review, analysis, or example

## Live Trade Gate

Before running `kalshi buy` or `kalshi sell`, confirm all of the following in plain text:

```
Ticker: <ticker>
Action: buy or sell
Side: yes or no
Count: <contracts>
Limit price: <cents>
Mode: demo or live
Estimated cost or proceeds: <$>
Maximum loss: <$>
Reason for trade: <brief thesis>
```

Then require explicit confirmation from the user. Accept only a clear instruction such as:

```
Yes, execute this live order:
kalshi buy <ticker> <count> <price> <side>
```

If the user has not confirmed live mode, use demo mode or stop.

## Price and Side Checks

Prices are in cents:
- `58` means `$0.58`, or 58 percent implied probability.
- Do not pass `0.58` unless the CLI documentation explicitly supports decimal dollars for that command.
- Reject prices outside `1` to `99` cents unless the user gives a market-structure reason.

Side checks:
- Specify `yes` or `no` explicitly.
- For `NO`, verify the user understands the inverse outcome and payout.
- For sells, verify the user owns or intends to close the matching side.

## Market and Data Freshness

Before execution, verify:
- Market is active and not halted, expired, or already resolved.
- Close or resolution time is compatible with the strategy.
- The latest analysis is fresh enough for the catalyst cycle.
- The bid/ask spread is acceptable for the trade size.
- Volume and open interest are adequate.
- Resolution rules are understood.

If data is stale or unclear, run:

```
kalshi analyze <ticker> --refresh
kalshi search <ticker> --json
kalshi portfolio --json
```

Use the exact commands supported by the installed CLI version.

## Sizing and Exposure

Before execution, calculate or state:
- Bankroll assumption
- Contract count
- Max loss
- Position cost
- Kelly or fractional Kelly recommendation, if used
- Existing exposure to the same event, series, theme, or correlated cluster

Useful checks:

```
kalshi basket validate --tickers <csv> --bankroll <usd>
kalshi correlate <t1> <t2> <t3> --window-days 90
kalshi portfolio --performance
```

Risk warnings:
- Multiple contracts in one event can be economically duplicated.
- Same-theme markets can be highly correlated even when tickers differ.
- Fractional Kelly does not protect against bad probabilities, stale data, or tail events.
- Thin books can turn a theoretical edge into negative expected value after spread and slippage.

## Order Placement

Prefer explicit limit orders:

```
kalshi buy <ticker> <count> <price> <side>
kalshi sell <ticker> <count> <price> <side>
```

Avoid omitted price unless the user explicitly wants the CLI default behavior and understands the risk.

After placing an order:
- Capture the order ID.
- Check whether it filled or is resting.
- If resting, define when to cancel or revise.
- Review `portfolio` and open orders.

## Cancellation

Before `kalshi cancel <order_id>`:
- Confirm the order ID.
- Confirm the order is the intended resting order.
- Explain that cancellation is state-changing.
- Ask for explicit confirmation if the cancellation affects live orders.

Do not cancel orders based only on a partial or ambiguous order ID.

## Demo Mode

Use demo mode for:
- Testing the CLI
- Rehearsing execution
- Validating command syntax
- Examples in documentation or chat
- Ambiguous requests that mention buying or selling without explicit live intent

Example:

```
KALSHI_USE_DEMO=true kalshi buy KXBTCD-26DEC31-T100000 1 58 yes
```

State clearly when a command is demo-only.

## Dry-Run and Watch Loops

For watch or scanner workflows:

```
kalshi watch --theme "<theme>" --interval 30 --dry-run
```

Before starting a loop, define:
- Theme or ticker scope
- Scan interval
- Whether results persist
- Stop condition
- Expected duration

Do not start long-running live monitoring without a clear user request.

## Secret Handling

Allowed:
- Check whether a variable is set without printing the value.
- Tell the user which variables are required.
- Suggest `kalshi init` to re-run setup.

Not allowed:
- Printing `.env`
- Printing private key files
- Copying credentials into commands shown in chat
- Committing credentials
- Asking the user to paste private keys into chat

Use placeholders in examples:

```
KALSHI_API_KEY=<your-key>
KALSHI_PRIVATE_KEY_FILE=/path/to/private-key.pem
```

## Failure Modes

If an order command fails:
- Do not retry automatically.
- Read the error at a high level without exposing secrets.
- Check whether the failure was auth, market state, price bounds, insufficient funds, or network/API availability.
- Ask before trying again, especially for live trades.

If CLI output is ambiguous:
- Stop and ask for clarification.
- Prefer `portfolio`, `orders`, or `--json` outputs if available.
- Do not infer fills from a command that only placed a resting order.

## Final Pre-Execution Prompt

Use this template before live execution:

```
This is a live Kalshi order. Please confirm:

Command: kalshi <buy|sell> <ticker> <count> <price> <yes|no>
Mode: live
Max loss: <$>
Rationale: <one sentence>

Reply with: Yes, execute this live order.
```

If the user replies with anything ambiguous, do not execute.
