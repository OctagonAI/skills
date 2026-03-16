# Prediction Markets Analysis Skill

Generate deep research reports on prediction market events using the Octagon Prediction Markets Agent. Combines real-time Kalshi market data with AI-driven analysis to surface price drivers, compare market vs. model probabilities, and identify potential mispricings across 120+ active markets.

## Installation

```bash
npx skills add OctagonAI/skills --skill prediction-markets-analysis
```

<details>
<summary>bun</summary>

```bash
bunx skills add OctagonAI/skills --skill prediction-markets-analysis
```

</details>

<details>
<summary>pnpm</summary>

```bash
pnpm dlx skills add OctagonAI/skills --skill prediction-markets-analysis
```

</details>

## What This Skill Does

This skill generates prediction market research reports:

- Market vs. model probability comparison to spot mispricings
- Event-driven research with key catalysts and price drivers
- Historical resolution tracking for base rate context
- Live contract snapshots (bid/ask, volume, open interest)
- Coverage across Politics, Economics, Crypto, Sports, Entertainment, Climate

## Example Usage

```
Analyze this Fed decision prediction market: https://kalshi.com/markets/kxfeddecision/fed-meeting/kxfeddecision-26jun
```

```
Research this Bitcoin price prediction: https://kalshi.com/markets/kxbtcminy/how-low-will-bitcoin-fall-this-year/kxbtcminy-27jan01
```

```
Generate a fresh report (bypass cache) for SpaceX IPO market: https://kalshi.com/markets/kxipospacex/when-will-spacex-ipo/kxipospacex
```

---

## Octagon MCP Setup

This skill requires the [Octagon MCP](https://github.com/OctagonAI/octagon-mcp) server to be configured in your AI agent.

**Note**: Report generation requires Octagon Plus, Pro, or Enterprise (3 credits per report). Cached reports are free.

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

### Model Variants

| Variant | Description |
|---------|-------------|
| `octagon-prediction-markets-agent` | Default - uses cache if available |
| `octagon-prediction-markets-agent:cache` | Always retrieve cached report |
| `octagon-prediction-markets-agent:refresh` | Always generate fresh report |

### Documentation

- [Octagon Docs](https://docs.octagonagents.com)
- [Browse Markets](https://octagonai.co/markets)
- [Octagon MCP GitHub](https://github.com/OctagonAI/octagon-mcp)
