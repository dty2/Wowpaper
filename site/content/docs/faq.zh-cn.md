---
title: "💡 FAQ"
weight: 5
cascade:
  type: docs
breadcrumbs: false
---

## 壁纸列表是什么

本质上是放置多个壁纸的目录

类似流媒体音乐软件中的歌单

本软件通过壁纸列表组织壁纸并播放

## 壁纸列表只能有一个吗

可以有多个

比如在`$HOME/.config/wow`中创建壁纸列表"aaa", "bbb"还有"ccc"

```bash
cd $HOME/.config/wow/
mkdir aaa bbb ccc
```

## 可以在其他目录位置创建壁纸列表吗

可以, 在配置文件中强制指定某壁纸列表的目录位置

因此可以放到任意目录下, 不用必须放到`$HOME/.config/wow`下

## 壁纸列表可以分散放置吗

可以, 在配置文件中强制指定某壁纸列表的目录位置

因此不要求所有的壁纸列表放在统一的目录下

即, 可以实现如下效果

- 壁纸列表xxx在`$HOME/.config/wow`目录
- 壁纸列表yyy在`$HOME/y/`目录
- 壁纸列表zzz在`$HOME/z/`目录
