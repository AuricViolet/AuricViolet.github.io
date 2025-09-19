---
title: Preparation
layout: default
nav_order: 2
---

### Installation

I'll only mention install briefly as there's really only a few things to consider.

1. Desktop Environment - There's a large number of desktop environments that NixOS can run, and this install list is by no means all of them. However, the nix options and customization support for Gnome and KDE I can attest to being top notch, where I cannot speak to how well documented and supported the other Desktops are.

2. Display Server Protocol - Wayland vs X11, at the time of writing, Wayland is a modern display server for Linux, set to replace X11(eventually) and is more performant. Some desktop environments offer full support for Wayland, while others do not, or have it available in an experimental state.

3. Password - A password is required for sudo operations, amd since most nixos commands require sudo, you must set a password for your initial user account. 

If it matters to you at all, I'll be using a Wayland display server, with a KDE desktop environment for most of these tutorials. 

As for filesystem, use what you like, but I'd recommend sticking with the default EXT4 or BTRFS.





