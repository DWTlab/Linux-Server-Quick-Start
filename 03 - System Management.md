These commands help you monitor your system's resources, manage processes, and control user access.

## 💻 System & Resource Information

| Command | Description |
|---|---|
| `uname -a` | Prints detailed system information (Kernel version, OS, etc.). |
| `df -h` | Displays **d**isk **f**ree space usage in a **h**uman-readable format. |
| `du -sh <directory>` | Shows the total disk **u**sage of a specific directory in a **s**ummarized, **h**uman-readable format. |
| `free -h` | Shows the amount of free and used memory (RAM). |
| `top` or `htop` | Displays a real-time, dynamic list of running processes and resource usage. `htop` is more user-friendly (install with `sudo apt install htop`). |
| `ip a` | Shows your network adapter information, including your IP **a**ddress. |

## ⚙️ Process Management

| Command | Description |
|---|---|
| `ps aux` | Displays all currently running processes on the system. |
| `kill <PID>` | **Kill**s a process with the specified **P**rocess **ID**. |
| `killall <process_name>` | Kills all processes with the specified name (e.g., `killall firefox`). |

## 👤 User Management

| Command | Description |
|---|---|
| `whoami` | Displays the current user's username. |
| `sudo <command>` | **S**uper**u**ser **do**; executes a command with administrator privileges. |
| `passwd` | Allows you to change your own password. |
