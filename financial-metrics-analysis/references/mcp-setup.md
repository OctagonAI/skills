# Octagon MCP Setup for Cursor

## Prerequisites

Install Node.js (includes npm and npx):

**macOS:**
```bash
brew install node
```

**Windows:**
Download from https://nodejs.org/ (LTS version)

Verify installation:
```bash
node -v
npm -v
npx -v
```

## Get Octagon API Key

1. Sign up at https://app.octagonai.co/signup/?redirectToAfterSignup=https://app.octagonai.co/api-keys
2. Navigate to **API Keys** in the left menu
3. Generate a new API key
4. Save the key securely

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

## Verify Setup

1. Refresh the MCP server list in Cursor
2. The `octagon-agent` tool should appear in available tools
3. Test with a simple query:
   ```
   Retrieve the current stock price for AAPL
   ```

## Available Tools

The Octagon MCP provides these tools:

| Tool | Description |
|------|-------------|
| `octagon-agent` | Comprehensive market intelligence (SEC filings, earnings, financials, stock data) |
| `octagon-scraper-agent` | Extract structured data from financial websites |
| `octagon-deep-research-agent` | Aggregate research from multiple sources |

## Troubleshooting

**API Key Issues**: Verify the key is correctly set in the command string with no extra spaces.

**Connection Issues**: Ensure you have internet connectivity and the Octagon API is accessible.

**Rate Limiting**: Reduce query frequency if encountering rate limit errors.

## Documentation

Full documentation: https://docs.octagonagents.com
