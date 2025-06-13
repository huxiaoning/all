[GitHub](https://github.com/PowerShell/PowerShell)

```powershell
> scoop install pwsh
'pwsh' (7.5.1) was installed successfully!
Notes
-----
Since Scoop uses pwsh.exe internally, to update PowerShell Core itself,
run `scoop update pwsh` from Windows PowerShell, i.e. powershell.exe.

Add PowerShell Core as a explorer context menu by running:
'F:\Scoop\.scoop\apps\pwsh\current\install-explorer-context.reg'
For file context menu, run 'F:\Scoop\.scoop\apps\pwsh\current\install-file-context.reg'
```


### Windows Terminal 集成 pwsh
```powershell
在设置中复制一份Windows PowerShell的配置
名称修改为 PowerShell7
Icon去下载一个,
https://techicons.dev/icons/powershell
或者隐藏Icon也可以

```


下面的作废
<br>

<br>
下载 msi 版本,方便与 IDE 集成
<br>
[PowerShell-7.5.1-win-x64.msi](https://github.com/PowerShell/PowerShell/releases/download/v7.5.1/PowerShell-7.5.1-win-x64.msi)
<br>

```powershell
> notepad $profile
[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://127.0.0.1:7890")

$env:HTTP_PROXY="http://127.0.0.1:7890"
$env:HTTPS_PROXY="http://127.0.0.1:7890"

mise activate pwsh | Out-String | Invoke-Expression

```

<br>
