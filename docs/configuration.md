---
title: Configuration
layout: default
nav_order: 2
parent: Preparation
---

### Configuration

Now we're going to start configuring things "the nix way".

If you open `configuration.nix` in any text editor, you will see that there's a lot of options here already, it may be a bit overwhelming at first, but I promise it isn't as confusing as it seems. 

Each line is what's called an "option", NixOS has thousands of these, for doing anything and everything you can imagine to a Linux operating system. In short, you write out the option that you want, assign it a value, and NixOS does the rest for you. 

"Okay, but how will I know what to write in the config to change what I want?" you might be wondering. 

Well, thankfully there's 3 excellent sources of this information, it might be worthwhile to bookmark them.

[NixPKGS] - the Nix software repository search, contains most any software you can imagine to install on your machine.
[NixOS Options] - A dictionary of every configuration option NixOS supports, along with some helpful tips on usage and syntax.
[NixOS Wiki] - The official wiki (there is a non-official one out there). Contains in-depth configurations and explanations.

These 3 sources will save you innumerable headaches.

So with all this information, what should we configure first? Let's start small. 
If you go to the [NixPKGS] page, and search `kittysay`, then click on the package name to expand it, you'll see 3 tabs under the "How to install?", click on NixOS Configuration, then copy the bolded package name in this case it's just `kittysay`. 

Paste this package name into your `configuration.nix` under the square braces of environment.systemPackages.Now, save the file. You do not need to include "pkgs." prior to your package name, as the default config already has ` = with pkgs;` after it, which tells NixOS to add the prefix itself to all apps in the list.

Now, if you try running kittysay from a terminal, you might notice it's not installed. 
NixOS needs to rebuild the system each time you change your configuration, this can be just to make a small change, or a huge one depending on what you're doing. This is how NixOS works it's magic, to do this, open a terminal window and run `sudo nixos-rebuild switch`.

This command tells NixOS to read the config, line by line, and rebuild it according to any changes made, then, switch to the new system build. Once complete, in that terminal you'll see that we can now run`kittysay Congratulations`. 

Congrats! You now have your first **generation**, you'll have many many more, and with each one you'll get closer to your perfect config. 

With each reboot, you'll see a list of previous generations in your boot menu, this will allow you to quickly revert to a previous generation if anything causes the new generation to fail or bug out. 

[NixPKGS]: https://search.nixos.org/packages?channel=25.05&
[NixOS Options]: https://search.nixos.org/options?channel=25.05&
[NixOS Wiki]: https://wiki.nixos.org/wiki/NixOS_Wiki
