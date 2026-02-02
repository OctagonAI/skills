# Octagon Skills

Agentic financial research skills powered by [Octagon MCP](https://github.com/OctagonAI/octagon-mcp) for autonomous market intelligence.

## Available Skills

### financial-metrics-analysis

Analyze year-over-year growth in income statement items for public companies.

**Example Query:**
```
Retrieve year-over-year growth in key income-statement items for AAPL, limited to 5 records and filtered by period FY.
```

**Output:**

| Year | Revenue Growth | Cost of Revenue Growth | Gross Profit Growth | Operating Income Growth | Net Income Growth |
|------|----------------|------------------------|---------------------|-------------------------|-------------------|

**Data Sources:** octagon-companies-agent, octagon-financials-agent

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
