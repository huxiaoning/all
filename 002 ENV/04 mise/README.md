### 安装

```powershell
> scoop install mise
```

### 配置环境变量

```powershell
> Get-ChildItem Env: | grep MISE_ALWAYS_KEEP_DOWNLOAD
MISE_ALWAYS_KEEP_DOWNLOAD      true

> Get-ChildItem Env: | grep MISE
MISE_ACTIVATE_AGGRESSIVE       true
MISE_ALWAYS_KEEP_DOWNLOAD      true
MISE_ALWAYS_KEEP_INSTALL       false
MISE_DATA_DIR                  F:\mise
MISE_GLOBAL_CONFIG_FILE        F:\mise\config.toml

# MISE_FISH_AUTO_ACTIVATE		
```

### 安装Java

```pwsh
# 安装mise托管的java版本
> mise install java@22 maven@3
> mise uninstall java@22

# 安装未经托管的版本
# oracle java8 下载地址
# https://www.oracle.com/java/technologies/downloads/archive/
# oracle java@8 需要自已下载并连接
> mise link java@8 --force "F:\developerInstall\Java\jdk1.8.0_441"
> mise uninstall java@8
```

