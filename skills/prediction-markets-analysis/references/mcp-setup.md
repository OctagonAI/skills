# Octagon MCP Setup

## Get Your Octagon API Key

1. Sign up for a free account at [Octagon](https://app.octagonai.co/signup/?redirectToAfterSignup=https://app.octagonai.co/api-keys)
2. After logging in, from left menu, navigate to **API Keys**
3. Generate a new API key
4. Save the key securely - you'll need it for configuration

**Note**: Prediction Markets report generation requires Octagon Plus, Pro, or Enterprise subscription (3 credits per report). Cached reports are free for all users.

## Prerequisites

Before installing or running Octagon MCP, you need to have `npx` (which comes with Node.js and npm) installed on your system.

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

## Configure Cursor

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

After adding, refresh the MCP server list to see the new tools. The Composer Agent will automatically use Octagon MCP when appropriate. Access the Composer via Command+L (Mac), select "Agent" next to the submit button, and enter your query.

## Configure Claude Desktop

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

## Configure Windsurf

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

## Remote MCP Server (Alternative)

For clients that support remote MCP connections:

**With OAuth (recommended):**
```
https://mcp.octagonagents.com/mcp
```

**Without OAuth:**
```
https://mcp.octagonagents.com/{OCTAGON_API_KEY}/mcp
```

## Verify Setup

1. Refresh the MCP server list
2. The `octagon-prediction-markets-agent` tool should appear in available tools
3. Test with a simple query:
   ```
   Analyze this prediction market: https://kalshi.com/markets/kxfeddecision/fed-meeting/kxfeddecision-26jun
   ```

## Available Tools

| Tool | Description |
|------|-------------|
| `octagon-prediction-markets-agent` | Generate research reports on prediction market events |
| `prediction_markets_history` | Fetch historical data for prediction market tickers |
| `octagon-agent` | Comprehensive market intelligence (SEC filings, earnings, financials, stock data) |
| `octagon-deep-research-agent` | Aggregate research from multiple web sources |

## Model Variants

When using the prediction markets agent, you can specify caching behavior:

| Variant | Behavior |
|---------|----------|
| `octagon-prediction-markets-agent` | Default - cached if available, else generate |
| `octagon-prediction-markets-agent:cache` | Always use cached report |
| `octagon-prediction-markets-agent:refresh` | Always generate fresh report |

## Troubleshooting

**API Key Issues**: Verify the key is correctly set in the command string with no extra spaces.

**Connection Issues**: Ensure you have internet connectivity and the Octagon API is accessible.

**Rate Limiting**: Reduce query frequency if encountering rate limit errors.

**Subscription Required**: Report generation requires Octagon Plus/Pro/Enterprise. Cached reports are free.

## Documentation

Full documentation: [https://docs.octagonagents.com](https://docs.octagonagents.com)

Browse markets: [https://octagonai.co/markets](https://octagonai.co/markets)
