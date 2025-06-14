```powershell
> [System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://127.0.0.1:7890")

> echo $?
True

> [System.Net.WebRequest]::DefaultWebProxy

Address               : http://127.0.0.1:7890/
BypassProxyOnLocal    : False
BypassList            : {}
BypassArrayList       : {}
Credentials           :
UseDefaultCredentials : False

> irm ifconfig.me
104.160.41.28

# 这个走的系统代理
> iwr -Uri https://www.google.com | Select-Object -Property StatusCode

StatusCode
----------
       200
```
