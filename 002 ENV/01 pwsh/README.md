[GitHub](https://github.com/PowerShell/PowerShell)

下载 msi 版本,方便与 IDE 集成
<br>
[PowerShell-7.5.1-win-x64.msi](https://github.com/PowerShell/PowerShell/releases/download/v7.5.1/PowerShell-7.5.1-win-x64.msi)
<br>

```powershell
notepad $profile
[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://127.0.0.1:7890")

$env:HTTP_PROXY="http://127.0.0.1:7890"
$env:HTTPS_PROXY="http://127.0.0.1:7890"

mise activate pwsh | Out-String | Invoke-Expression
```

<br>
### 为什么不使用scoop来安装pwsh?
因为更新不方便,得打开powershell来更新pwsh,不如直接下载msi安装包手动安装


### 沙盒使用缩主机代理
```powershell
notepad $profile
[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://172.25.128.1:7890")

$env:HTTP_PROXY="http://172.25.128.1:7890"
$env:HTTPS_PROXY="http://172.25.128.1:7890"

mise activate pwsh | Out-String | Invoke-Expression



172.25.128.1						----------- 这个是Windows沙盒访问缩主机的IP
用 ipconfig 网关IP就是缩主机IP

PS C:\Users\WDAGUtilityAccount> ipconfig

Windows IP Configuration


Ethernet adapter 以太网:

   Connection-specific DNS Suffix  . : mshome.net
   Link-local IPv6 Address . . . . . : fe80::a3fc:593:8749:a607%202
   IPv4 Address. . . . . . . . . . . : 172.25.134.109
   Subnet Mask . . . . . . . . . . . : 255.255.240.0
   Default Gateway . . . . . . . . . : 172.25.128.1
PS C:\Users\WDAGUtilityAccount>
```