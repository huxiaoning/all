### 搞机
```powershell
adb push Desktop.cer /sdcard/Download

# 把PC的7890端口 转发 到手机上的17890端口 (手机用电脑的流量)
adb reverse tcp:17890 tcp:7890
adb push "F:\PowershellWorkSpace\cloud\dns\xiaomi\adb_reverse_17890.yaml" /sdcard/Download
```


```yaml
proxies:
  - name: adb
    type: socks5
    server: 127.0.0.1
    port: 17890
proxy-groups:
  - name: PROXY
    type: select
    proxies:
      - adb
rules:
  - MATCH,PROXY
```