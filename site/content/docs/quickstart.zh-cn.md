---
title: "🚀 快速开始"
weight: 1
cascade:
  type: docs
breadcrumbs: false
---

## 安装

{{< dino type="error">}}
WowPaper采用使用"wlr-protocols"拓展协议实现窗口置底  
因此只能在支持该协议的合成器上(如hyprland)工作  
无法在不支持"wlr-protocols"协议的合成器或桌面环境(如GNOME)上工作
{{< /dino >}}

{{< tabs items="AUR" >}}

{{< tab >}}

```bash
paru -S wowpaper
```

{{< /tab >}}

{{< /tabs >}}

{{< cards cols="1" >}}
{{< card link="https://github.com/dty2/WowPaper/releases" title="󱍢  Github Release" >}}
{{< card link="../dev/build_and_install.md" title="󱍢  Local Build" >}}
{{< /cards >}}

## 使用

{{% steps %}}

### 在壁纸列表中添加壁纸

1. 在`$HOME/.config/wow`中创建壁纸列表"xxx"

```bash
mkdir $HOME/.config/wow/xxx
```

2. 将您的壁纸"zzz.mp4"放到壁纸列表"xxx"中

```bash
mv zzz.mp4 $HOME/.config/wow/xxx/zzz.mp4
```

{{< dino type="tip" >}}
**您是否在寻找以下内容?**

- [什么是壁纸列表?](../usr-doc/faq.md#什么是壁纸列表)
- [壁纸列表只能有一个吗?](../usr-doc/faq.md#壁纸列表只能有一个吗)
- [我可以在其他目录位置创建壁纸列表吗](../usr-doc/faq.md#可以在其他目录位置创建壁纸列表吗)
- [壁纸列表可以分散放置吗?](../usr-doc/faq.md#壁纸列表可以分散放置吗)

{{< /dino >}}

### 编写配置文件

1. 使用下列命令创建配置文件

```bash
touch $HOME/.config/wow/config.toml
```

2. 填写配置如下(壁纸列表为"xxx", 壁纸名为"zzz.mp4")  
   该配置效果为: 循环播放壁纸zzz.mp4

```toml
startlist = "xxx"

[xxx]
dir = "./xxx"
time = -1
order = ["zzz.mp4"]
```

{{< dino type="tip" >}}
**您是否在寻找以下内容?**

- [配置文件模板有木有?](../usr-doc/template.md)
- [这些配置选项都什么意思?](../usr-doc/faq.md#这些配置选项都什么意思)
- [配置文件位置可以自行更换吗?](../usr-doc/faq.md#配置文件位置可以自行更换吗)

{{< /dino >}}

### 启动!

```bash
wow-daemon
```

😄 大功告成!!!

{{< dino type="tip" >}}
**您是否在寻找以下内容?**

- [制作目的?](../usr-doc/faq.md#制作目的)
- [优势何在?](../usr-doc/faq.md#优势何在)
- [用户文档?](../usr-doc)
- [开发文档?](../usr-doc)

{{< /dino >}}

{{% /steps %}}
