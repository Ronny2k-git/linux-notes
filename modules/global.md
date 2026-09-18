[← back to index](../README.md)

# Global

Works on every distro.

### Moving around

| Command | What it does |
|---|---|
| `pwd` | where am I |
| `ls or ls -la` | list all or list all with details |
| `cd folder name` | enter folder |
| `cd ..` | up one level |
| `cd` | go home |

### Files

| Command | What it does |
|---|---|
| `mkdir -p folder name` | create folders, nested |
| `touch file` | create empty file |
| `cp file name destination/` | copy file |
| `cp -r folder destination/` | copy folder |
| `mv old new` | move **or** rename |
| `rm file` | delete file |
| `rm -r folder` | delete folder — no undo |

### Reading

| Command | What it does |
|---|---|
| `cat file name` | print whole file |
| `less file name` | scroll it — `q` quits, `/` searches |
| `tail -f file.log` | follow a log live |
| `nano file name` | edit — `Ctrl+O` save, `Ctrl+X` exit |

### Searching

| Command | What it does |
|---|---|
| `grep -rn "word" .` | search inside files |
| `find . -name "*.txt"` | find files by name |

### Redirecting

| Command | What it does |
|---|---|
| `cmd > file name` | write to file, overwrite |
| `cmd \| grep word` | filter output |

### Permissions

| Command | What it does |
|---|---|
| `chmod +x script.sh` | make executable |
| `sudo cmd` | run as admin |

### Processes

| Command | What it does |
|---|---|
| `btop or htop` | what's running (resource monitor) |
| `ps aux \| grep name` | find a process |
| `pgrep -a name` | find a process (command line) |
| `pkill process name` | kill a process by name |

### System info

| Command | What it does |
|---|---|
| `df -h` | disk space |
| `du -sh folder/` | size of a folder |
| `du -sh * \| sort -h` | what's eating space here |
| `ncdu` | browse disk usage |
| `free -h` | memory |
| `uname -r` | kernel version |
| `lsblk -f` | drives, partitions, filesystems |
| `lscpu` | CPU |
| `lsusb` | USB devices |
| `lspci -k` | PCI devices + loaded driver |

### Network

| Command | What it does |
|---|---|
| `ip a` | my IP addresses |
| `ping -c 4 google.com` | test connection (4 packages) |
| `wget url` | download a file |
| `nmcli device` | network status |
| `ss -tulpn` | what's listening on which port |

### USB drives

| Command | What it does |
|---|---|
| `udisksctl mount -b /dev/sda1` | mount it |
| `udisksctl unmount -b /dev/sda1` | unmount — always before unplugging |

### Archives & backup

| Command | What it does |
|---|---|
| `tar -czvf out.tar.gz folder/` | compress |
| `tar -xzvf file.tar.gz` | extract |
| `unzip file.zip` | unzip |
| `rsync -ah --progress src/ dst/` | copy with progress bar |

### Power

| Command | What it does |
|---|---|
| `systemctl poweroff` | shut down |
| `systemctl reboot` | restart |
| `systemctl suspend` | sleep |
| `loginctl terminate-user $USER` | log out |

### Terminal survival

| Keybind | What it does |
|---|---|
| `Tab` | autocomplete|
| `Ctrl+R` | search command history |
| `Ctrl+C` | cancel running command |
| `Ctrl+L` | clear screen |
| `!!` / `sudo !!` | repeat last command / with sudo |
| `man cmd` / `cmd --help` | documentation |

---