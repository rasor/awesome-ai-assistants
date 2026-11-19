# [github copilot](https://docs.github.com/en/copilot/)

## 1. prompt interfaces
* vscode (build in)
* cli
* desktop app

---

## 2. cli - copilot

---

## 3. file structure 

### configuration
* Global level: `~\.vscode\setting.json`
* Project level: `.\.mcp.json`
* User level: `.\.vscode\setting.json`

---

## 4. connectors / tools

### 4a. add mcp server

Via VSCode:
* Open Chat: Open Customizations from the Command Palette, then choose MCP Servers.

Via CLI:
```bash
# add mcp
copilot mcp add --transport http my-server https://your-server.example/mcp
# list mcps
copilot mcp list
```

This will add to your `.vscode\setting.json` or you can move it to project level `.mcp.json`

```json
{
  "mcpServers": {
    "my-server": {
      "type": "http",
      "url": "https://your-server.example/mcp",
      "tools": ["*"]
    }
  }
}
```

### 4b. browser

Via [browser extension `GitHub Copilot`](https://chromewebstore.google.com/detail/github-copilot/hblomdgalaelcilcdepgohfcogjiijhe) your prompt can interact with your current page, e.g.
```bash
# read page header
which page is open in my browser?

# goto url
Open github.com in my browser
```

HowTo [set it up](chrome-extension://hblomdgalaelcilcdepgohfcogjiijhe/gettingStarted.html)

---

