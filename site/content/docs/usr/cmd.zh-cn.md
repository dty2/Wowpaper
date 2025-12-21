---
title: "💻 命令"
weight: 1
cascade:
  type: docs
breadcrumbs: false
---

### CLI

| 功能概述         | 速记       | 命令参数                     | 使用说明                                |
| :--------------- | :--------- | :--------------------------- | :-------------------------------------- |
| 播放指定壁纸列表 | [L]ist     | {{< cp-code "wow-cli -l" >}} | 使用示例: wow-cli -l wallpaper-list     |
| 上一张           | [P]revious | {{< cp-code "wow-cli -p" >}} | 播放正在放映的壁纸的上一张              |
| 下一张           | [N]ext     | {{< cp-code "wow-cli -n" >}} | 播放正在放映的壁纸的下一张              |
| 显示信息         | [I]nfo     | {{< cp-code "wow-cli -i" >}} | 查看当前播放, 配置信所有壁纸信息        |
| 切换播放模式     | [M]ode     | {{< cp-code "wow-cli -m" >}} | 在手动/自动两种模式间切换的开关         |
| 刷新配置         | [R]efresh  | {{< cp-code "wow-cli -r" >}} | 当你修改配置文件后使用该命令刷新        |
| 测试(预览)效果   | [T]est     | {{< cp-code "wow-cli -t" >}} | 使用示例: wow-cli -t wallpaper/path     |
| 帮助             | [H]elp     | {{< cp-code "wow-cli -h" >}} | 查看帮助                                |
| 版本             | [V]ersion  | {{< cp-code "wow-cli -v" >}} | 查看版本                                |
| 设置工作目录     |            | {{< cp-code "--work-dir" >}} | 默认: XDG_RUNTIME_DIR, 必须与daemon相同 |
| 设置日志输出类型 |            | {{< cp-code "--log-type" >}} | 值: STDIO/FILE, 常用于调试和测试        |
| 关闭守护进程     | [Q]uit     | {{< cp-code "wow-cli -q" >}} | 优雅退出                                |

{{< dino type="info" >}}
**`wow-cli -t`的使用场景:**  
当你获得一张图片或视频壁纸并想快速预览效果时, 可以使用此命令  
它允许你在不正式设置的情况下检查壁纸是否符合预期. 预览持续30秒
{{< /dino >}}

{{< dino type="important" >}}
**关于`--work-dir`:**  
在工作目录中会有pid, sock和log文件  
因此, 守护进程必须与 CLI 使用相同的工作目录  
否则可能会导致错误和奇怪的问题  
常用于回归测试, 以及极少数想要控制程序运行时位置的用户  
所以除非绝对必要, 请不要手动设置"--work-dir"
{{< /dino >}}

### 守护进程

| 功能概述         | 速记      | 命令参数                        | 使用说明                             |
| :--------------- | :-------- | :------------------------------ | :----------------------------------- |
| 设置配置目录     |           | {{< cp-code "--config-dir" >}}  | 默认: XDG_CONFIG_HOME                |
| 设置工作目录     |           | {{< cp-code "--work-dir" >}}    | 默认: XDG_RUNTIME_DIR, 必须与cli相同 |
| 设置日志输出类型 |           | {{< cp-code "--log-type" >}}    | 值: STDIO/FILE, 常用于调试和测试     |
| 帮助             | [H]elp    | {{< cp-code "wow-daemon -h" >}} | 查看帮助                             |
| 版本             | [V]ersion | {{< cp-code "wow-daemon -v" >}} | 查看版本                             |
