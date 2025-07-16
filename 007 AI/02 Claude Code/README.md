### Claude

- [claude-code](https://www.anthropic.com/claude-code)
- [anyrouter](https://anyrouter.top/)

```powershell

mise exec node@24 -- npm install -g @anthropic-ai/claude-code
mise exec node@24 -- claude --version

# export ANTHROPIC_AUTH_TOKEN=sk-...
# export ANTHROPIC_BASE_URL=https://anyrouter.top
$env:ANTHROPIC_AUTH_TOKEN=sk-...
$env:ANTHROPIC_BASE_URL=https://anyrouter.top

mise exec node@24 -- claude
```