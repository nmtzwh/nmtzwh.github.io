---
layout: post
title: "Install bumblebee for laptop with Nvidia card"
date: 2016-06-22
---

Tom Zeng
22nd June, 2016

ref: [Bumblebee](https://en.opensuse.org/SDB:NVIDIA_Bumblebee)

~~~bash
zypper ar -f http://download.opensuse.org/repositories/X11:/Bumblebee/openSUSE_42.1/X11:Bumblebee.repo
zypper in bumblebee
usermod -G video,bumblebee tom
systemctl enable bumblebee
~~~

Check `/etc/modprobe.d/50-blacklist.conf` for line `blacklist nouveau`. If not add it.

~~~bash
mkinitrd
~~~

Install nvidia driver if want use its graphic card for games etc.
------------

~~~bash
zypper in linux-glibc-devel
zypper in -t pattern devel_kernel
~~~

Follow this [Install link](http://software.opensuse.org/download.html?project=X11%3ABumblebee&package=nvidia-bumblebee)

~~~bash
zypper in nvidia-bumblebee
zypper in nvidia-bumblebee-32bit
systemctl enable dkms
mkinitrd
reboot
~~~

Test function
-------------

~~~bash
optirun --status
optirun glxspheres
glxspheres
~~~
