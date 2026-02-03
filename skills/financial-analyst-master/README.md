# Financial Analyst Master Skill

Comprehensive equity research analyst skill that orchestrates all Octagon financial analysis skills for full company analysis, due diligence, and investment recommendations.

## Installation

```bash
npx skills add OctagonAI/skills --skill financial-analyst-master
```

<details>
<summary>bun</summary>

```bash
bunx skills add OctagonAI/skills --skill financial-analyst-master
```

</details>

<details>
<summary>pnpm</summary>

```bash
pnpm dlx skills add OctagonAI/skills --skill financial-analyst-master
```

</details>

## What This Skill Does

This master skill combines all financial analysis skills into a comprehensive equity research workflow:

- **Financial Statements**: Income statement, balance sheet, cash flow analysis
- **Growth Analysis**: YoY growth metrics across all financial statements
- **Segmentation**: Product and geographic revenue breakdown
- **Estimates & Ratings**: Analyst estimates, health scores, financial ratings
- **ESG**: Environmental, social, and governance ratings

## Example Usage

```
Write an initiation of coverage report for NVDA with investment thesis, valuation, and risks
```

---

## Octagon MCP Setup

This skill requires the [Octagon MCP](https://github.com/OctagonAI/octagon-mcp) server to be configured in your AI agent.

### Get Your API Key

1. Sign up at [Octagon](https://app.octagonai.co/signup/?redirectToAfterSignup=https://app.octagonai.co/api-keys)
2. Navigate to **API Keys** from the left menu
3. Generate and save your API key

### Configure Cursor

1. Open Cursor Settings → **Features > MCP Servers**
2. Click **+ Add New MCP Server**
3. Enter:
   - **Name**: `octagon-mcp`
   - **Type**: `command`
   - **Command**: `env OCTAGON_API_KEY=<your-api-key> npx -y octagon-mcp`

**Windows**: `cmd /c "set OCTAGON_API_KEY=<your-api-key> && npx -y octagon-mcp"`

### Configure Claude Desktop

Add to `claude_desktop_config.json`:

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

### Documentation

- [Octagon Docs](https://docs.octagonagents.com)
- [Octagon MCP GitHub](https://github.com/OctagonAI/octagon-mcp)
