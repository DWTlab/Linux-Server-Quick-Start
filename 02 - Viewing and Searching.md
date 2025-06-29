Once you can navigate, the next step is to see what's inside your files and find what you're looking for.

## 📝 Viewing File Contents

| Command | Description |
|---|---|
| `cat <file>` | Con**cat**enates and displays the entire content of a file at once. Best for short files. |
| `less <file>` | Displays the content of a file one page at a time. Use arrow keys to scroll and `q` to quit. Best for long files. |
| `head <file>` | Displays the first 10 lines of a file. Use `head -n 20` for the first 20 lines. |
| `tail <file>` | Displays the last 10 lines of a file. Use `tail -n 20` for the last 20 lines, or `tail -f` to watch for new lines in real-time. |

## ✏️ Simple File Editing

| Command | Description |
|---|---|
| `nano <file>` | Opens a simple, beginner-friendly terminal-based text editor. |
| `vim <file>` or `vi <file>` | Opens the powerful (but more complex) Vim text editor. |

## 🔎 Finding Files and Text

| Command | Description |
|---|---|
| `find <dir> -name "<pattern>"` | Searches for files within a directory (`<dir>`) that match a name (`<pattern>`). E.g., `find . -name "*.txt"`. |
| `grep "<text>" <file>` | Searches for a specific text pattern inside a file. It prints every line that contains the match. |
| `grep -r "<text>" <dir>` | **R**ecursively searches for a text pattern in all files within a directory. |
