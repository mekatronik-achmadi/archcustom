# ArchISO Packages

## Official

### install basic system
bash-completion mkinitcpio
cloc less bear archinstall
squashfs-tools rsync dkms
pv cmus libxcrypt-compat
neofetch lsb-release dtc
nano dialog bc tmux tree
ripgrep bat fzf onefetch
curl wget openssh sshfs
pacman-contrib mlocate
virtualbox-guest-utils
git tig terminus-font
arch-install-scripts
highlight mc fdupes
fakechroot fakeroot
mkinitcpio-archiso
cdrtools syslinux
base base-devel

### install linux kernel

linux linux-firmware linux-headers

### install posix meta

posix posix-software-development
posix-xsi posix-c-development

### install vim editor

vim vim-nerdcommenter
vim-airline vim-tagbar
vim-surround vim-nerdtree
vim-tabular vim-gitgutter

### install xorg server

xorg xorg-apps xorg-drivers
xorg-xinit xorg-fonts
archlinux-xdg-menu
xsel xclip xterm
xorg-fonts-misc
default-cursors
x11-ssh-askpass
xorg-xmessage

### install login manager

lightdm lightdm-gtk-greeter
lightdm-gtk-greeter-settings

### install mate desktop

mate mate-extra
dconf dconf-editor

### install themes and icons

icon-naming-utils gtk-update-icon-cache
papirus-icon-theme arc-solid-gtk-theme
gtk-engines gtk-engine-murrine
gnome-themes-extra libcanberra
sound-theme-freedesktop

### install gtk 2/3 libraries

gtk3 wxgtk3 glade
gtk2 gtkmm gtkmm3
adwaita-cursors
python-wxpython
python-gobject

### install desktop basic

tk ttf-liberation onboard
ttf-liberation-mono-nerd
dbus xdg-desktop-portal
xdg-desktop-portal-gtk
ttf-dejavu ttf-droid
libappindicator-gtk3
redshift python-xdg
archlinux-wallpaper
xdg-user-dirs-gtk

### install desktop tools

geany geany-plugins
qt5-base qt6-base
qt5ct qt6ct scrot
xdotool shotwell
parcellite meld

### install networking system

networkmanager nm-connection-editor
network-manager-applet modemmanager
mobile-broadband-provider-info iftop
bind-tools netctl ppp wpa_supplicant
net-tools wavemon bmon nethogs gping
crda iw iwd wireless_tools tigervnc
bridge-utils ethtool usb_modeswitch
traceroute dhcp dnsmasq nss-mdns
openresolv dhclient dhcpcd mtr
tcpdump iperf3 fping inetutils
gnu-netcat nmap termshark

### install audio system

pulseaudio portaudio
jack2 pulseaudio-jack
alsa-utils alsa-firmware
alsa-ucm-conf sof-firmware
alsa-oss alsa-lib alsa-plugins
pulseaudio-equalizer pavucontrol
pulseaudio-alsa pulseaudio-bluetooth

### install gio filesystem

gvfs gvfs-gphoto2 gvfs-afc
gvfs-mtp gvfs-smb gvfs-nfs

### install compression tools

tar atool xz libarchive unrar unarj
lhasa rpmextract lxsplit unrar-free
bzip2 gzip lz4 p7zip zip unzip
lrzip lzip lzop zstd cpio

### install build tools

mercurial breezy cvs
cblas openblas lapack
gobject-introspection
subversion mk-configure
mate-common gnome-common
pkgconf gendesk help2man
meson ninja boost setconf
automake autogen autoconf
cmake extra-cmake-modules
dos2unix doxygen graphviz
tcsh chrpath swig valabind

### install java basic

jre8-openjdk jdk8-openjdk

### install python installer

python-pkgconfig python-wheel
python-build python-installer
python-pipenv python-virtualenv
python-pip python-distutils-extra
cython0 pybind11 python-setuptools

### install internet tools

vimb filezilla uget aria2
qbittorrent-nox qbittorrent

### install bluetooth support

blueman bluez
bluez-utils

### install multimedia

ffmpegthumbnailer
ffmpeg gst-libav
gst-plugins-good
gst-plugins-base
gst-plugins-ugly
vlc sox guvcview

### install libva driver

intel-media-driver
libva-intel-driver
libva-vdpau-driver
libva-mesa-driver
libva libva-utils
libvdpau-va-gl
vdpauinfo

### install cd-dvd tools

fuseiso mdf2iso
brasero bchunk
squashfuse
dvdauthor
vcdimager

### install printing support

cups cups-pdf
ghostscript gsfonts
system-config-printer
gutenprint foomatic-db-engine
foomatic-db foomatic-db-nonfree

### install image scanner

sane sane-airscan
ipp-usb simple-scan

### install system information

lm_sensors xsensors hddtemp
lsof nmon sysstat procps-ng
usbutils dmidecode hwdetect
hdparm sdparm smartmontools
htop ltrace strace mesa-demos
linux-tools arandr read-edid
hwloc hwinfo lshw mesa-utils
ccze inxi atop libstatgrab

### install disk tools

ntfs-3g exfat-utils
gparted dosfstools
gpart e2fsprogs
gptfdisk mtools
dfc fuse2 fuse3

### install boot system

grub os-prober
efibootmgr
edk2-shell
edk2-ovmf

--------------------------------------------------------------------------------

## Non-Official

### install additional base

- qt5gtk2: https://aur.archlinux.org/packages/qt5gtk2/
- qt6gtk2: https://aur.archlinux.org/packages/qt6gtk2/
- gtk3-nocsd-git: https://aur.archlinux.org/packages/gtk3-nocsd-git/
- mate-tweak: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/mate-tweak/
- mate-zenity: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/mate-zenity/

### install additional tools

- downgrade: https://aur.archlinux.org/packages/downgrade/
- fake-hwclock: https://aur.archlinux.org/packages/fake-hwclock/
- hardinfo-git: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/hardinfo/

### install vim additionals

- vim-plug-git: https://aur.archlinux.org/packages/vim-plug-git/
- vim-devicons-git: https://aur.archlinux.org/packages/vim-devicons-git/
- vim-pkgbuild-git: https://aur.archlinux.org/packages/vim-pkgbuild-git/

### install custom packages

- archmate-font: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/archmate-font/
- archmate-menu: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/archmate-menu/
- archmate-theme: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/archmate-theme/
- archmate-archiso: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/archmate-archiso/
- archmate-desktop: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/archmate-desktop/
- archmate-install: https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/custom/archmate-install/

### install optional theme packages

- https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/theme/archmate-win95/
- https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/theme/archmate-win10/

--------------------------------------------------------------------------------

## Live Session

### Bugfix Ventoy no disk mount

```sh
ln -svf /dev/dm-0 /dev/disk/by-label/ARCH_LINUX
exit
```

### Start Mate Live Session

```sh
startx /usr/bin/mate-session
```

--------------------------------------------------------------------------------

## After Install

### repository

```sh
# ArchLinux Repository Main Server URL
# Lower Mirror Score means better
# Look for 100% synced mirror from here:
#   https://archlinux.org/mirrors/status/#successful
export REPOURL='http://mirror.internode.on.net/pub/archlinux'
```

### preparation

```sh
sudo systemctl enable systemd-timesyncd
sudo systemctl start systemd-timesyncd
sudo systemctl enable fake-hwclock fake-hwclock-save
sudo systemctl start fake-hwclock fake-hwclock-save

sudo ln -svf /usr/share/zoneinfo/Asia/Jakarta /etc/localtime
sudo date -s "3 JAN 2024 20:46"

echo "LANG=en_US.UTF-8" | sudo tee /etc/locale.conf
echo "en_US ISO-8859-1" | sudo tee /etc/locale.gen
echo "en_US.UTF-8 UTF-8" | sudo tee -a /etc/locale.gen
sudo locale-gen

sudo mkdir -vp /var/lib/pacman/sync/
sudo mkdir -vp /var/cache/pacman/pkg/

export ISOVER='mate_012024'
export DIRPATH="/home/development/Packages/ArchMate-x86_64/$ISOVER"
sudo rsync -avh $DIRPATH/databases/ /var/lib/pacman/sync/
sudo rsync -avh $DIRPATH/packages/official/ /var/cache/pacman/pkg/

echo "install driver packages"
pluma lists/driver.md
```

--------------------------------------------------------------------------------

## Configurations

### Git User

```sh
git config --global user.name "mekatronik-achmadi"
git config --global user.email "mekatronik.achmadi@gmail.com"

git config --global init.defaultBranch main
echo 'export GITHUBTOKEN=$(cat ~/GithubToken.txt)' | tee -a ~/.bashrc
```

### Pacman-Key

```sh
# optionally only if had problems
# need internet connection and proper time setting

sudo pacman-key --init
sudo pacman-key --populate archlinux

# if initialitation keep failed
#sudo pacman-key --refresh-keys
```

### Booting

#### GRUB disable submenu

```sh
sudo sed -i "s@#GRUB_DISABLE_SUBMENU=y@GRUB_DISABLE_SUBMENU=y@g" /etc/default/grub
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

#### GRUB-BIOS from live ISO

```sh
sudo mount /dev/sda1 /mnt/
sudo arch-chroot /mnt/

grub-install --recheck --target=i386-pc /dev/sda
grub-mkconfig -o /boot/grub/grub.cfg

exit
sudo umount /mnt/
```

#### GRUB-UEFI from Live ISO

```sh
sudo mount /dev/sda2 /mnt/
sudo mount /dev/sda1 /mnt/boot/EFI
sudo arch-chroot /mnt/

# reinstall grub for default uefi
grub-install --recheck --target=x86_64-efi --efi-directory=/boot/EFI/ --bootloader-id=grub_uefi

# reinstall grub for removable uefi
grub-install --recheck --removable --target=x86_64-efi --efi-directory=/boot/EFI/ --bootloader-id=grub_uefi

grub-mkconfig -o /boot/grub/grub.cfg

exit
sudo umount /mnt/boot/EFI
sudo umount /mnt/
```

#### GRUB include Windows

```sh
echo 'Reconfig GRUB to include Windows'
sudo sed -i 's|#GRUB_DISABLE_OS_PROBER=false|GRUB_DISABLE_OS_PROBER=false|g' /etc/default/grub
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

#### GRUB SWAP partition

```sh
sudo mkswap /dev/sdxy
sudo swapon /dev/sdxy

SWAPUUID=$(sudo blkid -s UUID -o value /dev/sdxy)
echo "UUID=$SWAPUUID none swap defaults 0 0" | sudo tee -a /etc/fstab
```

### Bash Shell

#### modify pacstrap

```sh
sudo bash /usr/share/archmate-archiso/pacstrap_modify
```

#### autologin shell

```sh
sudo mkdir -p /etc/
echo '
                    -@
                   .##@
                  .####@
                  @#####@
                . *######@
               .##@o@#####@
              /############@
             /##############@
            @######@**%######@
           @######`     %#####o
          @######@       ######%
        -@#######h       ######@.`
       /#####h**``       `**%@####@
      @H@*`                    `*%#@
     *`                            `*
' | sudo tee /etc/motd

sudo mkdir -p /etc/systemd/system/getty@tty1.service.d/

echo "[Service]
TTYVTDisallocate=no
" | sudo tee /etc/systemd/system/getty@tty1.service.d/noclear.conf

echo -e "[Service]
ExecStart=
ExecStart=-/sbin/agetty --autologin $USER --noclear %I 38400 linux
" | sudo tee /etc/systemd/system/getty@tty1.service.d/autologin.conf
```

#### bashrc

```sh
echo '[[ $- != *i* ]] && return' |  tee ~/.bashrc
echo "
shopt -s checkwinsize
shopt -s histappend
alias ls='ls --color=auto'
alias grep='grep --color=auto'
alias sudo='sudo -E'
alias makepkg='makepkg --nocheck --skippgpcheck'
alias htop='htop -C'
alias mc='mc --nocolor'
alias bat='bat --theme=GitHub'
export MAKEFLAGS=-j$(nproc)
export HISTCONTROL=ignorespace:ignoredups:erasedups
export REPOURL='http://mirror.internode.on.net/pub/archlinux'
PS1='\[\033[01m\][\u@\h \W]\$ \[\033[00m\]'
" | tee -a ~/.bashrc
```

#### create new user with/without password

```sh
sudo useradd -m -g users -G wheel,storage,power,tty,video -s /bin/bash -c username username

# change password
sudo passwd username

# remove password password
sudo passwd -d username
```

#### networkmanager

```sh
sudo systemctl disable systemd-networkd
sudo systemctl disable systemd-resolved
sudo systemctl stop systemd-networkd
sudo systemctl stop systemd-resolved

sudo ln -svf /run/NetworkManager/resolv.conf /etc/resolv.conf
sudo systemctl enable NetworkManager
sudo systemctl start NetworkManager
```

#### bluetooth

```sh
sudo systemctl enable bluetooth
sudo systemctl start bluetooth
sudo bluetoothctl
```

#### vim

```sh
sudo mkdir -p /etc
echo '" /usr/share/vim/vimfiles/archlinux.vim' | sudo tee /etc/vimrc

echo 'runtime! archlinux.vim
autocmd BufWritePre * %s/\s\+$//e
filetype plugin on
filetype indent on
filetype plugin indent on
set expandtab ts=4 sw=4 ai
set conceallevel=0
set encoding=utf-8
set termguicolors
set ic is hls
set number
set wrap!
set mouse=a
let g:tagbar_width=20
let g:NERDTreeWinSize=20
syntax on' | sudo tee -a /etc/vimrc
```

#### profile

```sh
sudo mkdir -p /etc/profile.d/
echo '
export PATH=$PATH:~/.local/bin
export QT_QPA_PLATFORMTHEME=qt5ct
export VISUAL=vim
export EDITOR=vim
export PAGER=less
export VIEWER=less
export FREETYPE_PROPERTIES="truetype:interpreter-version=40"
export FT2_SUBPIXEL_HINTING=2
export GTK_CSD=0
export LD_PRELOAD=/usr/lib/libgtk3-nocsd.so.0:$LD_PRELOAD
export FZF_DEFAULT_COMMAND="rg --files"
export FZF_DEFAULT_OPTS="-m"
' | sudo tee /etc/profile.d/arch-profile.sh
```

### Xorg

#### gtk theme

```sh
rm -f $HOME/.gtkrc-2.0
rm -f $HOME/.config/gtk-3.0/settings.ini

sudo mkdir -pv /etc/gtk-2.0/
echo '
gtk-icon-theme-name = "Papirus-Light"
gtk-theme-name = "Arc-Lighter-solid"
gtk-font-name = "Liberation Sans 8"
' | sudo tee /etc/gtk-2.0/gtkrc

sudo mkdir -pv /etc/gtk-3.0/
echo '
[Settings]
gtk-icon-theme-name = Papirus-Light
gtk-theme-name = Arc-Lighter-solid
gtk-font-name = Liberation Sans 8
gtk-application-prefer-dark-theme = false
' | sudo tee /etc/gtk-3.0/settings.ini
```

#### xterm

```sh
echo "XTerm*faceName: LiterationMono Nerd Font Mono
XTerm*faceSize: 8
XTerm*background: white
XTerm*foreground: black
XTerm*selectToClipboard: true
XTerm*eightBitInput: false
XTerm*eightBitOutput: true
XTerm*scrollBar: true
XTerm*fastScroll: true
XTerm*rightScrollBar: true
UXTerm*faceName: LiterationMono Nerd Font Mono
UXTerm*faceSize: 8
UXTerm*background: white
UXTerm*foreground: black
UXTerm*selectToClipboard: true
UXTerm*eightBitInput: false
UXTerm*eightBitOutput: true
UXTerm*scrollBar: true
UXTerm*fastScroll: true
UXTerm*rightScrollBar: true
Xft.autohint: 0
Xft.antialias: 1
Xft.hinting: true
Xft.hintstyle: hintslight
Xft.dpi: 96
Xft.rgba: rgb
Xft.lcdfilter: lcddefault" | tee ~/.Xdefaults

xrdb .Xdefaults
```

### LightDM

#### default session

```sh
sudo rm -vf /etc/systemd/logind.conf.d/do-not-suspend.conf
echo '[login]
HandleLidSwitch=suspend
HandleLidSwitchDocked=suspend
' | sudo tee /etc/systemd/logind.conf.d/lid-suspend.conf

# check available session
ls /usr/share/xsessions/ | cut -d. -f1
```

#### desktop session without lighdm

```sh
startx /usr/bin/mate-session
```

#### desktop session using xinitrc

```sh
echo 'exec mate-session' > ~/.xinitrc

startx
```

--------------------------------------------------------------------------------

## Utilities

### Disk

```sh
# list attached disk
lsblk -f -o NAME,FSTYPE,LABEL,FSAVAIL

# mount a partition
udisksctl mount -b /dev/sdb2

# check partition
lsblk -f -o NAME,FSTYPE,LABEL,FSAVAIL

# unmount partition
udisksctl unmount -b /dev/sdb2

# power off disks
udisksctl power-off -b /dev/sdb2
```

### VNC

#### server

```sh
vncpasswd

x0vncserver -rfbauth ~/.vnc/passwd
#x0vncserver -geometry 1280x1024+0+0 -rfbauth ~/.vnc/passwd
```

#### viewer

```sh
# Menu/Fullscreen -> F8

vncviewer <ip_number>:0
```

### Session Info

```sh
echo "$TERM in $SHELL"
ps -o 'cmd=' -p $(ps -o 'ppid=' -p $$)

echo $XDG_CURRENT_DESKTOP
echo $XDG_SESSION_TYPE
```

### CPU Limit

#### Get information

Kernel modules

```sh
ls /usr/lib/modules/$(uname -r)/kernel/drivers/cpufreq/
```

CPU info

```sh
sudo cpupower info
sudo cpupower frequency-info
cat /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor
```

```sh
sudo turbostat
```

```sh
watch -n1 sensors
```

#### Governor Scaling (Intel)

Limit to minimum

```sh
sudo cpupower frequency-set -g powersave
sudo cpupower set -b 15
```

Save scaling using systemd

```sh
sudo sed -i "s@#governor='ondemand'@governor='powersave'@g" /etc/default/cpupower
sudo sed -i "s@#perf_bias=@perf_bias=15@g" /etc/default/cpupower
sudo systemctl enable cpupower
sudo reboot
```

-----------------------------------------------------------

## SourceForge Upload

### Directories

Project folder:
- https://sourceforge.net/projects/archlinux-custom-iso/files/

For uploading using web interface:
- https://sourceforge.net/projects/archlinux-custom-iso/upload/

### SSH Setup

create SSH using username and project-name:

```sh
ssh -t mekatronik,archlinux-custom-iso@shell.sourceforge.net create
```

then you can exit

```sh
exit
```

### Manage

login using previously created SSH

```sh
ssh -t mekatronik,archlinux-custom-iso@shell.sourceforge.net
```

check files:

```sh
cd /home/frs/project/archlinux-custom-iso/

tree
ls -l *.iso
md5sum *.iso
```

### Uploading SFTP

upload using sftp from a new bash shell:

```sh
sftp mekatronik@frs.sourceforge.net
```

```sh
sftp> cd /home/frs/project/archlinux-custom-iso/
sftp> put readme.md
sftp> exit
```

### Uploading FileZilla

**Note:** Try to create SSH first, then login and exit.
This way may speed up uploading.

Connect FileZilla using:
- host: sftp://frs.sourceforge.net
- username: mekatronik
- password: password
- port: 22

Remote site: /home/pfs/project/archlinux-custom-iso/
