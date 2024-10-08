# Pacman Guidance

## Pacman Basic

### basic commands

```sh
nano /var/log/pacman.log
nano /etc/pacman.conf
nano /etc/wgetrc
nano /etc/pacman.d/mirrorlist
```

```sh
ls /var/lib/pacman/sync/*.db
ls /var/lib/pacman/sync/*.files
ls /var/cache/pacman/pkg/*.pkg.tar.xz
```

```sh
pacman -Sy
pacman -S <package_name | package_group_name>
pacman -Sy <package_name | package_group_name>
pacman -S --force <package_name | package_group_name>
pacman -S <package_name | package_group_name> --ignore <package_name>
pacman -Sy
pacman -Su
pacman -Sgg
pacman -Sg <package_group_name>
pacman -Sw <package_name>
pacman -Sup
pacman -Sp <package_name>
pacman -Sc
pacman -Scc
pacman -Sl
pacman -Sl <repository>
pacman -S <repository>/<package_name>
pacman -Ssq <part_package_name>
pacman -Sii <package_name>

pacman -Fy
pacman -Fs <part_filename>

pacman -Qq | grep <package_name>
pacman -Qii <package_name>
pacman -Qlq <package_name>
pacman -Qo <full_filename>

pacman -U packagefile.pkg.tar.gz
pacman -U --force packagefile.pkg.tar.gz
pacman -U --asdeps packagefile.pkg.tar.gz
pacman -U --asexplicit packagefile.pkg.tar.gz

pacman -Rs <package_name | package_group_name>
pacman -Rns <package_name | package_group_name>
pacman -Rns $(pacman -Qdtq)
pacman -Rns $(pacman -Qdttq)

yes | pacman -S <package_name>
yes | pacman -U packagefile.pkg.tar.gz
yes | pacman -Rns <package_name>

pactree <package_name>
paclist repository
```

```sh
pacstrap <mount-point> <package_name>
pacstrap <mount-point> <package_group_name>
pacstrap -i <mount-point> <package_name>
pacstrap -c <mount-point> <package_name>
pacstrap -d <directory> <package_name>
pacstrap -G <mount-point> <package_name>
pacstrap -M <mount-point> <package_name>
```

```sh
pacman-key --init
pacman-key --populate archlinux
pacman-key --populate archlinux manjaro
pacman-key --refresh-keys
```

```sh
downgrade <package_name> -- -w
```

## Servers

### Mirrors

- https://www.archlinux.org/mirrorlist/
- https://www.archlinux.org/mirrorlist/all/
- https://wiki.archlinux.org/index.php/Mirrors
- http://archlinuxarm.org/about/mirrors

### AUR Repository

- https://wiki.archlinux.org/index.php/Arch_User_Repository
- https://aur.archlinux.org/

### Archive Repository

- https://wiki.archlinux.org/index.php/Arch_Linux_Archive
- https://wiki.archlinux.org/index.php/downgrading_packages
- https://archive.archlinux.org/packages/
- https://archive.org/details/archlinuxarchive

## Pacman Settings

### Online Repository

```sh
# /etc/pacman.conf
# $repo = core, extra, or multilib
# $arch = x86_64, armv7h, or other architecture
# http://mirror.internode.on.net/pub/archlinux/iso/
```

```sh
echo -e "
[core]
Server = http://mirror.internode.on.net/pub/archlinux/\$repo/os/\$arch

[extra]
Server = http://mirror.internode.on.net/pub/archlinux/\$repo/os/\$arch

[multilib]
Server = http://mirror.internode.on.net/pub/archlinux/\$repo/os/\$arch
"
```

### Signature Check Level

```sh
# SigLevel = Never
# SigLevel = Optional TrustAll
# SigLevel = Required Database Optional
# LocalFileSigLevel = Optional
# RemoteFileSigLevel = Required
```

```sh
sed -i 's/SigLevel.*/SigLevel = Never/g' /etc/pacman.conf
```

### Package Databases URL

http://mirror.internode.on.net/pub/archlinux/core/os/x86_64/core.db
http://mirror.internode.on.net/pub/archlinux/extra/os/x86_64/extra.db
http://mirror.internode.on.net/pub/archlinux/multilib/os/x86_64/multilib.db

### Pacman Wget

```sh
# XferCommand = /usr/bin/wget --passive-ftp -c -O %o %u
```

```sh
pacman -S wget
sed -i "s@#XferCommand = /usr/bin/wget@XferCommand = /usr/bin/wget@g" /etc/pacman.conf
```

### Create Custom Repository

```sh
# $repo -> custom-repo-name
# $arch -> x86_64, armv7h, or other architecture
# Server -> URL or file path
```

```sh
echo -e "
[custom]
SigLevel = Never
Server = file:///path
#Server = https://URL
" >> /etc/pacman.conf
```

### Repository File Index

```sh
repo-add /path/custom.db.tar.gz /path/*.pkg.tar.xz
cp /path/custom.db.tar.gz /path/custom.db
```

---------------------------------------------------------

## Makepkg Basic

### Skip Some Checks

```sh
alias makepkg='makepkg --nocheck --skippgpcheck'
```

### Prepare Build Script

```sh
tar -xzf pkgname.tar.gz
cd pkgname/
cat PKGBUILD
```

### Create and Apply Patch

```sh
diff -Naur filename.old filename.new > filename.patch
diff -Naur directory_old directory_new > filename.patch
patch filename.old filename.patch
patch -p1 < filename.patch
```

### Compile and Build a pkg.tar.gz Package

```sh
makepkg -do
makepkg -sr
makepkg -ser
makepkg -sir
makepkg -seir
makepkg -Re
makepkg -Rei
makepkg --force
makepkg --holdver
makepkg --repackage
makepkg --skippgpcheck
makepkg --skipchecksums
makepkg -sir --asdeps
makepkg -seir --asdeps
```

### Archiving and Building Source Directory

```sh
makepkg -do
export ZIPNAME=$(cat PKGBUILD | grep -m 1 -w "pkgname" | cut -d= -f2)
zip -r $ZIPNAME-src.zip ./src/
makepkg -seir
```

### General Content of PKGBUILD

```sh
pkgname=qtserialterminal
#_pkgname=qtserialterminal
#_gitname=qtserialterminal
```

```sh
pkgver=0.1
pkgrel=1
pkgdesc="program stm32 chip via bootloader"
url= "http://optional.source.url/"
license=('WTFPL')
```

```sh
arch=('x86_64')
#arch=('any')
#arch=('armv7h')
#arch=('armv7h' 'x86_64')
```

```sh
depends=('qt5-base' 'qt5-serialport')
#depends=()
makedepends=('qt5-base' 'qt5-serialport')
#makedepends=()
```

```sh
options=('makeflags')
#options=('staticlibs')
#options=('libtool')
#options=('!strip')
#options=('!emptydirs')
```

```sh
install=pkg.install
```

```sh
provides=("$pkgname")
#provides=("$pkgname=$pkgver")
conflicts=("$pkgname" "$pkgname-git")
```

```sh
source=('${pkgname}.zip')
#source=('$pkgname.desktop $pkgname.sh $pkgname.xml')
#source=('https://github.com/git-cola/git-cola/archive/v$pkgver.zip')
#source=('http://ftp.gnome.org/pub/GNOME/sources/${_pkgname}/${pkgver}/${_pkgname}-${pkgver}.tar.xz')
#source=("$pkgname::git+https://github.com/mekatronik-achmadi/achmadi-installer")
```

```sh
prepare() {
    cd "${pkgname}-master"
    #cd "$srcdir"
    #cd "${_gitname}"
    #cd "${pkgname}-${pkgver}"
    #cd "${_pkgname}-${pkgver}"
    #cd "$srcdir/${pkgname}-$pkgver"
    
    patch ${pkgname}/file file.patch
    #patch -p1 < ../../patch-file.patch
    #patch < patch-file.patch
    #patch -uN -i patch-file.patch
    #patch -uN -pX -i patch-file.patch
}
```

```sh
build() {
    cd "${pkgname}-master"
    #cd "$srcdir"
    #cd "${_gitname}"
    #cd "${pkgname}-${pkgver}"
    #cd "${_pkgname}-${pkgver}"
    #cd "$srcdir/${pkgname}-$pkgver"
    qmake
    #./autogen.sh
    #./configure
    make all
    #make all doc html
}
```

```sh
package() {
    cd "${pkgname}-master"
    #cd "$srcdir"
    #cd "${_gitname}"
    #cd "${pkgname}-${pkgver}"
    #cd "${_pkgname}-${pkgver}"
    #cd "$srcdir/${pkgname}-$pkgver"
    make INSTALL_ROOT=${pkgdir} install
    #make install
    #make prefix=/usr DESTDIR="$pkgdir" install
    #make prefix=/usr DESTDIR="$pkgdir" install{,-doc,-html}
    install -d $pkgdir/path/
    mv -vf file $pkgdir/path/
    #mv -vf ../file $pkgdir/path/
}
```

```sh
pkgver() {
    cd "$pkgname"
    git describe --long --tags | sed 's/-/.r/;s/-/./'
}
```

```sh
sha256sum source_package.zip
sha256sum source_package.tar.gz
md5sum source_package.zip
md5sum source_package.tar.gz
```

### Example of General Content PKGBUILD

```sh
# overwrite specific PKGBUILD fields
# multiple version of "pkgname" grouped in one "pkgbase"
# check ./SRCINFO
```

```sh
pkgbase = eagle
pkgname = eagle
pkgdesc = A powerful suite for schematic capture and printed circuit board design (aka eaglecad)
pkgver = 7.3.0
pkgrel = 2
url = http://www.cadsoft.de/
install = eagle.install
arch = ('i686' 'x86_64')
license = custom
depends = ('desktop-file-utils' 'fontconfig' 'libcups' 'libxcursor' 'libxi' 'libxrandr' 'shared-mime-info')
options = (!emptydirs)
sources = ('eagle.desktop' 'eagle.sh' 'eagle.xml')
sha256sums = ('86307352ad81aa0dee0dfe58ab6799b06200d489a8f6cef77845e772202d20a6'
            '0e38128c87ad72b692e16d5be75b7b21182e4e89caeadfc2bb285588c060176c'
            '293ef717030e171903ba555a5c698e581f056d2a33884868018ab2af96a94a06')
source_i686 = ("eagle-7.3.0.run::ftp://ftp.cadsoft.de/eagle/program/7.3/eagle-lin32-7.3.0.run")
sha256sums_i686 = ('93428e5cd6938f6a5efccce5f9ca1d2223ba2118868efd810a3fc84caf871232')
source_x86_64 = ("eagle-7.3.0.run::ftp://ftp.cadsoft.de/eagle/program/7.3/eagle-lin64-7.3.0.run")
sha256sums_x86_64 = ('2e7d98dc3c03bbd6ff3c10b54001722f57e25f8db8776851beac6fe755c8a7a5')
```

### Example of General Content pkg.install

```sh
update_icons() {
    gtk-update-icon-cache -q -t -f usr/share/icons/hicolor
    update-desktop-database -q
}

update_settings() {
    update-desktop-database /usr/share/applications
    update-mime-database /usr/share/mime
    glib-compile-schemas /usr/share/glib-2.0/schemas/
}

post_install() {
    update_icons
    update_settings
}

post_upgrade() {
    update_icons
    update_settings
}
```

### Vim Editing PKGBUILD

```sh
echo "Vim command"
echo ":set ft=PKGBUILD"
```

## Makefile

### Qmake Variable for "make install"

```sh
# project.pro
```

```sh
target.path = /usr/local/bin
INSTALLS += target
```

### Makefile Basic Command for "make install"

```sh
install -d /usr/local/bin/
install -m 755 -p qtserialterminal /usr/local/bin/qtserialterminal
install -d /usr/local/share/qtserialterminal
cp -rvf resources /usr/local/share/qtserialterminal
```

### Makefile for "make install"

```sh
PREFIX = /usr/local
INSTALL = install
COPY    = cp -rvf
install:
    $(INSTALL) -d $(DESTDIR)$(PREFIX)/bin
    $(INSTALL) -m 755 stm32_microxplorer $(DESTDIR)$(PREFIX)/bin
    $(INSTALL) -d $(DESTDIR)$(PREFIX)/share/stm32_microxplorer
    $(COPY) db $(DESTDIR)$(PREFIX)/share/stm32_microxplorer
```
