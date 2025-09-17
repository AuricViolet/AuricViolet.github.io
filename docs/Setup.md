---
title: Initial Setup
layout: default
nav_order: 2
parent: The Road Ahead
---

### Initial Setup
So before we can really start there's a small bit of housekeeping...

The first thing I should tell you about NixOS is the way we manage the OS.
Unlike most every other OS, NixOS for the most part, has all of it's configs written in a single directory `/etc/nixos`.

This houses our primeval `configuration.nix` which is the beginning of our entire operating system. If you're already poking around in there, you may have noticed `hardware-configuration.nix`. Of the two, we will mainly be dealing with `configuration.nix`.

We will be using this directory extensively for the remainder of our tutorials, so it's good to get familiar with it. It turns out this folder has special permissions, requiring an admin password to edit them. Our first step is to find a way around this so we don't have to edit these files directly from `/etc/nixos`, and we don't have to edit the permissions.

### Symlinking /etc/nixos

First we will move and rename /etc/nixos to /etc/nixosBackup, so we can replace it with a symlink.

`sudo mv /etc/nixos /etc/nixosBackup`
Next, we need to make a new folder somewhere, I'll use the home directory for ease of access, then copy all files from our Backup into the new folder:

`mkdir ~/nixos`
`sudo cp /etc/nixosBackup/* ~/nixos`

Finally, create a symlink in /etc/nixos to our new nixos folder.
`sudo ln -s ~/nixos /etc`

Here are all the commands together:


```bash
sudo mv /etc/nixos /etc/nixosBackup
mkdir ~/nixos
sudo cp /etc/nixosBackup/* ~/nixos
sudo ln -s ~/nixos /etc 
```
{% endhighlight %}
Awesome! Now we can freely edit all our nix files from ~/nixos.



