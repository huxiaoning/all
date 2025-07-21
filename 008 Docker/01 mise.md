### mise

```powershell
@'
FROM ubuntu:latest
WORKDIR /app
RUN apt update -y \
    && apt install -y gpg sudo wget curl \
    && install -dm 755 /etc/apt/keyrings \
    && wget -qO - https://mise.jdx.dev/gpg-key.pub | gpg --dearmor | sudo tee /etc/apt/keyrings/mise-archive-keyring.gpg 1> /dev/null \
    && echo "deb [signed-by=/etc/apt/keyrings/mise-archive-keyring.gpg arch=amd64] https://mise.jdx.dev/deb stable main" | sudo tee /etc/apt/sources.list.d/mise.list \
    && apt update \
    && apt install -y mise \
    && echo 'eval "$(mise activate bash)"' >> ~/.bashrc
'@ > Dockerfile4mise

# 删除旧的镜像
if (docker images -q mise:1.0) { docker rmi mise:1.0 }
# 构建新的镜像
docker build -f Dockerfile4mise -t mise:1.0 .

rm -r Dockerfile4mise


docker run -it --rm mise:1.0 bash
mise version
mise use -g ubi:mthmulders/mcs
mcs search nacos-client
```