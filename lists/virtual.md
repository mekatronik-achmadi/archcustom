# Virtual Packages

## Official

### install virtualization tools

virtualbox vde2 virtualbox-host-dkms virtualbox-guest-iso
qemu-desktop qemu-guest-agent qemu-emulators-full
qemu-user-static qemu-user-static-binfmt

### install docker

docker docker-compose

--------------------------------------------------------------------------------

## AUR

### install live USB writer

- https://aur.archlinux.org/packages/ventoy-bin/

### install virtualbox extension pack

- https://aur.archlinux.org/packages/virtualbox-ext-oracle/

--------------------------------------------------------------------------------

## Configurations

### configure virtualbox host

```sh
echo 'vboxdrv
vboxnetadp
vboxnetflt
vboxpci' | sudo tee /etc/modules-load.d/virtualbox.conf

sudo groupadd vboxusers
sudo gpasswd -a $USER vboxusers
```

```sh
echo 'mount shared folder on guest'
sudo mount -t vboxsf -o rw,uid=$USER folder_name /mnt
```

```sh
#if failed to start at first run
sudo rm -rvf ~/.config/VirtualBox/
```

### configure qemu additional driver

```sh
wget https://www.spice-space.org/download/binaries/spice-guest-tools/spice-guest-tools-latest.exe
```

### configure docker

```sh
sudo groupadd -f docker
sudo gpasswd -a $USER docker

# temporarily reload group
newgrp docker

export DOCKERPATH="/home/development/Virtuals/Dockers"

sudo mkdir -p /etc/docker/
sudo mkdir -p /var/lib/docker/

sudo mkdir -p $DOCKERPATH/
sudo chown -R root:root $DOCKERPATH/

echo "
{
    \"data-root\": \"$DOCKERPATH\"
}" | sudo tee /etc/docker/daemon.json

sudo systemctl stop docker.service
sudo rsync -aP /var/lib/docker/ $DOCKERPATH

sudo systemctl enable docker.service
sudo systemctl start docker.service
```

```sh
docker pull hello-world
docker run hello-world
```

```sh
git clone https://github.com/repo/dockerweb.git
cd dockerweb/

ls docker-compose.yml
docker-compose up --build

docker-compose up
docker-compose down
docker-compose up -d --build
```
