---
title: "📘 Usr Doc"
weight: 2
cascade:
  type: docs
  params:
    reversePagination: false
breadcrumbs: false
---

## Introduction

Wowpaper is a wallpaper player(Adopting a Client-Server architecture)

wow-cli(Client) is only responsible for sending control commands to wow-daemon

For information on control commands and command-line parameters, please read:

{{< cards cols="1" >}}
{{< card link="./cmd" title="💻 Command" >}}
{{< /cards >}}

The wow-daemon (Server) is responsible for reading the configuration,
playing the wallpaper, and processing the control commands sent by the client

For configuration file please read:

{{< cards cols="1" >}}
{{< card link="./config" title="⚙️ Configuration" >}}
{{< /cards >}}

## Origin

Back in college, I started tinkering with X11, and later gradually moved over to Wayland.

Although my full‑keyboard control becoming smoother and smoother,
but all I could do was sit there blankly, watching my roommate happily play with Steam’s Wallpaper Engine.

Whenever I saw those stunning wallpapers, I couldn’t help blurting out in amazement: "Holy shit!"

Because, the wallpaper solutions that I found never quite satisfied me:

1. Using [🌐linux-wallpaperengine](https://github.com/Almamu/linux-wallpaperengine)

   > But, still relies on official assets. And I didn’t want to spend money

2. Using [🌐swww](https://github.com/Almamu/linux-wallpaperengine)(now renamed [🌐awww](https://codeberg.org/LGFae/awww))

   > But, only supports GIFs as animated wallpapers

3. Using [🌐mpvpaper](https://github.com/GhostNaN/mpvpaper)

   > But, doesn’t support static wallpapers. And lacks transition animations

After graduation, while idling at home one day…

<img src="/patrick.gif" style="display: inline-block; vertical-align: top; margin-right: 1em;" />

A sudden spark hit me: why not make my own wallpaper software?

In order to allow users who use this wallpaper software to also get "Holy Shit!" from others

So I named my project "Wowpaper", carrying the hope:

"Use the wowpaper, Be a Wow Maker"
