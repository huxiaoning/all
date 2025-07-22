### yt-dlp
#### 01 [命令行](https://github.com/yt-dlp/yt-dlp)
```powershell
scoop install yt-dlp
# 必须撤底关闭浏览器，否则读不到cookie无法登录，如果想不关闭chrome也可以下载
# 推荐安装这个插件，可以不关闭chrome https://github.com/seproDev/yt-dlp-ChromeCookieUnlock
# 插件安装方法 https://github.com/yt-dlp/yt-dlp#installing-plugins
# 存放位置 ${APPDATA}/yt-dlp/plugins/yt-dlp-ChromeCookieUnlock/yt_dlp_plugins/
# 存放位置 C:\Users\huxiaoning\AppData\Roaming\yt-dlp\plugins\yt-dlp-ChromeCookieUnlock
yt-dlp https://www.youtube.com/watch?v=RhOo9wQMxeQ --cookies-from-browser chrome

```

#### 02 [GUI](https://github.com/oleksis/youtube-dl-gui)
```powershell
# 安装完以后程序名是 yt-dlg.exe
scoop install youtube-dl-gui
```


#### 03 media-downloader
```powershell
scoop install media-downloader
```