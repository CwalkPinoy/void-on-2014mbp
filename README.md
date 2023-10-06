# void on 2014mbp
 quick fixes for 2014 macbook pro running void xfce

/etc/rc.local
modprobe -r usbmouse
modprobe -r bcm5973
modprobe bcm5974

sudo xbps-install -S broadcom-wl-dkms

sudo xbps-install -S linux6.13-headers

sudo xbps-reconfigure -a