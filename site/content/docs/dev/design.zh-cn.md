---
title: "设计"
cascade:
  type: docs
  params:
    reversePagination: false
breadcrumbs: false
---

## Basic库

它被打包为一个动态库, 供客户端和守护进程使用

它包括 IPC, 日志, 版本管理, 命令行参数解析以及常用函数

### 工作目录

`--work-dir` 参数指定工作目录 `$WORK_DIR`, 默认值为 `$XDG_RUNTIME_DIR`

### 日志

日志目录位于 `$WORK_DIR/wow/log/`

- 保留：如果程序运行期间日志全部为 INFO, 则日志不会保留
  如果运行期间出现 WARNING 或 ERROR, 则会保留整个日志
- 截断：当日志超过 50MB 时会进行截断, 截断发生时会丢弃截断前的所有日志
- 限流：日志每秒最多允许输出 50 条

### IPC

IPC 使用本地套接字和 JSON 文本实现

本地套接字监听在 `$WORK_DIR/wow/wow.sock`

#### 请求

- refresh: `{ "action": "refresh" }`
- next: `{ "action": "next" }`
- prev: `{ "action": "prev" }`
- manual: `{ "action": "manual" }`
- test:

```
{
  "action": "test",
  "target": "[wallpaper-name]"
}
```

- list:

```
{
  "action": "list",
  "target": "[list-name]"
}
```

- quit: `{ "action": "quit" }`
- info: `{ "action": "info" }`

#### 响应

`{ "result": "[result-info]" }`

## 客户端

实现非常简陋, 甚至有点丑陋

工作内容: 解析命令行, 通过 IPC 与守护进程通信, 实现控制和信息获取

当然也可以使用其他方式实现...

(小声)我的下一个项目会重新利用IPC, 到时候会有一个更漂亮的控制方式, 因此这个项目就只用命令行式客户端了

## 守护进程

这里会有一个图来生动地说明, 因此当你看到这段文字时, 说明我偷懒了...

### 配置目录

默认配置目录在 `$XDG_CONFIG_HOME`, 也就是 `$HOME/.config/`
