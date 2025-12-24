---
title: "💻 Command"
weight: 1
cascade:
  type: docs
breadcrumbs: false
---

### CLI

| Function Overview                   | Quick Reference | Command Parameters           | Usage Instructions                                                 |
| :---------------------------------- | :-------------- | :--------------------------- | :----------------------------------------------------------------- |
| Play a list of specified wallpapers | [L]ist          | {{< cp-code "wow-cli -l" >}} | Example usage: wow-cli -l wallpaper-list                           |
| Previous                            | [P]revious      | {{< cp-code "wow-cli -p" >}} | Play the previous wallpaper of the currently playing wallpaper     |
| Next                                | [N]ext          | {{< cp-code "wow-cli -n" >}} | Play the next wallpaper of the currently playing wallpaper         |
| Display information                 | [I]nfo          | {{< cp-code "wow-cli -i" >}} | View currently playing, configure all wallpaper information        |
| Switch playback mode                | [M]ode          | {{< cp-code "wow-cli -m" >}} | Switch between manual and automatic modes                          |
| Refresh configuration               | [R]efresh       | {{< cp-code "wow-cli -r" >}} | Use this command to refresh after modifying the configuration file |
| Test (preview) effect               | [T]est          | {{< cp-code "wow-cli -t" >}} | Example usage: wow-cli -t wallpaper/path                           |
| Help                                | [H]elp          | {{< cp-code "wow-cli -h" >}} | View help                                                          |
| Version                             | [V]ersion       | {{< cp-code "wow-cli -v" >}} | View version                                                       |
| Set working directory               |                 | {{< cp-code "--work-dir" >}} | Default: XDG_RUNTIME_DIR, must be the same as daemon               |
| Set log output type                 |                 | {{< cp-code "--log-type" >}} | Value: STDIO/FILE, commonly used for debugging and testing         |
| Shut down the daemon                | [Q]uit          | {{< cp-code "wow-cli -q" >}} | Graceful exit                                                      |

{{< dino type="info" >}}
**Use cases for `wow-cli -t`:**
When you have an image or video wallpaper and want to quickly preview the effect, you can use this command.
It allows you to check if the wallpaper meets expectations without formally setting it. The preview lasts for 30 seconds.
{{< /dino >}}

{{< dino type="important" >}}
**About `--work-dir`:**
The working directory will contain pid, sock, and log files.
Therefore, the daemon must use the same working directory as the CLI.
Otherwise, it may cause errors and strange problems.
Commonly used for regression testing, and by a very small number of users who want to control the program's runtime location.
So unless absolutely necessary, please do not manually set "--work-dir".
{{< /dino >}}

### Daemon Process

| Function Overview           | Quick Reference | Command Parameters              | Usage Instructions                                         |
| :-------------------------- | :-------------- | :------------------------------ | :--------------------------------------------------------- |
| Set Configuration Directory |                 | {{< cp-code "--config-dir" >}}  | Default: XDG_CONFIG_HOME                                   |
| Set Working Directory       |                 | {{< cp-code "--work-dir" >}}    | Default: XDG_RUNTIME_DIR, must be the same as cli          |
| Set Log Output Type         |                 | {{< cp-code "--log-type" >}}    | Value: STDIO/FILE, commonly used for debugging and testing |
| Help                        | [H]elp          | {{< cp-code "wow-daemon -h" >}} | View Help                                                  |
| Version                     | [V]ersion       | {{< cp-code "wow-daemon -v" >}} | View Version                                               |
