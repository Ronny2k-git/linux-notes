# Ubuntu
 
### apt
 
| Command | |
|---|---|
| `sudo apt update && sudo apt upgrade` | **update — in that order** |
| `sudo apt install pkg` | install |
| `sudo apt install ./file_name.deb` | install a .deb |
| `sudo apt remove pkg` | uninstall |
| `sudo apt purge pkg` | uninstall + configs |
| `sudo apt autoremove` | clean unused deps |
| `apt search word` | search |
| `apt show pkg` | package details |
 
### Snap & Flatpak
 
| Command | |
|---|---|
| `sudo snap install pkg` | install snap |
| `snap list` | installed snaps |
| `flatpak install flathub app.id` | install flatpak |
| `flatpak list` | installed flatpaks |
 
### GNOME
 
| Command | |
|---|---|
| `gnome-control-center` | settings |
| `nautilus path/` | file manager |
| `gsettings set org.gnome.desktop.interface text-scaling-factor 1.15` | bigger text, any value |
| `Alt+F2` → `r` | restart GNOME (X11 only) |

---