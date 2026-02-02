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
| [cash-flow-statement](cash-flow-statement/) | Retrieve cash flow statement data (OCF, Investing, Financing, FCF, Cash Position) |
| [revenue-product-segmentation](revenue-product-segmentation/) | Retrieve revenue breakdown by product segment with concentration analysis |
| [revenue-geographic-segmentation](revenue-geographic-segmentation/) | Retrieve revenue breakdown by geographic segment with regional exposure |
| [analyst-estimates](analyst-estimates/) | Retrieve analyst Revenue and EPS estimates with consensus ranges |
| [financial-health-scores](financial-health-scores/) | Retrieve Altman Z-Score and Piotroski Score for financial health assessment |

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
