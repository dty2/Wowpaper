---
title: "控制"
---

## CLI 命令

```bash
# --------------------------------------------------------------
wow-cli -h --help                       # [H]elp     帮助
wow-cli -v --version                    # [V]ersion  版本
wow-cli -i                              # [I]nfo     显示所有信息(壁纸列表、当前播放状态)
# --------------------------------------------------------------
wow-cli -n                              # [N]ext     下一张壁纸
wow-cli -p                              # [P]revious 上一张壁纸
wow-cli -m                              # [M]anual   手动播放
wow-cli -r                              # [R]efresh  刷新
wow-cli -q                              # [Q]uit     退出(守护进程)
# --------------------------------------------------------------
wow-cli -t [wallpaper name]             # [T]est     预览指定壁纸
wow-cli -l [list name]                  # [L]ist     播放指定的壁纸列表
# --------------------------------------------------------------
wow-cli    --work-dir [config path]     # 设置工作目录(默认是$XDG_RUNTIME_DIR)
wow-cli    --log-type [STDIO/FILE]      # 设置日志输出类型(FILE/STDIO)
```

> [!NOTE]
> `wow-cli -t [wallpaper name]` 的使用场景:
> 当你获得一张图片或视频壁纸并想快速预览效果时, 可以使用此命令
> 它允许你在不正式设置的情况下检查壁纸是否符合预期. 预览持续30秒

## 守护进程命令

```bash
# --------------------------------------------------------------
wow-daemon -h --help                    # 帮助
wow-daemon -v --version                 # 版本
# --------------------------------------------------------------
wow-daemon    --config-dir              # 设置配置目录
wow-daemon    --work-dir [config path]  # 设置工作目录(默认是$XDG_RUNTIME_DIR)
wow-daemon    --log-type [STDIO/FILE]   # 设置日志输出类型(FILE/STDIO)
```
