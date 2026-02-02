# Octagon Skills

A collection of AI agent skills for financial data analysis powered by the [Octagon MCP](https://github.com/OctagonAI/octagon-mcp).

## Installation

```bash
npx skills add OctagonAI/skills
```

<details>
<summary>bun</summary>

```bash
bunx skills add OctagonAI/skills
```

</details>

<details>
<summary>pnpm</summary>

```bash
pnpm dlx skills add OctagonAI/skills
```

</details>

<details>
<summary>Claude Code</summary>

```
/plugin install <skill-name>
```

</details>

<details>
<summary>Manual installation</summary>

Copy the skill folder to your Claude skills directory.

</details>

## Financial Metrics Analysis Skills

| Skill | Category | Description |
|-------|----------|-------------|
| [financial-metrics-master](skills/financial-metrics-master/) | **Master** | Comprehensive equity research analyst skill that orchestrates all skills for full company analysis |
| [income-statement](skills/income-statement/) | Financial Statements | Retrieve real-time income statement data (Revenue, Net Income, EPS Diluted) |
| [balance-sheet](skills/balance-sheet/) | Financial Statements | Retrieve detailed balance sheet data (Assets, Liabilities, Equity, Net Debt) |
| [cash-flow-statement](skills/cash-flow-statement/) | Financial Statements | Retrieve cash flow statement data (OCF, Investing, Financing, FCF, Cash Position) |
| [financial-metrics-analysis](skills/financial-metrics-analysis/) | Growth Analysis | Analyze year-over-year growth in income statement items (Revenue, COGS, Gross Profit, Operating Income, Net Income) |
| [income-statement-growth](skills/income-statement-growth/) | Growth Analysis | Retrieve YoY growth in Revenue, Gross Profit, Operating Income, Net Income, and EPS Diluted |
| [balance-sheet-growth](skills/balance-sheet-growth/) | Growth Analysis | Retrieve YoY growth in Total Assets, Liabilities, Equity, Cash, and Inventories |
| [cash-flow-growth](skills/cash-flow-growth/) | Growth Analysis | Retrieve YoY growth in Operating Cash Flow, Free Cash Flow, and Net Cash Flow |
| [financial-growth](skills/financial-growth/) | Growth Analysis | Retrieve comprehensive YoY growth in Revenue, Gross Profit, Operating Income, Net Income, EPS, and FCF |
| [revenue-product-segmentation](skills/revenue-product-segmentation/) | Segmentation | Retrieve revenue breakdown by product segment with concentration analysis |
| [revenue-geographic-segmentation](skills/revenue-geographic-segmentation/) | Segmentation | Retrieve revenue breakdown by geographic segment with regional exposure |
| [analyst-estimates](skills/analyst-estimates/) | Estimates & Ratings | Retrieve analyst Revenue and EPS estimates with consensus ranges |
| [financial-health-scores](skills/financial-health-scores/) | Estimates & Ratings | Retrieve Altman Z-Score and Piotroski Score for financial health assessment |
| [historical-financial-ratings](skills/historical-financial-ratings/) | Estimates & Ratings | Retrieve historical financial ratings and key metric scores (ROA, ROE, DCF, D/E) over time |
| [ratings-snapshot](skills/ratings-snapshot/) | Estimates & Ratings | Retrieve current financial ratings overview for quick assessment |
| [esg-ratings](skills/esg-ratings/) | ESG | Retrieve ESG ratings and scores including MSCI ratings, Sustainalytics risk, and industry rank |
| [esg-benchmark-comparison](skills/esg-benchmark-comparison/) | ESG | Retrieve ESG benchmark comparison metrics by sector using MSCI, S&P, CDP frameworks |
| [sec-10k-analysis](skills/sec-10k-analysis/) | SEC Filing Analysis | Analyze 10-K annual filings to extract key financial metrics, risk factors, and business insights |
| [sec-10q-analysis](skills/sec-10q-analysis/) | SEC Filing Analysis | Analyze 10-Q quarterly filings to extract quarterly performance metrics and segment breakdown |

## Get Your Octagon API Key

1. Sign up for a free account at [Octagon](https://app.octagonai.co/signup/?redirectToAfterSignup=https://app.octagonai.co/api-keys)
2. After logging in, from left menu, navigate to **API Keys**
3. Generate a new API key
4. Save the key securely - you'll need it for configuration

## Prerequisites

Before using these skills, you need to have `npx` (which comes with Node.js and npm) installed on your system.

### Mac (macOS)

1. **Install Homebrew** (if you don't have it):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. **Install Node.js (includes npm and npx):**
   ```bash
   brew install node
   ```

3. **Verify installation:**
   ```bash
   node -v
   npm -v
   npx -v
   ```

### Windows

1. **Download the Node.js installer:**
   - Go to [https://nodejs.org/](https://nodejs.org/) and download the LTS version for Windows.
2. **Run the installer** and follow the prompts. This will install Node.js, npm, and npx.
3. **Verify installation:**
   Open Command Prompt and run:
   ```cmd
   node -v
   npm -v
   npx -v
   ```

If you see version numbers for all three, you are ready to proceed.

## MCP Setup

### Cursor

1. Open Cursor Settings
2. Go to **Features > MCP Servers**
3. Click **+ Add New MCP Server**
4. Enter:
   - **Name**: `octagon-mcp`
   - **Type**: `command`
   - **Command**: `env OCTAGON_API_KEY=<your-api-key> npx -y octagon-mcp`

Replace `<your-api-key>` with your actual Octagon API key.

**Windows users:** Use this command format instead:
```
cmd /c "set OCTAGON_API_KEY=<your-api-key> && npx -y octagon-mcp"
```

After adding, refresh the MCP server list to see the new tools. Access the Composer via Command+L (Mac), select "Agent" next to the submit button, and enter your query.

### Claude Desktop

1. Open Claude Desktop
2. Go to Settings > Developer > Edit Config
3. Add the following to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "octagon-mcp-server": {
      "command": "npx",
      "args": ["-y", "octagon-mcp@latest"],
      "env": {
        "OCTAGON_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

4. Restart Claude for the changes to take effect

### Windsurf

Add this to your `./codeium/windsurf/model_config.json`:

```json
{
  "mcpServers": {
    "octagon-mcp-server": {
      "command": "npx",
      "args": ["-y", "octagon-mcp@latest"],
      "env": {
        "OCTAGON_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

## Troubleshooting

- **API Key Issues**: Verify the key is correctly set in the command string with no extra spaces.
- **Connection Issues**: Ensure you have internet connectivity and the Octagon API is accessible.
- **Rate Limiting**: Reduce query frequency if encountering rate limit errors.

## Documentation

- [Octagon Documentation](https://docs.octagonagents.com)
- [Octagon MCP GitHub](https://github.com/OctagonAI/octagon-mcp)
