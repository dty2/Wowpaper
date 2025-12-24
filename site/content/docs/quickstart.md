---
title: "🚀 Quick Start"
weight: 1
cascade:
  type: docs
breadcrumbs: false
---

## Install

{{< dino type="important" >}}
**Important:**  
WowPaper uses the wlr-protocols extended protocol to realize window bottoming  
Therefore only works on Compositor that support this protocol (such as hyprland)  
Can't work at the Compositor and Desktop Environments(such as GNOME) which are not support "wlr-protocols"  
{{< /dino >}}

There are three ways to install Wowpaper now

1. If you use Arch, you can use package manager to install

{{< tabs items="AUR" >}}

{{< tab >}}

```bash
paru -S wowpaper
```

{{< /tab >}}

{{< /tabs >}}

2. For other system, you can download bin file in release

{{< cards cols="1" >}}
{{< card link="https://github.com/dty2/WowPaper/releases" title="Github Release" >}}
{{< /cards >}}

3. Or, you can clone respository and build your self

```bash
git clone git@github.com:dty2/Wowpaper.git
```

{{< cards cols="1" >}}
{{< card link="./dev/build" title="Local Build" >}}
{{< /cards >}}

## Use

{{% steps %}}

### Add wallpaper to wallpaper list

1. Create a wallpaper list "xxx" in `$HOME/.config/wow`

```bash
mkdir $HOME/.config/wow/xxx
```

2. Put your wallpaper "zzz.mp4" into the wallpaper list "xxx"

```bash
mv zzz.mp4 $HOME/.config/wow/xxx/zzz.mp4
```

### Edit Configuration File

1. Use these command to create Configuration File

```bash
touch $HOME/.config/wow/config.toml
```

2. Fill in the configuration as follows  
   (wallpaper list is "xxx", wallpaper name is "zzz.mp4")  
   This configuration effect: Looping wallpaper zzz.mp4

```toml
startlist = "xxx"

[xxx]
dir = "./xxx"
time = -1
order = ["zzz.mp4"]
```

### Launch!

```bash
wow-daemon
```

😄 Done!!!

{{< dino type="info" >}}
**Tip:**  
Get more help please read [📘Usr Doc](./usr)
{{< /dino >}}

{{% /steps %}}
