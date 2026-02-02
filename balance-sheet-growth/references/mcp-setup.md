# Octagon MCP Setup for Cursor

## Prerequisites

Install Node.js (includes npm and npx):

**macOS:**
```bash
brew install node
```

**Windows:**
Download from https://nodejs.org/ (LTS version)

Verify:
```bash
node -v && npm -v && npx -v
```

## Get Octagon API Key

1. Sign up at https://octagonagents.com
2. Navigate to **API Keys** in left menu
3. Generate and save your key

## Configure Cursor

1. Open Cursor Settings
2. Go to **Features > MCP Servers**
3. Click **+ Add New MCP Server**
4. Enter:
   - **Name:** `octagon-mcp`
   - **Type:** `command`
   - **Command:** `env OCTAGON_API_KEY=<your-api-key> npx -y octagon-mcp`

**Windows:**
```
cmd /c "set OCTAGON_API_KEY=<your-api-key> && npx -y octagon-mcp"
```

## Verify

Refresh MCP server list. Test with:
```
Retrieve the current stock price for AAPL
```

## Documentation

https://docs.octagonagents.com
