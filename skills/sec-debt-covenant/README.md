# SEC Debt Covenant Skill

Analyze debt covenants and credit agreement terms from SEC filings using the Octagon MCP server.

## Installation

```bash
npx skills add OctagonAI/skills --skill sec-debt-covenant
```

<details>
<summary>bun</summary>

```bash
bunx skills add OctagonAI/skills --skill sec-debt-covenant
```

</details>

<details>
<summary>pnpm</summary>

```bash
pnpm dlx skills add OctagonAI/skills --skill sec-debt-covenant
```

</details>

## What This Skill Does

This skill analyzes debt disclosures:

- Covenant terms and thresholds
- Debt maturity schedules
- Interest rate terms
- Credit facility details
- Covenant compliance status

## Example Usage

```
Analyze debt covenants and credit terms from company's 10-K filing
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
