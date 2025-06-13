```powershell
# 卸载scoop
# scoop uninstall scoop

# 设置 PowerShell 执行策略为 Unrestricted 、 RemoteSigned 或 ByPass 之一
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

# 创建安装目录
# > f:
# > mkdir Scoop
# > cd Scoop

# 创建两个目录：用户目录和全局目录
# > mkdir .scoop
# > mkdir .global

# 将安装程序写入本地脚本文件 install.ps1
> irm get.scoop.sh -outfile 'install.ps1'

# 安装 (指定安装位置)
# > .\install.ps1 -ScoopDir 'F:\Scoop\.scoop' -ScoopGlobalDir 'F:\Scoop\.global' -NoProxy
> .\install.ps1

> scoop --version
Current Scoop version:
859d1db5 (HEAD -> master, tag: v0.5.2, origin/master, origin/HEAD) chore(release): Bump to version 0.5.2 (#6080)

'main' bucket:
7b485e9b2 (HEAD -> master, origin/master, origin/HEAD) uv: Update to version 0.4.13

> scoop list
There aren't any apps installed.
>
```