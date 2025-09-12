---
title: Home
layout: home
nav_order: 1
---
I was motivated to create this page after my own struggles with getting started with NixOS. The documentation is one of the biggest blind spots for Nix and NixOS, and I figured, "what better way to contribute to the NixOS ecosystem than to share my own struggles and triumphs." I hope that this page might help others in the future to learn from my mistakes, or at least avoid painful troubleshooting.

But why NixOS? Isn't insert popular Arch/Debian distro better and more practical for my use case?

Have you ever been sitting at a black recovery terminal, wondering how everything went so wrong after trying to simply upgrade a driver?

Do you love to tinker, run bleeding-edge updates, and customize your OS, but find it difficult to experiment without breaking things?

Do you find yourself copying and pasting large chunks of terminal code from tutorials or wiki pages to fix an issue, only to have to look them up again next month when you inevitably reinstall to fix some annoying problem?

Then maybe, just maybe, NixOS is for you after all.

What is NixOS?

NixOS is an atomic, reproducible, and functional operating system.

Atomic: updates are incapable of breaking the OS to an irrecoverable state, as you can always roll back to a previous one. NixOS handles this automatically.

Reproducible: If two machines have the same configuration code, they will be identical, down to the lowest level. Meaning there's no more "Sorry, but x works on my machine."

Functional: Configs are abstracted to a higher level and written in plain English. You tell the operating system what to do, and it deals with all the dirty and often confusing commands needed to do it.
