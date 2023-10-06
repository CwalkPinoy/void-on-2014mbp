# void on 2014mbp
 quick fixes for 2014 macbook pro running void xfce


/etc/rc.local
```
modprobe -r usbmouse
modprobe -r bcm5974
modprobe bcm5974
```
```
xbps-install -S broadcom-wl-dkms
(check error message about missing headers)
xbps-install -S linux<x>.<y>-headers
xbps-reconfigure -a
```