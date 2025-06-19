
- pwsh
- scoop
- windows-terminal
- mise


### 沙盒
```bash
$ mkdir C:\Users\WDAGUtilityAccount\Documents\PowerShell\
$ notepad $profile
[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://172.25.128.1:7890")
$env:HTTP_PROXY="http://172.25.128.1:7890"
$env:HTTPS_PROXY="http://172.25.128.1:7890"

# 重新打开 pwsh
$ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
$ irm get.scoop.sh -outfile 'install.ps1'
$ .\install.ps1

$ scoop alias add ls 'scoop list'

$ scoop config proxy 172.25.128.1:7890

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


```