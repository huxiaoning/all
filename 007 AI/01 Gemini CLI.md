### [Gemini CLI](https://github.com/google-gemini/gemini-cli)

#### Quickstart
```powershell
npx https://github.com/google-gemini/gemini-cli
# 或者
npm install -g @google/gemini-cli
gemini
```

#### mise
```powershell
mise exec node@24 -- npx https://github.com/google-gemini/gemini-cli
# 或者
mise exec node@24 -- npm install -g @google/gemini-cli
mise exec node@24 -- gemini
```

#### docker
```powershell
#docker pull jdxcode/mise:latest
#docker run -it --rm --name mise jdxcode/mise:latest mise exec node@24 -- npx https://github.com/google-gemini/gemini-cli
#docker run jdxcode/mise x node@24 -- npx https://github.com/google-gemini/gemini-cli

#docker pull ubuntu:latest
#docker run -it --rm --name ubuntu ubuntu:latest bash
#apt update -y
#apt install -y curl
#curl https://mise.run | sh
#/root/.local/bin/mise exec node@24 -- npm install -g @google/gemini-cli
#/root/.local/bin/mise exec node@24 -- gemini

docker run -it --rm --name ubuntu ubuntu:latest bash
apt update -y
apt install -y gpg sudo wget curl
install -dm 755 /etc/apt/keyrings
wget -qO - https://mise.jdx.dev/gpg-key.pub | gpg --dearmor | sudo tee /etc/apt/keyrings/mise-archive-keyring.gpg 1> /dev/null
echo "deb [signed-by=/etc/apt/keyrings/mise-archive-keyring.gpg arch=amd64] https://mise.jdx.dev/deb stable main" | sudo tee /etc/apt/sources.list.d/mise.list
apt update
apt install -y mise

mise exec node@24 -- npx https://github.com/google-gemini/gemini-cli
# 或者
mise exec node@24 -- npm install -g @google/gemini-cli
GEMINI_API_KEY=https://aistudio.google.com/apikey
mise exec node@24 -- gemini
```

```dockerfile
FROM ubuntu:latest
RUN apt update -y \
    && apt install -y gpg sudo wget curl \
    && install -dm 755 /etc/apt/keyrings \
    && wget -qO - https://mise.jdx.dev/gpg-key.pub | gpg --dearmor | sudo tee /etc/apt/keyrings/mise-archive-keyring.gpg 1> /dev/null \
    && echo "deb [signed-by=/etc/apt/keyrings/mise-archive-keyring.gpg arch=amd64] https://mise.jdx.dev/deb stable main" | sudo tee /etc/apt/sources.list.d/mise.list \
    && apt update \
    && apt install -y mise \
    && echo 'eval "$(mise activate bash)"' >> ~/.bashrc
```
```powershell
docker build -t mise:1.0 .
docker run -it --rm --name mise mise:1.0 bash

mise ls
mise use -g node@24
mise set -g GEMINI_API_KEY=https://aistudio.google.com/apikey
npm install -g @google/gemini-cli
gemini
```