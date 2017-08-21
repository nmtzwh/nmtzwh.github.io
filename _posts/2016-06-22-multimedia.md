---
layout: post
title: "Some multimedia libraries and Additional repositoriest"
date: 2016-06-22
---

Add Repository
----------
[Additional repos](https://en.opensuse.org/Additional_package_repositories)

~~~bash
zypper -n ar -f http://ftp.gwdg.de/pub/linux/packman/suse/openSUSE_Leap_42.1/ packman
zypper -n ar -f http://download.opensuse.org/repositories/server:/http/openSUSE_Leap_42.1/ httpAdd
zypper ref
~~~

Install packages
-------------
Install

    k3b-codecs
    ffmpeg
    lame
    phonon-backend-vlc
    phonon4qt5-backend-vlc
    vlc-codecs
    flash-player

remove

    phonon-backend-gstreamer
    phonon4qt5-backend-gstreamer
