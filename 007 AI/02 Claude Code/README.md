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

#### Docker
```powershell
@'
FROM ubuntu:latest
RUN apt update -y \
    && apt install -y gpg sudo wget curl \
    && install -dm 755 /etc/apt/keyrings \
    && wget -qO - https://mise.jdx.dev/gpg-key.pub | gpg --dearmor | sudo tee /etc/apt/keyrings/mise-archive-keyring.gpg 1> /dev/null \
    && echo "deb [signed-by=/etc/apt/keyrings/mise-archive-keyring.gpg arch=amd64] https://mise.jdx.dev/deb stable main" | sudo tee /etc/apt/sources.list.d/mise.list \
    && apt update \
    && apt install -y mise \
    && echo 'eval "$(mise activate bash)"' >> ~/.bashrc
'@ > Dockerfile4claude


docker build -f Dockerfile4claude -t claude:1.0 .

rm -r Dockerfile4claude
```