## Update pacman package manager:
* sudo pacman -Syyu
## Install & Update aur package manager:
* sudo pacman -S yay
* yay -Syyu

## Install & Active snapcraft package manager:
* sudo pacman -S snapd
* sudo systemctl enable --now snapd.socket
* sudo ln -s /var/lib/snapd/snap/snap
