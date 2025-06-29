A step-by-step walkthrough for setting up a new Linux Mint server, specifically for hosting Plex and Audiobookshelf.

### Basic Firewall Security (UFW)
| Command | Description |
|---|---|
| `sudo ufw status` | Checks if the firewall is active. |
| `sudo ufw default deny incoming` | Blocks all incoming connections by default. |
| `sudo ufw default allow outgoing` | Allows all outgoing connections from the server. |
| `sudo ufw allow ssh` | Allows connections for remote management (Port 22). |
| `sudo ufw allow 32400` | Allows connections to the Plex web interface. |
| `sudo ufw allow 13378` | Allows connections to the Audiobookshelf web interface. |
| `sudo ufw enable` | **Turns the firewall on.** |
| `sudo ufw reload`| Reloads the firewall rules after making a change. |

### Installing Plex & Audiobookshelf
For both, you must first download the `.deb` installation file from their official websites.
- **Plex:** [plex.tv/media-server-downloads](https://www.plex.tv/media-server-downloads/)
- **Audiobookshelf:** [github.com/advplyr/audiobookshelf/releases](https://github.com/advplyr/audiobookshelf/releases)

| Command | Description |
|---|---|
| `cd ~/Downloads` | Navigates to the folder where you downloaded the files. |
| `sudo dpkg -i <package_name>.deb` | Installs the application from the `.deb` file. Use the actual file name. |

### Managing Services
| Command | Description |
|---|---|
| `sudo systemctl status <service>` | Checks if a service is running (e.g., `plexmediaserver`, `audiobookshelf`). |
| `sudo systemctl enable <service>` | **Important!** Makes the service start automatically when the server boots. |
| `sudo systemctl start <service>` | Manually starts a service. |
| `sudo systemctl stop <service>` | Manually stops a service. |
| `sudo systemctl restart <service>` | Manually restarts a service. |

### Media Permissions
This is crucial for allowing Plex and Audiobookshelf to see your media files.
1. Create your media folders (e.g., `sudo mkdir -p /mnt/media/movies`).
2. Set permissions:

| Command | Description |
|---|---|
| `sudo chown -R $USER:$USER /path/to/media` | Changes the owner of the media folder to you (`$USER` is a variable for your username). |
| `sudo chmod -R 775 /path/to/media` | Sets Read/Write/Execute permissions for you and the group, and Read/Execute for others. |
