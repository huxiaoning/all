### yt-dlp
#### 01 [命令行](https://github.com/yt-dlp/yt-dlp)
```powershell
scoop install yt-dlp

yt-dlp --proxy socks5://127.0.0.1:7890 "https://www.youtube.com/watch?v=Rz__ODnIhLg&list=PLADrJe98EUfE8en2t7yxGwoGZUlG2yTMQ"

[youtube:tab] Extracting URL: https://www.youtube.com/watch?v=Rz__ODnIhLg&list=PLADrJe98EUfE8en2t7yxGwoGZUlG2yTMQ
[youtube:tab] Downloading playlist PLADrJe98EUfE8en2t7yxGwoGZUlG2yTMQ - add --no-playlist to download just the video Rz__ODnIhLg
[youtube:tab] PLADrJe98EUfE8en2t7yxGwoGZUlG2yTMQ: Downloading webpage
WARNING: [youtube:tab] Unable to download webpage: HTTP Error 429: Too Many Requests (caused by <HTTPError 429: Too Many Requests>)
[youtube:tab] PLADrJe98EUfE8en2t7yxGwoGZUlG2yTMQ: Downloading API parameters API JSON
[youtube:tab] PLADrJe98EUfE8en2t7yxGwoGZUlG2yTMQ: Downloading API JSON
WARNING: [youtube:tab] Unable to recognize playlist. Downloading just video Rz__ODnIhLg
[youtube] Extracting URL: https://www.youtube.com/watch?v=Rz__ODnIhLg
[youtube] Rz__ODnIhLg: Downloading webpage
WARNING: [youtube] Unable to download webpage: HTTP Error 429: Too Many Requests (caused by <HTTPError 429: Too Many Requests>)
[youtube] Rz__ODnIhLg: Downloading tv client config
[youtube] Rz__ODnIhLg: Downloading tv player API JSON
[youtube] Rz__ODnIhLg: Downloading ios player API JSON
[youtube] Rz__ODnIhLg: Downloading web player API JSON

ERROR: [youtube] Rz__ODnIhLg: Sign in to confirm you’re not a bot. Use --cookies-from-browser or --cookies for the authentication. 
See  https://github.com/yt-dlp/yt-dlp/wiki/FAQ#how-do-i-pass-cookies-to-yt-dlp  for how to manually pass cookies. 
Also see  https://github.com/yt-dlp/yt-dlp/wiki/Extractors#exporting-youtube-cookies  for tips on effectively exporting YouTube cookies
```

#### 02 [GUI](https://github.com/oleksis/youtube-dl-gui)
```powershell
scoop install youtube-dl-gui
```