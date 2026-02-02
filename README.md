# Octagon Skills

Agentic financial research skills powered by [Octagon MCP](https://github.com/OctagonAI/octagon-mcp).

## Available Skills

| Skill | Description |
|-------|-------------|
| [financial-metrics-analysis](financial-metrics-analysis/) | Analyze year-over-year growth in income statement items (Revenue, COGS, Gross Profit, Operating Income, Net Income) |
| [income-statement-growth](income-statement-growth/) | Retrieve YoY growth in Revenue, Gross Profit, Operating Income, Net Income, and EPS Diluted |
| [balance-sheet-growth](balance-sheet-growth/) | Retrieve YoY growth in Total Assets, Liabilities, Equity, Cash, and Inventories |
| [cash-flow-growth](cash-flow-growth/) | Retrieve YoY growth in Operating Cash Flow, Free Cash Flow, and Net Cash Flow |
| [financial-growth](financial-growth/) | Retrieve comprehensive YoY growth in Revenue, Gross Profit, Operating Income, Net Income, EPS, and FCF |
| [income-statement](income-statement/) | Retrieve real-time income statement data (Revenue, Net Income, EPS Diluted) |
| [balance-sheet](balance-sheet/) | Retrieve detailed balance sheet data (Assets, Liabilities, Equity, Net Debt) |

## Prerequisites

- [Octagon API Key](https://octagonagents.com) (free)
- Node.js with npx
- Cursor IDE with MCP support

## Quick Setup

1. Get your API key from https://octagonagents.com
2. In Cursor: Settings > Features > MCP Servers > Add New
3. Configure:
   - **Name:** `octagon-mcp`
   - **Type:** `command`
   - **Command:** `env OCTAGON_API_KEY=<your-key> npx -y octagon-mcp`

## License

MIT
