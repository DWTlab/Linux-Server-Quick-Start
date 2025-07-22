These are the fundamental commands for operating within the Linux shell. Mastering these is the first step to becoming comfortable with the command line.

## 🐚 Basic Shell Shortcuts

| Command    | Description                                        |
| ---------- | -------------------------------------------------- |
| `clear`    | Clears all text from the terminal screen.          |
| `history`  | Displays a list of previously used commands.       |
| `!!`       | Executes the very last command you ran.            |
| `exit`     | Closes the current terminal session.               |
| `Ctrl + C` | Force-stops the currently running command.         |
| `Ctrl + Z` | Pauses the current command (can be resumed later). |

## 📁 Navigating the Filesystem

| Command          | Description                                                                       |
| ---------------- | --------------------------------------------------------------------------------- |
| `pwd`            | **P**rint **W**orking **D**irectory (shows your exact current location).          |
| `ls`             | **L**i**s**ts the files and directories in your current location.                 |
| `ls -la`         | Lists all contents (including hidden `.files`) in a long, detailed format.        |
| `cd <directory>` | **C**hange **D**irectory to the specified path (e.g., `cd /home/user/Documents`). |
| `cd ..`          | Moves you up one directory level.                                                 |
| `cd ~` or `cd`   | Navigates directly to your home directory from anywhere.                          |

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
