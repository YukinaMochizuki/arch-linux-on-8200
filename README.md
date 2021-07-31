# arch-linux-on-8200
Arch Linux installation notes &amp; script for my HP Compaq 8200 Elite Microtower

Based on [arch-linux-on-7559](https://github.com/YukinaMochizuki/arch-linux-on-7559) except wifi and bluetooth support

### Tmp
after installing i3

fonts
```sh
# CJK and color-emoji
pacman -S noto-fonts-cjk noto-fonts-emoji 

# terminal fonts
pacman -S ttf-bitstream-vera ttf-dejavu

# polybar
pacman -S ttf-fantasque-sans-mono
```

aur package
```
polybar
notion-app-enhanced
# bing-wallpaper-git

# polybar
nerd-fonts-complete
```

application
```
sudo pacman -S lsb-release
wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash
```

other
```
ibus-setup
playerctl
```

### Issues
#### URxvt doesn't show unicode characters

```
# need to change LANG from C to en-US UTF-8
# ref: https://wiki.archlinux.org/title/Locale
sudo localectl set-locale LANG=en_US.UTF-8
```

/etc/locale.conf
```
LANG=en_US.UTF-8
LANGUAGE=en_US:en_GB:en
LC_TIME=en_US.UTF-8
LC_COLLATE=C
```

reboot

#### Copy and paste in URxvt

From [Clipboard in Arch Wiki](https://wiki.archlinux.org/title/clipboard):
> Synchronize PRIMARY, CLIPBOARD and cut buffer selections
```
sudo pacman -S autocutsel
```


### Todo
- credit
