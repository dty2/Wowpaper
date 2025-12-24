---
title: "⚙️ 配置"
weight: 3
cascade:
  type: docs
breadcrumbs: false
---

```toml
# 这里填入你希望最开始播放的壁纸列表
startlist = ""

#这里填入你的壁纸列表
[]

# 这里填入你的壁纸列表的目录
# 相对路径和绝对路径都可以
# 相对路径只能相对于配置目录
# 配置目录默认值是"$HOME/.config/wow/"
# 例子:
# dir = "./aaa" ✅: 绝对路径是 $HOME/.config/wow/aaa
# dir = "/home/yourname/wallpapers/bbb" ✅ 支持绝对路径
# dir = "$HOME/wallpapers/ccc" ✅: 支持环境变量
dir = ""

# 该项不设置则设置默认值(-1)
# -1 表示手动控制壁纸的切换
# 如果设置为60(或其他整数值), 那么表示为自动切换
# 并且每张壁纸播放60秒就切换下一个
# 例子:
# time = -1 ✅: 手动模式
# time = 30 ✅: 自动播放, 每张壁纸播放30秒
# time = 30.5 ❎
# time = -2 ❎
# time = -30 ❎
time = -1

# 该项也可以不设置
# 不设置或置空, 表示没有顺序要求
# 此时按照加载顺序播放壁纸
# 而order不为空时, 按照order列表中壁纸顺序播放壁纸
# 未填入的壁纸即使在壁纸列表(目录)中也不会播放
# 必须写文件全名, 如果有文件后缀则必须将后缀写上
# 例子:
# order = [
#   "aaa.webm",
#   "bbb", --> 没有文件后缀, 但实际文件类型是webp
#   "eee.webp"
# ] ✅: play order: aaa, bbb, eee
# order = [] ✅: 置空也是可以的
# order = [
#   "aaa.jjj", --> aaa.jjj 是png文件
# ] ✅: 实际文件类型决定是否可用
# order = [
#   "aaa", --> aaa.png is full file name
# ] ❎: 必须写文件全名, 如果有文件后缀则必须将后缀写上
order = []

# 你可以有多个壁纸列表
# 并且如你所见, xxx播放列表只设置了必要项
["xxx"]
dir = "./xxx"

["yyy"]
dir = "./yyy"
time = 40
```
