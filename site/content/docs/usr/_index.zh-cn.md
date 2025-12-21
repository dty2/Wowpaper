---
title: "📘 用户文档"
weight: 2
cascade:
  type: docs
  params:
    reversePagination: false
breadcrumbs: false
---

## 简介

Wowpaper是一个壁纸播放器(采用Client-Server架构)

其中wow-cli(Client)只负责发送控制命令给wow-daemon

关于控制命令与命令行参数请阅读:

{{< cards cols="1" >}}
{{< card link="./cmd" title="💻 命令" >}}
{{< /cards >}}

而wow-daemon(Server)则负责读取配置和播放壁纸, 处理Client发送的控制命令

关于配置文件请阅读:

{{< cards cols="1" >}}
{{< card link="./config" title="⚙️ 配置" >}}
{{< /cards >}}

## 由来

大学时, 我从X11开始折腾, 后来逐渐转到Wayland

虽然全键盘操作越来越丝滑

但是我却只能呆呆地看着我的室友快乐地使用Steam上的壁纸引擎

并且面对惊艳的壁纸, 我总是不由自主地发出"我靠"的惊叹

无奈, 如此这般~~只因~~我找到的壁纸解决方案(如下)都不合我意

1. 使用[🌐linux-wallpaperengine](https://github.com/Almamu/linux-wallpaperengine)

   > 但是, 仍然需要来自官方的素材, 而我不想花钱

2. 使用[🌐swww](https://github.com/Almamu/linux-wallpaperengine)(如今叫[🌐awww](https://codeberg.org/LGFae/awww))

   > 但是, 仅支持使用gif作为动态壁纸

3. [🌐mpvpaper](https://github.com/GhostNaN/mpvpaper)

   > 但是, 不支持静态壁纸, 且没有切换动画

如今我毕业了, 在家啃老某一天竟然发生了...

<img src="/patrick.gif" style="display: inline-block; vertical-align: top; margin-right: 1em;" />

于是, 我突发奇想地打算做一个壁纸软件

为了让使用这个壁纸软件的用户也能得到来自别人的"我靠"

我为我的软件起名为"Wowpaper", 并寄以希望:

"Use the wowpaper, Be a Wow Maker"
