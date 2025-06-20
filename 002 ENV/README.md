
- pwsh
- scoop
- windows-terminal
- mise


### 沙盒
```bash
$gateway = (Get-NetIPConfiguration).IPv4DefaultGateway.NextHop
$proxyIP = $gateway
$proxy = "http://"+$proxyIP+":7890"

$ mkdir C:\Users\WDAGUtilityAccount\Documents\PowerShell\
$ notepad $profile
[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy($proxy)
$env:HTTP_PROXY=$proxy
$env:HTTPS_PROXY=$proxy

# 重新打开 pwsh
$ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
$ irm get.scoop.sh -outfile 'install.ps1'
$ .\install.ps1

$ scoop alias add ls 'scoop list'

$ scoop config proxy $proxy

$ scoop install 7zip
C:\Users\WDAGUtilityAccount\scoop\apps\7zip\current\install-context.reg

$ scoop install git
git config --global credential.helper manager
C:\Users\WDAGUtilityAccount\scoop\apps\git\current\install-context.reg
C:\Users\WDAGUtilityAccount\scoop\apps\git\current\install-file-associations.reg

$ scoop install aria2
scoop config aria2-enabled false
scoop config aria2-warning-enabled false

$ scoop bucket add extras
$ scoop bucket add versions

$ scoop install windows-terminal
$ reg import "C:\Users\WDAGUtilityAccount\scoop\apps\windows-terminal\current\install-context.reg"
$ scoop install extras/vcredist2022

$ scoop install mise
$ mise use -g java@24 maven@3 node@10

$ scoop install idea-ultimate
```