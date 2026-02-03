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
| [financial-analyst-master](skills/financial-analyst-master/) | **Master** | Comprehensive equity research analyst skill that orchestrates all skills for full company analysis |
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

## Earnings Call Analysis Skills

| Skill | Category | Description |
|-------|----------|-------------|
| [earnings-analyst-master](skills/earnings-analyst-master/) | **Master** | Comprehensive earnings analyst skill that orchestrates all earnings skills for transcript analysis |
| [earnings-call-insights](skills/earnings-call-insights/) | Guidance Analysis | Analyze earnings call transcripts to extract future guidance, strategic priorities, and management commentary |
| [earnings-call-analysis](skills/earnings-call-analysis/) | Transcript Analysis | Analyze earnings call transcripts with follow-up questions and source citations |
| [earnings-mgmt-comments](skills/earnings-mgmt-comments/) | Management Commentary | Extract management's commentary on specific topics with executive attribution |
| [earnings-qa-analysis](skills/earnings-qa-analysis/) | Q&A Analysis | Analyze the Q&A section for strategic insights and analyst concerns |
| [earnings-financial-guidance](skills/earnings-financial-guidance/) | Financial Guidance | Extract financial guidance and forward-looking statements with segment detail |
| [earnings-analyst-questions](skills/earnings-analyst-questions/) | Analyst Questions | Identify key themes and concerns raised by analysts with attribution |
| [earnings-conf-call-sentiment](skills/earnings-conf-call-sentiment/) | Sentiment Analysis | Analyze overall sentiment and tone of management during conference calls |
| [earnings-revenue-guidance](skills/earnings-revenue-guidance/) | Revenue Guidance | Extract revenue guidance and growth projections with segment and currency breakdown |
| [earnings-competitive-review](skills/earnings-competitive-review/) | Competitive Analysis | Analyze competitive landscape, market positioning, and strategic differentiation |
| [earnings-capital-allocation](skills/earnings-capital-allocation/) | Capital Allocation | Extract capital allocation, investment priorities, buybacks, and dividend commentary |
| [earnings-market-expansion](skills/earnings-market-expansion/) | Market Expansion | Identify geographic growth plans, new market launches, and product diversification |
| [earnings-cost-mgmt](skills/earnings-cost-mgmt/) | Cost Management | Analyze cost reduction initiatives, restructuring, and operational efficiency |
| [earnings-product-pipeline](skills/earnings-product-pipeline/) | Product Pipeline | Extract R&D updates, clinical trials, regulatory filings, and launch timelines |

## SEC Filings Analysis Skills

| Skill | Category | Description |
|-------|----------|-------------|
| [sec-analyst-master](skills/sec-analyst-master/) | **Master** | Comprehensive SEC filing analyst skill that orchestrates all SEC skills for due diligence |
| [sec-10k-analysis](skills/sec-10k-analysis/) | Annual Filings | Analyze 10-K annual filings to extract key financial metrics, risk factors, and business insights |
| [sec-10q-analysis](skills/sec-10q-analysis/) | Quarterly Filings | Analyze 10-Q quarterly filings to extract quarterly performance metrics and segment breakdown |
| [sec-risk-factors](skills/sec-risk-factors/) | Risk Analysis | Extract and summarize risk factors from 10-K and 10-Q filings with categorization |
| [sec-mda-analysis](skills/sec-mda-analysis/) | Management Analysis | Analyze Management Discussion and Analysis sections for strategic insights |
| [sec-8k-analysis](skills/sec-8k-analysis/) | Current Events | Analyze 8-K filings to extract material events and corporate changes |
| [sec-proxy-analysis](skills/sec-proxy-analysis/) | Governance | Extract executive compensation and governance info from proxy statements |
| [sec-business-desc-analysis](skills/sec-business-desc-analysis/) | Business Analysis | Extract business descriptions and competitive landscape from 10-K filings |
| [sec-footnotes-analysis](skills/sec-footnotes-analysis/) | Accounting | Analyze footnotes and accounting policies from 10-K and 10-Q filings |
| [sec-s1-analysis](skills/sec-s1-analysis/) | IPO Analysis | Analyze S-1 registration statements for IPO risks, opportunities, and capitalization |
| [sec-amendments-review](skills/sec-amendments-review/) | Filing Changes | Review amendments to SEC filings and identify material changes or corrections |
| [sec-annual-comparison](skills/sec-annual-comparison/) | Trend Analysis | Compare key metrics and risk factors between current and prior year 10-K filings |
| [sec-segment-reporting](skills/sec-segment-reporting/) | Segment Analysis | Analyze business segment performance, margins, and geographic breakdown |
| [sec-cash-flow-review](skills/sec-cash-flow-review/) | Cash Flow | Extract and analyze cash flow trends and working capital changes |
| [sec-corp-governance](skills/sec-corp-governance/) | Governance | Review corporate governance practices, board composition, and policies |
| [sec-debt-covenant](skills/sec-debt-covenant/) | Debt Analysis | Analyze debt covenants and credit agreement terms from SEC filings |

## Stock Performance & Market Data Skills

| Skill | Category | Description |
|-------|----------|-------------|
| [market-analyst-master](skills/market-analyst-master/) | **Master** | Comprehensive market analyst skill that orchestrates all stock skills for market analysis |
| [stock-performance](skills/stock-performance/) | Price Data | Retrieve daily closing prices, trading volume, and historical price trends |
| [stock-quote](skills/stock-quote/) | Price Data | Get real-time stock quotes with current price, volume, day range, 52-week range, and moving averages |
| [batch-market-cap](skills/batch-market-cap/) | Market Cap | Retrieve market capitalization data for multiple companies at once |
| [company-market-cap](skills/company-market-cap/) | Market Cap | Get market capitalization data for a single company with size classification |
| [price-target-summary](skills/price-target-summary/) | Analyst Sentiment | Retrieve analysts' price target summary with trends across timeframes |
| [price-target-consensus](skills/price-target-consensus/) | Analyst Sentiment | Get consensus, median, high, and low analyst price targets |
| [stock-grades](skills/stock-grades/) | Analyst Sentiment | Get latest analyst ratings, upgrades, and downgrades from financial institutions |
| [sector-pe-ratios](skills/sector-pe-ratios/) | Valuation | Retrieve sector P/E ratios by exchange for valuation benchmarking |
| [industry-pe-ratios](skills/industry-pe-ratios/) | Valuation | Retrieve industry-specific P/E ratios for peer group comparisons |
| [sector-performance-snapshot](skills/sector-performance-snapshot/) | Sector Analysis | Get sector-wide metrics including revenue, EBITDA, market cap, and enterprise value |
| [industry-performance-snapshot](skills/industry-performance-snapshot/) | Sector Analysis | Get daily industry performance overview with average price changes |
| [historical-market-cap](skills/historical-market-cap/) | Market Cap | Retrieve historical market capitalization data over date ranges |
| [stock-historical-index](skills/stock-historical-index/) | Index Data | Retrieve historical end-of-day price data for market indices (S&P 500, NASDAQ, etc.) |
| [stock-price-change](skills/stock-price-change/) | Price Data | Get price change statistics across multiple time periods (1D to 10Y) |
| [commodities-list](skills/commodities-list/) | Commodities | Retrieve catalog of tradable commodities across energy, metals, and agriculture |
| [commodities-quote](skills/commodities-quote/) | Commodities | Get real-time commodity price quotes with day ranges and moving averages |
| [forex-list](skills/forex-list/) | Forex | Retrieve listing of actively traded currency pairs (majors, crosses, exotics) |

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

## License

MIT License - see [LICENSE](LICENSE) for details.
