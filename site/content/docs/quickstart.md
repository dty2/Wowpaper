---
title: "🚀 Quick Start"
weight: 1
cascade:
  type: docs
breadcrumbs: false
---

## Install

{{< dino type="error" >}}
WowPaper uses the wlr-protocols extended protocol to realize window bottoming  
Therefore only works on Compositor that support this protocol (such as hyprland)  
Can't work at the Compositor and Desktop Environments(such as GNOME) which are not support "wlr-protocols"  
{{< /dino >}}

{{< tabs items="AUR" >}}

{{< tab >}}

```bash
paru -S wowpaper
```

{{< /tab >}}

{{< /tabs >}}

{{< cards cols="1" >}}
{{< card link="https://github.com/dty2/WowPaper/releases" title=" Github Release" >}}  
{{< card link="/../dev/build_and_install" title="󱑥 Local Build" >}}
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

{{< dino type="tip" >}}
**Are you looking for these?**

- [what is wallpaper list?](../usr/faq#what-is-wallpaper-list)
- [Can a wallpaper list only have one?](../usr/faq#Can-a-wallpaper-list-only-have-one)
- [Can I create wallpaper lists in other directory locations?](../usr/faq#Can-I-create-wallpaper-lists-in-other-directory-locations)
- [Can the wallpaper list be arranged in a scattered manner?](../usr/faq#Can-the-wallpaper-list-be-arranged-in-a-scattered-manner)

{{< /dino >}}

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

{{< dino type="tip" >}}
**Are you looking for these?**

- [Is there a configuration file template?](../usr/template)
- [What do these configuration options mean?](../usr/faq#What-do-these-configuration-options-mean)
- [Can the configuration file location be changed manually?](../usr/faq#Can-the-configuration-file-location-be-changed-manually)

{{< /dino >}}

### Launch!

```bash
wow-daemon
```

😄 Done!!!

{{< dino type="tip" >}}
**Are you looking for these?**

- [Purpose of creation?](../usr/faq#Purpose-of-creation)
- [Advantages?](../usr/faq#Advantages)
- [User documentation?](../usr)
- [Developer documentation?](../usr)

{{< /dino >}}

{{% /steps %}}
