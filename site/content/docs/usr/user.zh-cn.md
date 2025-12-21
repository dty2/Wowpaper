---
title: "用户指南"
---

## 常见命令

- "[I]nfo", 显示所有信息(壁纸列表, 当前播放状态)

```bash
wow-cli -i
```

- "[N]ext", 下一张壁纸

```bash
wow-cli -n
```

- "[P]revious", 上一张壁纸

```bash
wow-cli -p
```

- "[M]anual", 手动播放

```bash
wow-cli -m
```

- "[R]efresh", 刷新

```bash
wow-cli -r
```

- "[Q]uit", 退出(守护进程)

```bash
wow-cli -q
```

- "[T]est", 预览指定壁纸

```bash
wow-cli -t [wallpaper name]
```

- "[L]ist", 播放指定的壁纸列表

```bash
wow-cli -l [list name]
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

{{< callout type="error" >}}
在工作目录中会有pid, sock和log文件
因此, 守护进程必须与 CLI 使用相同的工作目录
否则可能会导致错误和奇怪的问题
所以除非绝对必要, 请不要手动设置"--work-dir"
{{< /callout >}}
