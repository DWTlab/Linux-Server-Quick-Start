Welcome to your Linux command reference vault. This collection of notes is designed to provide a clear and concise guide for beginners using the Linux terminal.

---

## 🐚 Basic Shell Shortcuts

| Command    | Description                                        |
| ---------- | -------------------------------------------------- |
| `clear`    | Clears all text from the terminal screen.          |
| `history`  | Displays a list of previously used commands.       |
| `!!`       | Executes the very last command you ran.            |
| `exit`     | Closes the current terminal session.               |
| `Ctrl + C` | Force-stops the currently running command.         |
| `Ctrl + Z` | Pauses the current command (can be resumed later). |

---

## 📁 Navigating the Filesystem

| Command          | Description                                                                       |
| ---------------- | --------------------------------------------------------------------------------- |
| `pwd`            | **P**rint **W**orking **D**irectory (shows your exact current location).          |
| `ls`             | **L**i**s**ts the files and directories in your current location.                 |
| `ls -la`         | Lists all contents (including hidden `.files`) in a long, detailed format.        |
| `cd <directory>` | **C**hange **D**irectory to the specified path (e.g., `cd /home/user/Documents`). |
| `cd ..`          | Moves you up one directory level.                                                 |
| `cd ~` or `cd`   | Navigates directly to your home directory from anywhere.                          |

---

## 🛠️ Creating, Moving, and Deleting

| Command                     | Description                                                                                           |
| --------------------------- | ----------------------------------------------------------------------------------------------------- |
| `touch <file>`              | Creates a new, empty file with the specified name.                                                    |
| `mkdir <directory>`         | **M**a**k**es a new **dir**ectory.                                                                    |
| `mv <source> <destination>` | **M**o**v**es a file or directory. Also used to rename things (e.g., `mv old_name.txt new_name.txt`). |
| `cp <source> <destination>` | **C**o**p**ies a file or directory. Use `cp -r` to copy a directory and its contents.                 |
| `rm <file>`                 | **R**e**m**oves a file. **This is permanent and cannot be undone.**                                   |
| `rmdir <directory>`         | **R**e**m**oves an *empty* **dir**ectory.                                                             |
| `rm -r <directory>`         | Removes a directory and all of its contents. **Use with extreme caution.**                            |

---

## 📝 Viewing File Contents

| Command       | Description                                                                                                                     |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `cat <file>`  | Con**cat**enates and displays the entire content of a file at once. Best for short files.                                       |
| `less <file>` | Displays the content of a file one page at a time. Use arrow keys to scroll and `q` to quit. Best for long files.               |
| `head <file>` | Displays the first 10 lines of a file. Use `head -n 20` for the first 20 lines.                                                 |
| `tail <file>` | Displays the last 10 lines of a file. Use `tail -n 20` for the last 20 lines, or `tail -f` to watch for new lines in real-time. |

---

## ✏️ Simple File Editing

| Command                     | Description                                                   |
| --------------------------- | ------------------------------------------------------------- |
| `nano <file>`               | Opens a simple, beginner-friendly terminal-based text editor. |
| `vim <file>` or `vi <file>` | Opens the powerful (but more complex) Vim text editor.        |

---

## 🔎 Finding Files and Text

| Command                        | Description                                                                                                    |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| `find <dir> -name "<pattern>"` | Searches for files within a directory (`<dir>`) that match a name (`<pattern>`). E.g., `find . -name "*.txt"`. |
| `grep "<text>" <file>`         | Searches for a specific text pattern inside a file. It prints every line that contains the match.              |
| `grep -r "<text>" <dir>`       | **R**ecursively searches for a text pattern in all files within a directory.                                   |

---

## 💻 System & Resource Information

| Command              | Description                                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `uname -a`           | Prints detailed system information (Kernel version, OS, etc.).                                                                                   |
| `df -h`              | Displays **d**isk **f**ree space usage in a **h**uman-readable format.                                                                           |
| `du -sh <directory>` | Shows the total disk **u**sage of a specific directory in a **s**ummarized, **h**uman-readable format.                                           |
| `free -h`            | Shows the amount of free and used memory (RAM).                                                                                                  |
| `top` or `htop`      | Displays a real-time, dynamic list of running processes and resource usage. `htop` is more user-friendly (install with `sudo apt install htop`). |
| `ip a`               | Shows your network adapter information, including your IP **a**ddress.                                                                           |

---

## ⚙️ Process Management

| Command                  | Description                                                            |
| ------------------------ | ---------------------------------------------------------------------- |
| `ps aux`                 | Displays all currently running processes on the system.                |
| `kill <PID>`             | **Kill**s a process with the specified **P**rocess **ID**.             |
| `killall <process_name>` | Kills all processes with the specified name (e.g., `killall firefox`). |

---

## 👤 User Management

| Command          | Description                                                                 |
| ---------------- | --------------------------------------------------------------------------- |
| `whoami`         | Displays the current user's username.                                       |
| `sudo <command>` | **S**uper**u**ser **do**; executes a command with administrator privileges. |
| `passwd`         | Allows you to change your own password.                                     |

---

## 🛡️ Basic Firewall Security (UFW)

| Command                           | Description                                             |
| --------------------------------- | ------------------------------------------------------- |
| `sudo ufw status`                 | Checks if the firewall is active.                       |
| `sudo ufw default deny incoming`  | Blocks all incoming connections by default.             |
| `sudo ufw default allow outgoing` | Allows all outgoing connections from the server.        |
| `sudo ufw allow ssh`              | Allows connections for remote management (Port 22).     |
| `sudo ufw allow 32400`            | Allows connections to the Plex web interface.           |
| `sudo ufw allow 13378`            | Allows connections to the Audiobookshelf web interface. |
| `sudo ufw enable`                 | **Turns the firewall on.**                              |
| `sudo ufw reload`                 | Reloads the firewall rules after making a change.       |

---

## 🏴‍☠️ Installing Plex & Audiobookshelf

For both, you must first download the `.deb` installation file from their official websites.

- **Plex:** [plex.tv/media-server-downloads](https://www.plex.tv/media-server-downloads/)
- **Audiobookshelf:** [github.com/advplyr/audiobookshelf/releases](https://github.com/advplyr/audiobookshelf/releases)

| Command                           | Description                                                              |
| --------------------------------- | ------------------------------------------------------------------------ |
| `cd ~/Downloads`                  | Navigates to the folder where you downloaded the files.                  |
| `sudo dpkg -i <package_name>.deb` | Installs the application from the `.deb` file. Use the actual file name. |

---

## 🧰 Managing Services

| Command                            | Description                                                                 |
| ---------------------------------- | --------------------------------------------------------------------------- |
| `sudo systemctl status <service>`  | Checks if a service is running (e.g., `plexmediaserver`, `audiobookshelf`). |
| `sudo systemctl enable <service>`  | **Important!** Makes the service start automatically when the server boots. |
| `sudo systemctl start <service>`   | Manually starts a service.                                                  |
| `sudo systemctl stop <service>`    | Manually stops a service.                                                   |
| `sudo systemctl restart <service>` | Manually restarts a service.                                                |

---

## 🔒 Media Permissions

This is crucial for allowing Plex and Audiobookshelf to see your media files.

1. Create your media folders (e.g., `sudo mkdir -p /mnt/media/movies`).
2. Set permissions:

| Command                                    | Description                                                                             |
| ------------------------------------------ | --------------------------------------------------------------------------------------- |
| `sudo chown -R $USER:$USER /path/to/media` | Changes the owner of the media folder to you (`$USER` is a variable for your username). |
| `sudo chmod -R 775 /path/to/media`         | Sets Read/Write/Execute permissions for you and the group, and Read/Execute for others. |

---

## 🧹 Software Update & Cleanup

This is your main weekly task. It gets all the latest security patches and feature updates for your system and applications.

| Command                         | Description                                                                                     |
| ------------------------------- | ----------------------------------------------------------------------------------------------- |
| `sudo apt update`               | Refreshes the list of available packages from the system's software sources.                    |
| `sudo apt upgrade -y`           | Upgrades all installed system packages to their newest versions.                                |
| `flatpak update -y`             | Separately, this updates all of your installed Flatpak applications.                            |
| `sudo apt autoremove -y`        | **Recommended.** Removes packages that were installed as dependencies but are no longer needed. |
| `sudo apt clean`                | Clears the local cache of downloaded package files to free up disk space.                       |
| `flatpak uninstall --unused -y` | The Flatpak equivalent of `autoremove`. It removes any unused Flatpak runtimes.                 |

---

## 🐧 All-in-One Update Command

For a quick weekly tune-up, you can chain the most common commands together. This single line will update your system, update your flatpaks, and remove any leftover packages.

```bash
sudo apt update && sudo apt upgrade -y && flatpak update -y && sudo apt autoremove -y
```

---

## 🖥️ System Health

Here are three key commands for checking system health and clearing out old files.

#### ❌ Check for Failed Services

This is the most important health check. It will tell you if any background processes have crashed or failed to start. An empty output from this command is a good sign.

```bash
systemctl --failed
```

#### 📔 Clean Up System Logs

Over time, system log files can grow very large. This command will safely shrink the logs to a more manageable size (e.g., 100MB).

```bash
sudo journalctl --vacuum-size=100M
```

#### 🗑️ Empty the Trash

This command will forcefully empty your user's trash can. Be certain before running, as this cannot be undone.

```bash
rm -rf ~/.local/share/Trash/files/*
```
