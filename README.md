# usbip-service-shell

**usbip-service-shell** is a set of Linux services for the **USB/IP Project** that allow you to take no actions needed for handling sudden reboots and/or plug/unplug USB devices on fly

## Download
You can download the alpha version [here](https://github.com/alpertsev/usbip-service-shell/tree/v0.1.0)

## Requirements, Conventions or Software Version Used ##
Host - a Raspberry Pi 3B+ single board computer with Ubuntu 20.04.1 LTS (GNU/Linux 5.4.0-1034-raspi armv7l)

Client - a GIGABYTE™ C246WU4 i3-8100 workstation with Ubuntu 20.04.1 LTS (GNU/Linux 5.4.0-1034-genetic x86_64)

On both machines installed:
 * OpenSSH_8.2p1
 * OpenSSL 1.1.1f 31 Mar 2020
 * usbip-utils 2.0
 * [Passwordless](https://www.redhat.com/sysadmin/passwordless-ssh) SSH Login for the other root.

## Instructions
 - copy files [here](https://github.com/alpertsev/usbip-service-shell/tree/main/host) to your Host Computer and files [here](https://github.com/alpertsev/usbip-service-shell/tree/main/client) to your Client Computer as file structures dictate.
 - change IP-addresses of your host / client in the corresponded **/etc/usbip.conf** files on both computers
 - run **sudo systemctl enable usbipd && sudo systemctl start usbipd** on both computers
 - run **sudo systemctl enable usbipd-restart** on your Client Computer
 - enjoy!

## Known Issues
- not yet

## Development
 - Power Management implementation for USBIP Host
 - make BT version, not Wi-Fi
 - speed up ssh-commands
 - Proximity Sensor Interface to wake up the host
 
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgment
- [Takahiro Hirofuchi](http://usbip.sourceforge.net/) - A famous USB-IP implementation proven by years!!
- [Alexey Pertsev](https://www.alpertsev.com/) - usbip-service-shell-v0.1.0 developer - [Donate](https://paypal.me/alpertsev)

## License
[Apache-2.0](http://www.apache.org/licenses/LICENSE-2.0)
