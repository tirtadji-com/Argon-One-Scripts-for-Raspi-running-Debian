# Argon One installation script for Debian 10

> The Argon One requires a one-line script to be run on the Raspberry Pi using the case for the power button and fan to function correctly. 

## Description

The Argon One case is a solid Aluminum alloy case for the Raspberry Pi 4 that offers passive and active cooling (see https://www.argon40.com/argon-one-raspberry-pi-4-case.html). 

This script has been adapted from the original [installation script](https://download.argon40.com/argon1.sh) which is
designed to work with Raspbian (Raspberry OS); the modified scripted has been developed for use with [Debian 10.7](https://raspi.debian.net/).

The modified script contains three changes to the original script:

1. Fork from [Meuter Github](https://github.com/meuter/argon-one-case-ubuntu-20.04).
2. Package dependencies have been adapted for Debian 10.7.

## Install

Feel free to review the source code of the modified script before installation.

```bash
cd /tmp/
wget https://raw.githubusercontent.com/tirtadji-com/Argon-One-Scripts-for-Raspi-running-Debian/main/argon1.sh
chmod a+x argon1.sh
sudo ./argon1.sh
```

## Usage

Upon installation of the Argon One Pi 4 script for Debian 10, the setting of the Argon one Pi 4 cooling system are as follows:

| CPU Temp | Fan Power |
| -------- | --------- |
| 55 C     | 10%       |
| 60 C     | 55%       |
| 65 C     | 100%      |

However, you may change or configure the Fan to your desired settings by using `argonone-config` to configure the fan behaviour.

### Commands

The script will generate several scripts and config files. The main commands are

- `argonone-config` to config the fan behaviour
- `argonone-uninstall` to remove all the scripts and services (conf file remains though)

I also added a custom command:

- `argonone-tempmon` which monitors the temperature using the Linux `sysfs`.

## Warning

This has been developed in an afternoon and has been only tested on my Raspberry Pi 4. No issues so far, but big disclaimer nonetheless: use at your own risk.

## Credit

Credit for [Cédric Meuter](mailto:cedric.meuter@gmail.com)