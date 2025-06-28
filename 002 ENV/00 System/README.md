### 系统

- [Ventoy](https://www.ventoy.net/cn/index.html)
- [微PE](https://www.wepe.com.cn/)
- [Win11](https://www.freedidi.com/13121.html)
- DiskGenius

- 安装完系统后用 DiskGenius 做全量C盘备份
- 安装完打印机驱动后用 DiskGenius 做C盘增量备份

### 🔧 实际使用方法（推荐操作流程）：

将微PE ISO 放进 Ventoy U 盘

比如：WePE_64.iso

插上 U 盘 → 电脑启动选择 Ventoy → 选择 WePE 启动

进入微PE 环境

打开你熟悉的备份工具（DiskGenius、Dism++、Ghost）

还原你之前保存在其它磁盘或U盘上的镜像文件

.wim → 用 Dism++

.gho → 用 Ghost

.img → 用 DiskGenius

完成后重启，拔掉U盘，系统恢复成功

```
scoop install ventoy
scoop install anyburn
```
### 开机启动按键
- 华硕
  - 按 F2 或者 DEL
- 惠普
  - 按 ESC 

### 激活
```bash
irm https://massgrave.dev/get | iex
https://gravesoft.dev/
# 下载office365 选择那个带星星的
https://gravesoft.dev/office_c2r_links#chinese-simplified-zh-cn
https://github.com/gravesoft/CAS
```

### 驱动
[驱动人生海外版](https://www.drivethelife.com/)
```powershell
# 还是这个靠普些
scoop bucket add xrgzs_sdoog https://github.com/xrgzs/sdoog
scoop install xrgzs_sdoog/iobit-driver-booster
```
