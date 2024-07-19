---
layout: post
title: SSL BigSix as soundcard for Linux
date: 2024-07-19 18:35:13
description: Using BigSix as a soundcard for Linux Debian 
tags: linux todo
categories: linux
featured: false
---

No problems. Linux Debian see the BigSix after USB Connect. I use pavucontrol for configurations. 

````markup 
# pavucontrol 
````

<a href="https://wiki.debian.org/PulseAudio#Basic_Configuration">https://wiki.debian.org/PulseAudio#Basic_Configuration</a>

To reread the config files ~/.config/pulse/daemon.conf and /etc/pulse/daemon.conf, one can restart pulse:

````markup 
$ systemctl --user restart pulseaudio.service
````

- ALSA (works for Bitwig and BiGSiX)
- PulseAudio is on top of ALSA
- pavucontrol (optional package for PulseAudio) or pamixer

Stop running the PulseAudio daemon for a while

If you suspect trouble with a running PulseAudio daemon in your systemd user session, you can switch it off:

````markup 
systemctl --user mask pulseaudio.socket
systemctl --user stop pulseaudio.service
````

and then to switch it on:

````markup 
systemctl --user unmask pulseaudio.socket
systemctl --user start pulseaudio.service
````


More bash history infos ;-) (todo)
````markup
#wire plumber conrtrol CLI 
$wpctl status

aplay -lL (liste der Karten / Devices)

TIPPS: (NOT FOR ME)
amixer -c2 #or correct card index (Angabe der Kartennummer von "aplay -lL" 
pactl list cards
pactl list sources
#During a recording
pactl list source-outputs

PIPEWIRE
Pipwire activ?
systemctl status --user pipewire

pipewire
pipewire -h
pipewire --version
systemctl --user restart pipewire.service

w-link -l
pw-link -o
pw-link -i
pw-link -l -o -I
pw-link -l -i -I
pw-link -l 98 89
pw-link -l 107 89
pw-link -h
pw-link -d 96

pw-mon | egrep "card_name" (zeigt alle erkannten devices an)
pw-mon | grep SiX 
pw-mon | egrep "SiX"
pw-mon 

########################################################################
speaker-test (vorsicht rauschen laut)
speaker-test -c 2 -t /usr/lib/libreoffice/share/gallery/sounds/applause.wav
speaker-test -c 2 -t wav
########################################################################
SHOW AUDIO DEVICES (no usb?)
lspci | grep Audio 


lspci card0
lspci -t
lspci
########################################################################
vi /etc/pulse/client.conf

multimedia-jack
qjackctl
JACK
########################################################################
Alsa

aplay -l (list all soundcards and digital audio devices)
aplay -L (list device names)
aplay -D (select PCM by name)

aplay -vv /usr/lib/libreoffice/share/gallery/sounds/applause.wav
aplay -vv -D front:CARD=SiX,DEV=0 /usr/lib/libreoffice/share/gallery/sounds/applause.wav
aplay -vv -D usbstream:CARD=SiX,DEV=0 /usr/lib/libreoffice/share/gallery/sounds/applause.wav
aplay -vv -D dmix:CARD=SiX,DEV=0 /usr/lib/libreoffice/share/gallery/sounds/applause.wav
aplay -vv -D plughw:CARD=SiX,DEV=0 /usr/lib/libreoffice/share/gallery/sounds/applause.wav

alsamixer &
cd /proc/asound/card0
cd /proc/asound/card1


cd /proc/asound/card2
more /proc/asound/cards (to find all cards !)
more /proc/asound/card2/id (SiX)
more /proc/asound/card2/pcm0c/sub0/hw_params
more /proc/asound/card2/stream0
more /proc/asound/devices (to show all audio devices ..)

more /proc/asound/oss/sndstat 
more /proc/asound/oss/devices 
more /proc/asound/pcm0c/sub0/info 
more /proc/asound/pcm0c/sub0/hw_params 
more /proc/asound/pcm0c/sub0/status 
more /proc/asound/pcm0p/info 

more /proc/asound/oss/sndstat
Sound Driver:3.8.1a-980706 (ALSA emulation code)
Card config: 
HDA Intel PCH at 0xa3230000 irq 127
HDA NVidia at 0xa3080000 irq 17
Solid State Logic BiG SiX at usb-0000:00:14.0-5, high speed
Blackmagic Design Blackmagic Design at usb-0000:00:14.0-6, high speed
Audio devices: NOT ENABLED IN CONFIG


more /proc/asound/pcm
00-00: ALC892 Analog : ALC892 Analog : playback 1 : capture 1
00-01: ALC892 Digital : ALC892 Digital : playback 1
00-02: ALC892 Alt Analog : ALC892 Alt Analog : capture 1
01-03: HDMI 0 : HDMI 0 : playback 1
01-07: HDMI 1 : HDMI 1 : playback 1
01-08: HDMI 2 : HDMI 2 : playback 1
01-09: HDMI 3 : HDMI 3 : playback 1
02-00: USB Audio : USB Audio : playback 1 : capture 1
03-00: USB Audio : USB Audio : capture 1

more /proc/asound/SiX/pcm0p/sub0/info
stream: PLAYBACK

more /proc/asound/SiX/pcm0c/sub0/info
stream: CAPTURE

more /proc/asound/Design/stream0
Blackmagic Design Blackmagic Design at usb-0000:00:14.0-6, high speed : USB Audio

````

