# Arch
 
### pacman
 
| Command | What it does |
|---|---|
| `sudo pacman -Syu` | **update everything — do this first** |
| `sudo pacman -S pkg` | install |
| `sudo pacman -S --needed pkg1 pkg2` | install, skip what's there |
| `sudo pacman -Rns pkg` | remove + unused deps |
| `pacman -Ss word` | search available |
| `pacman -Qs word` | search installed |
| `pacman -Qo /path/file` | which package owns this file |
| `pacman -Qqe` | what I installed on purpose |
| `paccache -r` | clean package cache |
 
### yay (AUR)
 
| Command | What it does |
|---|---|
| `yay -S pkg` | install from AUR |
| `yay -Syu` | update everything incl. AUR |
 
### Backup your setup
 
```bash
pacman -Qqen > pkglist-pacman.txt
pacman -Qqem > pkglist-aur.txt
systemctl list-unit-files --state=enabled > services.txt
 
# restore
sudo pacman -S --needed - < pkglist-pacman.txt
yay -S --needed - < pkglist-aur.txt
```
 
### Hyprland
 
Config: `~/.config/hypr/hyprland.lua` — **Lua since 0.55**, old tutorials use `.conf` syntax.
 
| Command | What it does |
|---|---|
| `hyprctl monitors` | resolution, scale, available modes |
| `hyprctl binds` | all keybinds — find collisions here |
| `hyprctl clients` | open windows + their class |
| `hyprctl reload` | reload config |
| `hyprctl dispatch exit` | log out |
| `tail -50 $XDG_RUNTIME_DIR/hypr/*/hyprland.log` | why it broke |
| `hyprctl activeworkspace` | Show current workspace|
 
```lua
hl.bind("SUPER + F", hl.dsp.window.fullscreen())
hl.env("VAR", "value")
hl.on("hyprland.start", function() hl.exec_cmd("waybar") end)
hl.config({ decoration = { blur = { enabled = false } } })
hl.monitor({ output = "HDMI-A-1", mode = "3440x1440@60", position = "auto", scale = 1.50 })
```
 
Emergency binds if the config errors: `SUPER+Q` terminal · `SUPER+R` launcher · `SUPER+M` exit.
 
Screenshot: `grim -g "$(slurp)" ~/Pictures/$(date +%Y%m%d-%H%M%S).png`
 
---