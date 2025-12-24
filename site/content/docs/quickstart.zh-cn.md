---
title: "🚀 快速开始"
weight: 1
cascade:
  type: docs
breadcrumbs: false
---

## 安装

{{< dino type="important">}}
**重要:**  
WowPaper采用使用"wlr-protocols"拓展协议实现窗口置底  
因此只能在支持该协议的合成器上(如hyprland)工作  
无法在不支持"wlr-protocols"协议的合成器或桌面环境(如GNOME)上工作
{{< /dino >}}

目前有三种方式可以安装Wowpaper

1. 如果你使用Arch, 你可以使用包管理器来安装

{{< tabs items="AUR" >}}

{{< tab >}}

```bash
paru -S wowpaper
```

{{< /tab >}}

{{< /tabs >}}

2. 对于他系统上, 你可以在Github Release中下载二进制文件

{{< cards cols="1" >}}
{{< card link="https://github.com/dty2/WowPaper/releases" title="Github Release" >}}
{{< /cards >}}

3. 或者, 你也可以克隆仓库并自己构建

```bash
git clone git@github.com:dty2/Wowpaper.git
```

{{< cards cols="1" >}}
{{< card link="./dev/build" title="Local Build" >}}
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

### 启动!

```bash
wow-daemon
```

😄 大功告成!!!

{{< dino type="info" >}}
**提示:**  
获得更多帮助请阅读[📘用户文档](./usr)
{{< /dino >}}

{{% /steps %}}
