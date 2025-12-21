---
title: "Design"
cascade:
  type: docs
  params:
    reversePagination: false
breadcrumbs: false
---

## Basic lib

It is packaged as a dynamic library for use by both the client and daemon

It includes IPC, logging, versioning, command-line argument parsing, and commonly used functions

### WorkDir

The `--work-dir` parameter specifies the working directory `$WORK_DIR`, which defaults to `$XDG_RUNTIME_DIR`.

### Log

The log directory is located at $WORK_DIR/wow/log/

- Retention: If all log entries are INFO during program execution, the log will not be retained.
  If WARNING or ERROR entries appear in the log during program execution, the entire log will be retained.
- Truncating: Log entries exceeding 50MB will be truncated; all log entries before truncation will be discarded.
- Rate Limiting: Only 50 log entries are allowed per second.

### IPC

IPC is implemented using local sockets and JSON text.

The local socket listens on $WORK_DIR/wow/wow.sock

#### Request

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

#### Response

`{ "result": "[result-info]" }`

## Client Side

The implementation is extremely rudimentary, even somewhat ugly

Job Description: Parse command lines and communicate with the Daemon via IPC to achieve control and information retrieval

Other methods could be used...

(Whispering) My next project will reuse IPC, and it will have a more elegant control scheme, so this project will use a command-line client

## Daemon

A diagram will be provided here to illustrate this vividly. Therefore, if you see this text, it means I was lazy...

### Config dir

Default Configuration directory is at `$XDG_CONFIG_HOME`, it is `$HOME/.config/`
