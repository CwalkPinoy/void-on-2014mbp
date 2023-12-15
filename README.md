# void on 2014mbp
 quick fixes for 2014 macbook pro running void xfce

```
if mouse doesnt work in post-install use this

sudo vi /etc/modprobe.d/usbmouse.conf
blacklist usbmouse

important: have a network switch on hand or a wire for ethernet (use a thunderbolt adapter) before booting
install void normally
reboot

open xfce4-terminal

for wifi:

uname -r (note the first 2 numbers)
sudo xbps-install -S
sudo xbps-install -u xbps
sudo xbps-install -S linux<x>.<y>-headers (use those first 2 numbers)
sudo xbps-install -S void-repo-nonfree
sudo xbps-install -S
sudo xbps-install -S broadcom-wl-dkms
sudo xbps-install -Su
sudo reboot

for bluetooth (with applet):

sudo xbps-install -S bluez blueman
sudo ln -s /etc/sv/bluetoothd /var/service
launch blueman-applet in terminal, click yes to have it autostart
```
