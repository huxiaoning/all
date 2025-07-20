### sdkman

```powershell
@'
FROM ubuntu:latest
WORKDIR /app
RUN apt update -y \
    && apt install -y curl zip unzip \
    && curl -s "https://get.sdkman.io" | bash
'@ > Dockerfile4sdkman

# 删除旧的镜像
if (docker images -q sdkman:1.0) { docker rmi sdkman:1.0 }
# 构建新的镜像
docker build -f Dockerfile4sdkman -t sdkman:1.0 .

rm -r Dockerfile4sdkman


docker run -it --rm sdkman:1.0 bash
sdk version
sdk install mcs

```