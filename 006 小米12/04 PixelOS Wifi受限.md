### PixelOS Wifi受限

```powershell
adb shell settings put global captive_portal_mode 0

# 其实上面那一条命令就行了，下面的是网上搜索到的，备份下吧
adb shell settings put global captive_portal_http_url http://captive.v2ex.co/generate_204
adb shell settings put global captive_portal_https_url http://captive.v2ex.co/generate_204
```