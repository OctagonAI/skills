# Income Statement Growth Skill

Retrieve year-over-year growth in Revenue, Gross Profit, Operating Income, Net Income, and EPS Diluted for public companies using the Octagon MCP server.

## Installation

```bash
npx skills add OctagonAI/skills --skill income-statement-growth
```

<details>
<summary>bun</summary>

```bash
bunx skills add OctagonAI/skills --skill income-statement-growth
```

</details>

<details>
<summary>pnpm</summary>

```bash
pnpm dlx skills add OctagonAI/skills --skill income-statement-growth
```

</details>

## What This Skill Does

This skill retrieves income statement growth metrics:

- Revenue growth percentage YoY
- Gross profit growth trends
- Operating income growth
- Net income growth rates
- EPS diluted growth

## Example Usage

```
Retrieve YoY growth in Revenue, Gross Profit, and Net Income for AMZN
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
