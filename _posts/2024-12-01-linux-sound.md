---
layout: post
title: Music Playlist
date: 2024-12-01 07:00:10
last_updated: 2024-12-01 07:00:10
description: working with music
tags: music playlist
categories: music
featured: false
---

draft

## Linux Sound Pipewire

[Introduction to Pipewire]: https://bootlin.com/blog/an-introduction-to-pipewire/ "Introduction to Pipewire"
[Introduction to Pipewire]

[Pipewire]: https://pipewire.org/ "Pipewire"
[Pipewire]

PipeWire
* Capture and playback of audio and video with minimal latency.
* Real-time multimedia processing on audio and video.
* Multiprocess architecture to let applications share multimedia content.
* Seamless support for PulseAudio, JACK, ALSA, and GStreamer applications. 
* Sandboxed applications support. See Flatpak for more info.

PipeWire is used by bitwik-studio

Getting Pipewire
```
git clone https://gitlab.freedesktop.org/pipewire/pipewire.git
```

[Pipewire Documents]: https://docs.pipewire.org/ "Pipewire Documents"
[Pipewire Documents]

[More Pipewire Help]: https://gitlab.freedesktop.org/pipewire/pipewire/-/blob/master/README.md "Pipewire Help"
[More Pipewire Help]

Using tools
pw-cat can be used to play and record audio and midi. Use pw-cat -h to get
some more help. There are some aliases like pw-play and pw-record to make
things easier:
```
$ pw-play /home/wim/data/01.\ Firepower.wav
```

Running JACK applications
Depending on how the system was configured, you can either run PipeWire and
JACK side-by-side or have PipeWire take over the functionality of JACK
completely.
In dual mode, JACK apps will by default use the JACK server. To direct a JACK
app to PipeWire, you can use the pw-jack script like this:
```
$ pw-jack <appname>
```

If you replaced JACK with PipeWire completely, pw-jack does not have any
effect and can be omitted.
JACK applications will automatically use the buffer-size chosen by the
server. You can force a maximum buffer size (latency) by setting the
PIPEWIRE_LATENCY environment variable like so:
```
PIPEWIRE_LATENCY=128/48000 jack_simple_client
```
Requests the jack_simple_client to run with a buffer of 128 or
less samples.

# Pipewire and Pulse Audio
Running PulseAudio applications
PipeWire can run a PulseAudio compatible replacement server. You can't
use both servers at the same time. Usually your package manager will
make the server conflict so that you can only install one or the
other.
PulseAudio applications still use the regular PulseAudio client
libraries and you don't need to do anything else than change the
server implementation.
A successful swap of the server can be verified by checking the
output of
```
pactl info
```
It should include the string:

```
Server Name: PulseAudio (on PipeWire 0.3.x)
```
You can use pavucontrol to change profiles and ports, change volumes
or redirect streams, just like with PulseAudio.

## Inspecting the PipeWire state
To inspect and manipulate the PipeWire graph via GUI, you can use Helvum.
Alternatively, you can use use one of the excellent JACK tools, such as Carla,
catia, qjackctl, ...

However, you will not be able to see all features like the video ports.
```
pw-mon
pw-dot
pw-top
pw-dump
pw-cli
```
pw-mon dumps and monitors the state of the PipeWire daemon.
pw-dot can dump a graph of the pipeline, check out the help for
how to do this.
pw-top monitors the real-time status of the graph. This is handy to
find out what clients are running and how much DSP resources they
use.
pw-dump dumps the state of the PipeWire daemon in JSON format. This
can be used to find out the properties and parameters of the objects
in the PipeWire daemon.
There is a more complicated tool to inspect the state of the server
with pw-cli. This tool can be used interactively or it can execute
single commands like this to get the server information:
```
$ pw-cli info 0
```


