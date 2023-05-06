# chadwm (Initial look)

<img src="https://github.com/siduck/chadwm/blob/screenshots/screenshots/initial_look.png">
<img src="https://github.com/siduck/chadwm/blob/screenshots/screenshots/col_layout.png">
<img src="https://github.com/siduck/chadwm/blob/screenshots/screenshots/occ_act_tags.png">
<img src="https://github.com/siduck/chadwm/blob/screenshots/screenshots/chadwm.png">
<img src='https://i.redd.it/t1pvmqlq3oc81.png'>
<img src="https://github.com/siduck/chadwm/blob/screenshots/screenshots/gruvchad.png">


# Requirements

- dash (shell)
- imlib2 
- xsetroot package (status2d uses this to add colors on dwmbar)
- JetbrainsMono Nerd Font or any nerd font but dont forget to set it in config.def.h
- Make sure to setup your terminal's theme accordingly do doc-dwm's theme such as nord, onedark etc...

## Other requirements
- picom (dccsillag fork)
- feh
- acpi
- rofi

# Install

```
git clone https://github.com/docfaizal/doc-dwm --depth 1  ~/.config/doc-dwm
cd ~/.config/doc-dwm 
cp -r Xresources ~/
cp -r rofi ~/.config
cd dwm
sudo make clean install
```

# Run chadwm

## With startx

```shell
startx ~/.config/doc-dwm/scripts/dwm-autostart

```

## With sx

```shell
sx sh ~/.config/doc-dwm/scripts/dwm-autostart```

(Make an alias for this :v)

```shell
alias d-dwm='startx ~/.config/doc-dwm/scripts/dwm-autostart'
```

## With Display Manager

- Create a desktop entry (make sure to change `user` with your user):

```shell
sudo touch /usr/share/xsessions/doc-dwm.desktop  
```

```
[Desktop Entry]
Name=doc-dwm
Comment=dwm made beautiful 
Exec=$HOME/.config/doc-dwm/scripts/dwm-autostart 
Type=Application 
```

- [wallpaper](https://github.com/siduck/chadwm/blob/screenshots/screenshots/chad.png)

# Recompile

- You need to recompile dwm after every change you make to its source code.

```
cd ~/.config/chadwm/chadwm
rm config.h
sudo make clean install
```

# Change themes

- Bar  : in bar.sh (line 9) and config.def.h (line 35)
- rofi : in config.rasi (line 15)



# Patches

- barpadding 
- bottomstack
- cfacts
- dragmfact 
- dragcfact (took from [bakkeby's build](https://github.com/bakkeby/dwm-flexipatch))
- fibonacii
- gaplessgrid
- horizgrid
- movestack 
- vanity gaps
- colorful tags
- statuspadding 
- status2d
- underline tags
- notitle
- winicon
- [preserveonrestart](https://github.com/PhyTech-R0/dwm-phyOS/blob/master/patches/dwm-6.3-patches/dwm-preserveonrestart-6.3.diff). This patch doesnt let all windows mix up into tag 1 after restarting dwm.
- shiftview
