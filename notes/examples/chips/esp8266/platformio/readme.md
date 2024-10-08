# PlatformIO

## Setup

```sh
mkdir -p $HOME/PyEnv;cd $HOME/PyEnv
virtualenv platformio --system-site-packages

source $HOME/PyEnv/platformio/bin/activate
mkdir -p $HOME/.platformio/
pip install platformio

UDEV=https://raw.githubusercontent.com/platformio/platformio-core/develop/platformio/assets/system/99-platformio-udev.rules
curl -fsSL $UDEV | sudo tee /etc/udev/rules.d/99-platformio-udev.rules
sudo udevadm control --reload-rules
sudo udevadm trigger

deactivate
cd -
```

## Home Webpage

```
source $HOME/PyEnv/platformio/bin/activate
pio home --no-open &
xdg-open http://localhost:8008/ &
```

## Project

### Setup

```sh
source $HOME/PyEnv/platformio/bin/activate
mkdir -p blink/;cd blink/

pio project init -b nodemcuv2
```

```sh
source $HOME/PyEnv/platformio/bin/activate
mkdir -p blink_nonos/;cd blink_nonos/

pio project init -b nodemcuv2 \
-O "framework=esp8266-nonos-sdk" \
-O "build_flags=-Isrc/include"
```

```sh
source $HOME/PyEnv/platformio/bin/activate
mkdir -p blink_rtos/;cd blink_rtos/

pio project init -b nodemcuv2 -O "framework=esp8266-rtos-sdk"
```

### Build

```sh
echo -e 'all:
\tpio run

compiledb:
\tpio run --target compiledb

upload:
\tpio run --target upload

clean:
\tpio run --target clean

monitor:
\tpio device monitor -p /dev/ttyUSB0 -b 115200
' | tee Makefile
```

```sh
source $HOME/PyEnv/platformio/bin/activate
export MAKEFLAGS=-j$(nproc)

make compiledb
make all

ls .pio/build/nodemcu/firmware.bin
make upload
```

### Serial

```sh
source $HOME/PyEnv/platformio/bin/activate
make monitor
```

