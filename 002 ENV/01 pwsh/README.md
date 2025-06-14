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
