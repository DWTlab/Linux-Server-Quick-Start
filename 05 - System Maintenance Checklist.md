### Software Update & Cleanup

This is your main weekly task. It gets all the latest security patches and feature updates for your system and applications.

| Command                         | Description                                                                                     |
| ------------------------------- | ----------------------------------------------------------------------------------------------- |
| `sudo apt update`               | Refreshes the list of available packages from the system's software sources.                    |
| `sudo apt upgrade -y`           | Upgrades all installed system packages to their newest versions.                                |
| `flatpak update -y`             | Separately, this updates all of your installed Flatpak applications.                            |
| `sudo apt autoremove -y`        | **Recommended.** Removes packages that were installed as dependencies but are no longer needed. |
| `sudo apt clean`                | Clears the local cache of downloaded package files to free up disk space.                       |
| `flatpak uninstall --unused -y` | The Flatpak equivalent of `autoremove`. It removes any unused Flatpak runtimes.                 |

### All-in-One Update Command

For a quick weekly tune-up, you can chain the most common commands together. This single line will update your system, update your flatpaks, and remove any leftover packages.

```bash
sudo apt update && sudo apt upgrade -y && flatpak update -y && sudo apt autoremove -y
```

### System Health & Cleanup

Here are three key commands for checking system health and clearing out old files.

#### Check for Failed Services

This is the most important health check. It will tell you if any background processes have crashed or failed to start. An empty output from this command is a good sign.

```bash
systemctl --failed
```

#### Clean Up System Logs

Over time, system log files can grow very large. This command will safely shrink the logs to a more manageable size (e.g., 100MB).

```bash
sudo journalctl --vacuum-size=100M
```

#### Empty the Trash

This command will forcefully empty your user's trash can. Be certain before running, as this cannot be undone.

```bash
rm -rf ~/.local/share/Trash/files/*
```