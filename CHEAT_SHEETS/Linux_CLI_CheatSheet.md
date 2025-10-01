# Linux CLI Cheat Sheet — Task 2
Below is a compact table-style cheat sheet you can copy into your repo file. Use it as a quick reference for navigation, file management, permissions, and package management.

# Linux CLI Cheat Sheet — Task 2


Below is a compact table-style cheat sheet you can copy into your repo file. Use it as a quick reference for navigation, file management, permissions, and package management.


| Group | Command | Purpose | Example |
|---|---|---|---|
| Navigation | `pwd` | Print working directory (tells you where you are). | `pwd` |
| Navigation | `ls -la` | List files (including hidden files) and detailed attributes. | `ls -la /etc` |
| Navigation | `cd /path/` | Change directory. | `cd /var/log` |
| Navigation | `cd ..` | Move up one directory level. | `cd ..` |
| File Management | `touch file.txt` | Create an empty file. | `touch notes.txt` |
| File Management | `mkdir dir_name` | Create a new directory. | `mkdir lab_files` |
| File Management | `cp src dest` | Copy files or directories. | `cp notes.txt /tmp/` |
| File Management | `rm -r name` | Remove a file or recursively remove a directory. | `rm -r lab_files` |
| Permissions | `ls -l` | View permissions, owner, and group. | `ls -l` |
| Permissions | `chmod XXX file` | Change permissions using octal notation (e.g., 755). | `chmod 700 secret.sh` |
| Permissions | `chown user:group file` | Change the owner and/or group of a file. | `sudo chown root secret.sh` |
| System/Packages | `sudo apt update` | Refresh the list of available package updates. | `sudo apt update` |
| System/Packages | `sudo apt full-upgrade -y` | Upgrade all installed packages to their latest versions. | `sudo apt full-upgrade -y` |
| System/Packages | `sudo apt install pkgname` | Install a new package. | `sudo apt install net-tools` |
| System/Packages | `man command` | Display the manual page for any command. | `man nmap` |
