---
layout: post
title: Linux NVIDIA (draft)
date: 2024-07-22 17:37:00
last_updated: 2024-08-16 08:14:10
description: Linux NVIDIA
tags: linux nvidia personalnote
categories: linux
featured: false
---

draft

NVIDIA moeglichst nur über die Distri installieren!!
aptitude nvidia-driver
oder
apt-get install nvidia-driver

alles deinstallieren hat nur funktioniert mit:
apt-get purge *nvidia*

(Kernelquellen muessen vorhanden sein ..)
root@mutterschiff:~# uname -r
6.1.0-18-amd64
root@mutterschiff:~# apt install --reinstall linux-headers-$(uname -r)

03.03.2024 NVIDIA Treiber von NVIDIA heruntergeladen und über das RUN Script installiert.

######

check nvidia driver installed
https://linuxconfig.org/how-to-check-nvidia-driver-version-on-your-linux-system

root@mutterschiff:/home/fackelm2# nvidia-smi
Sun Mar 3 13:06:21 2024       
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 550.54.14 Driver Version: 550.54.14 CUDA Version: 12.4 |
|-----------------------------------------+------------------------+----------------------+
| GPU Name Persistence-M | Bus-Id Disp.A | Volatile Uncorr. ECC |
| Fan Temp Perf Pwr:Usage/Cap | Memory-Usage | GPU-Util Compute M. |
| | | MIG M. |
|=========================================+========================+======================|
| 0 NVIDIA GeForce GTX 1060 6GB Off | 00000000:01:00.0 On | N/A |
| 45% 41C P0 26W / 120W | 394MiB / 6144MiB | 0% Default |
| | | N/A |
+-----------------------------------------+------------------------+----------------------+

+-----------------------------------------------------------------------------------------+
| Processes:                                                                              |
| GPU GI CI PID Type Process name GPU Memory |
| ID ID Usage |
|=========================================================================================|
| 0 N/A N/A 733 G /usr/lib/xorg/Xorg 208MiB |
| 0 N/A N/A 1430 G firefox-esr 183MiB |
+-----------------------------------------------------------------------------------------+

Please note that both above solutions will work only if the actual NVIDIA module is loaded.

Another place where to find NVIDIA driver version is to consult Xorg X server log files:
root@mutterschiff:/home/fackelm2# more /var/log/Xorg.0.log | grep "X Driver"
[     6.031] (II) NVIDIA dlloader X Driver 550.54.14 Thu Feb 22 01:31:16 UTC 2024

Retrieve module version
If all above commands fail because you are unable to load NVIDIA module you can always see NVIDIA version number by
directly retrieving nvidia.ko module version using modinfo command. The below command will check for NVIDIA driver
version under your currently running kernel:

root@mutterschiff:/home/fackelm2# find /usr/lib/modules -name nvidia.ko
/usr/lib/modules/6.1.0-18-amd64/updates/dkms/nvidia.ko

#####

debian nvidida prorietary driver
https://wiki.debian.org/NvidiaGraphicsDrivers

$ lspci -nn | egrep -i "3d|display|vga"

# apt install linux-headers-amd64

change /etc/apt/source.list
contrib non-free

# apt update

# apt install nvidia-driver firmware-misc-nonfree

#########

anon21050130
Juli 2022

When I open the folder, where the driver is, in the terminal and type “./NVIDIA-Driver.run” (this is the name I gave to
the file) this appears:

You appear to be running an X server; please exit X before installing. For further details, please see the section
INSTALLING THE NVIDIA DRIVER in the README available on the Linux driver download page at www.nvidia.com 312.

In section 4 - Installing the NVIDIA Driver on the Readme page it says to exit the X server, but it doesn’t say how to
do that.

I typed these two commands in the terminal, the first one the screen went black and my PC restarted and when it came
back I tried it and the same error appeared. The second, nothing happened and after the retry, the same error.

systemctl stop display-manager
systemctl stop lightdm.service

Now it’s up to you, friends, it’s you I’m counting on.

    I gave up installing by the runfile installer. I preferred to install with this command: sudo apt-get install nvidia-driver-515 

    erstellt
    Juli 2022
    letzte Antw.
    Aug. 2022
    4
    Antworten
    61,2 T.
    Aufrufe
    2
    Benutzer
    2
    „Gefällt mir“
    3

generix
Top Contributor
Juli 2022

You shouldn’t use the runfile installer at all, please use the driver from the repo of your distribution.
sudo systemctl isolate multi-user.target
should turn off graphics.
anon21050130
Aug. 2022

I gave up installing by the runfile installer. I preferred to install with this command:

sudo apt-get install nvidia-driver-515


