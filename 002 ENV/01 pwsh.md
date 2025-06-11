
[GitHub](https://github.com/PowerShell/PowerShell)

下载 msi 版本,方便与 IDE 集成

```powershell
> notepad $profile
[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://127.0.0.1:7890")

$env:HTTP_PROXY="http://127.0.0.1:7890"
$env:HTTPS_PROXY="http://127.0.0.1:7890"

mise activate pwsh | Out-String | Invoke-Expression

```