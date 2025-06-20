### Windows沙盒

### 备用
```powershell
# $env:USERNAME
# C:\Users\WDAGUtilityAccount\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
# C:\Users\WDAGUtilityAccount\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1

cat C:\Users\$env:USERNAME\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
cat C:\Users\$env:USERNAME\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
```
### 脚本 init.ps1
```powershell
$gateway = (Get-NetIPConfiguration).IPv4DefaultGateway.NextHop
$proxy_ip = $gateway
$proxy_port = 7890
$protocol = "http://"

$http_proxy = $protocol + $proxy_ip + ":" + $proxy_port
$proxy = $proxy_ip + ":" + $proxy_port

mkdir C:\Users\$env:USERNAME\Documents\PowerShell\
mkdir C:\Users\$env:USERNAME\Documents\WindowsPowerShell\
echo "[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy(`"$http_proxy`")" > C:\Users\$env:USERNAME\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
echo "[System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy(`"$http_proxy`")" > C:\Users\$env:USERNAME\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
echo "`$env:HTTP_PROXY`=`"$proxy`"" >> C:\Users\$env:USERNAME\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
echo "`$env:HTTP_PROXY`=`"$proxy`"" >> C:\Users\$env:USERNAME\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
echo "`$env:HTTPS_PROXY`=`"$proxy`"" >> C:\Users\$env:USERNAME\Documents\PowerShell\Microsoft.PowerShell_profile.ps1
echo "`$env:HTTPS_PROXY`=`"$proxy`"" >> C:\Users\$env:USERNAME\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1

Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
. $profile


```