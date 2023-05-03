## Update pacman package manager:
* sudo pacman -Syyu
## Install & Update aur package manager:
* sudo pacman -S yay
* yay -Syyu

## Install & Active snapcraft package manager:
* sudo pacman -S snapd
* sudo systemctl enable --now snapd.socket
* sudo ln -s /var/lib/snapd/snap/snap

## Install & Update pamac package manager:
* sudo pacman -S pamac
* sudo pamac update

## Install & Update flatpak package manager:
* sudo pacman -S flatpak
* sudo flatpak update

## Set and fix the mirrors to Germany:
* sudo pacman-mirrors -c Germany
* sudo pacman-mirrors -f

## Install Required Tools Linux:
* sudo pacman -S linux515-headers base-devel copyq firewalld gparted latte-dock alacarte libreoffice-fresh kvantum wine clamav clamtk cmake
* yay -S optimus-manager stacer powerline-fonts-git ulauncher peazip-gtk2-bin httpbin

## Install Required Applications:
* sudo pacman -S ark cheese lshw obs-studio okular simplescreenrecorder steam p7zip htop timeshift
* sudo flatpak install anydesk

## Install Browser:
* sudo pacman -S firefox links torbrowser-launcher
* yay -S google-chrome
* sudo pamac install brave-browser

## Install Editor:
* sudo pacman -S kate micro nano vim deepin-editor notepadqq
* yay -S xournalpp

## Install Multimedia:
* sudo pacman -S clementine elisa vlc
* sudo snap install spotify
* yay -S jamesdsp
* sudo snap install dragon

## Install Social Media:
* sudo pacman -S discord telegram-desktop
* sudo snap install whatsapp-for-linux
* sudo snap install skype

## Customize Konsole:
* sudo pacman -S zsh
* sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
* git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
* ZSH_THEME="powerlevel10k/powerlevel10k" >> ~/.zshrc
* sudo pacman -S zsh screenfetch neofetch
* yay -S translate-shell nerdfetch pantheon-terminal figlet lolcat
* sudo su
* echo screenfetch >> ~/.zshrc

## Graphic tools:
* sudo pacman -S gimp krita rnote shotwell gwenview inkscape appimagelauncher snapper flameshot
* yay -S lorien-bin

## Programming tools:
* sudo pacman -S ipython nodejs npm git pycharm-community-edition
* yay -S gitflow-avh
* sudo snap install gitkraken --classic
* sudo snap install postman
* sudo snap install insomnia
* sudo snap install code --classic
* sudo snap install atom --classic

## Network tools:
* Wireshark: install and enable capture packets:
* sudo pacman -S wireshark-qt
* sudo chmod +x /usr/bin/dumpcap
* other tools:
* sudo pacman -S remmina net-tools nmap
* yay -S wrk
* pamac install putty

## Enable TRIM for SSD
* sudo systemctl enable fstrim.timer
* sudo systemctl start fstrim.timer

## Install Docker:
* sudo pacman -S docker docker-compose
* sudo systemctl start docker
* sudo systemctl enable docker

## Uncomplicated FireWall: install, enable, add to startup
* sudo pamac install ufw
* sudo pamac install gufw
* sudo ufw enable
* sudo systemctl enable ufw

# Databases:
## postgresql
* sudo pacman -S postgresql
* sudo -iu postgres
* initdb --locale $LANG -E UTF8 -D '/var/lib/postgres/data/'
* exit
* sudo systemctl start postgresql.service
* sudo systemctl enable --now postgresql.service

## pgadmin
* sudo mkdir /var/lib/pgadmin
* sudo mkdir /var/log/pgadmin
* sudo chown $USER /var/lib/pgadmin
* sudo chown $USER /var/log/pgadmin
* python3 -m venv pgadmin4
* source pgadmin4/bin/activate
* pip install pgadmin4
* cd pgadmin4
* pgadmin4

## mongodb
* yay -Sq mongodb-bin mongodb-compass
* sudo systemctl start mongodb.service
* sudo systemctl enable mongodb.service

## redis
* sudo pacman -Sq redis
* sudo systemctl start redis
* sudo systemctl enable redis

## sqlite
* sudo pacman -Sq sqlite
