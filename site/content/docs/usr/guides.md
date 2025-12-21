+++
date = '2025-12-13T20:11:41+08:00'
title = "Guides"
+++

# Guides

> [!IMPORTANT]
> There are pid, sock and log file in work dir
> Thus, daemon must have the same work dir with cli
> Otherwise, it may lead to errors and strange things
> So unless absolutely necessary, do not manually set "--work-dir" manually

## CLI command

```bash
# --------------------------------------------------------------
wow-cli -h --help                       # [H]elp     help
wow-cli -v --version                    # [V]ersion  version
wow-cli -i                              # [I]nfo     Show all information (wallpaper lists, current playback status)
# --------------------------------------------------------------
wow-cli -n                              # [N]ext     Next wallpaper
wow-cli -p                              # [P]revious Previous wallpaper
wow-cli -m                              # [M]anual   Manual playback
wow-cli -r                              # [R]efresh  Refresh
wow-cli -q                              # [Q]uit     Quit (daemon)
# --------------------------------------------------------------
wow-cli -t [wallpaper name]             # [T]est     Preview a wallpaper
wow-cli -l [list name]                  # [L]ist     Play a specified list
# --------------------------------------------------------------
wow-cli    --work-dir [config path]     # set work dir(default is $XDG_RUNTIME_DIR)
wow-cli    --log-type [STDIO/FILE]      # set log output type(FILE/STDIO)
```

> [!NOTE]
> Usage scenario for `wow-cli -t [wallpaper name]`:
> When you obtain an image or video wallpaper and want to quickly preview its effect, you can use this command.
> It allows you to check whether the wallpaper meets your expectations without formally setting it. The preview lasts for 30 seconds.

## Daemon command

```bash
# --------------------------------------------------------------
wow-daemon  -v --version                # version
wow-daemon  -h --help                   # help
# --------------------------------------------------------------
wow-daemon     --config-dir             # set config dir
wow-daemon     --work-dir [config path] # set work dir(default is $XDG_RUNTIME_DIR)
wow-daemon     --log-type [STDIO/FILE]  # set log output type(FILE/STDIO)
```
