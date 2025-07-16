### Claude

- [claude-code](https://www.anthropic.com/claude-code)
- [anyrouter](https://anyrouter.top/)
- [文档](https://docs.anthropic.com/en/docs/claude-code/overview)


```bash
# WSL
mise exec node@24 -- npm install -g socks-proxy-agent --registry=https://registry.npmmirror.com
mise exec node@24 -- npm config set proxy socks://172.20.20.208:7890
mise exec node@24 -- npm config set https-proxy socks://172.20.20.208:7890

mise exec node@24 -- npm install -g @anthropic-ai/claude-code
mise exec node@24 -- claude --version
# export ANTHROPIC_AUTH_TOKEN=sk-...
export ANTHROPIC_BASE_URL=https://anyrouter.top
mise exec node@24 -- claude
```

```powershell

mise exec node@24 -- npm install -g @anthropic-ai/claude-code
mise exec node@24 -- claude --version

# export ANTHROPIC_AUTH_TOKEN=sk-...
# export ANTHROPIC_BASE_URL=https://anyrouter.top
$env:ANTHROPIC_AUTH_TOKEN=sk-...
$env:ANTHROPIC_BASE_URL=https://anyrouter.top
$env:CLAUDE_CODE_GIT_BASH_PATH=F:\Scoop\.scoop\apps\git\current\bin\bash.exe

mise exec node@24 -- claude
```