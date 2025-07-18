### [JetBrains](https://github.com/JetBrains/mcp-jetbrains)

#### Gemini CLI
```bash
$ vim .gemini/extensions/my-extension/gemini-extension.json
{
  "name": "my-extension",
  "version": "1.0.0",
  "mcpServers": {
    "jetbrains": {
      "command": "npx",
      "args": [
        "-y",
        "@jetbrains/mcp-proxy"
      ]
    },
    "time": {
      "command": "uvx",
      "args": [
        "mcp-server-time",
        "--local-timezone=America/New_York"
      ]
    }
  },
  "contextFileName": "GEMINI.md",
  "excludeTools": [
    "run_shell_command"
  ]
}
```


### Sugment Code
```
npx -y @jetbrains/mcp-proxy
```