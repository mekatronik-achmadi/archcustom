# Arch-Linux Custom ISO

This is just example of custom Arch-Linux ISOs using Archiso dan Pacstrap tools.

**NOTE:** This works done by myself just as a hobby and I had no any relation to amazing people in Arch-Linux Dev Team.

## ISO Variants

The **archlinux-mate_012024-x86_64.iso** contain Mate Desktop with LightDM as Login Manager (disabled by default).

The desktop session can be started using command:

```sh
startx /usr/bin/mate-session
```

Optionally, you can enable LightDM using command:

```sh
systemctl enable lightdm
systemctl start lightdm
```

and login into desktop from there.

## Install From Live Session

You can try to follow this document:

https://github.com/mekatronik-achmadi/archcustom/tree/main/archiso/install_live/install_readme.md

## Project Repository

You are free to visit this project repository on Github:

https://github.com/mekatronik-achmadi/archcustom/tree/main/archiso

