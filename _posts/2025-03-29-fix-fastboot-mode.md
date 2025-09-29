---
layout: post
title: Fix Fastboot Mode Device State Locked
subtitle: A guide on how to Fix Fastboot Mode Device State Locked (Unlockable)
#thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [Fastboot, android, graphineOS, device state locked]
author: kp
---



In this guide, we will show you the steps to fix the Fastboot Mode Device State Locked (Unlockable). There’s a generic rule of thumb that you need to unlock the bootloader before flashing any custom ROM. While that still holds true, however, nowadays, a bunch of custom ROMs allow you to relock the bootloader as well. Some of the well-known players in this domain include the likes of [GrapheneOS](https://grapheneos.org/), HellucaOS, and [CalyxOS](https://calyxos.org/).

What these ROMs do is they erase the stock Android Verified Boot key [via the fastboot erase avb_custom_key command] and replace it with their own “non-stock/custom” Verified Boot key [the name of the file is avb_pkmd.bin and it is flashed in the avb_custom_key partition via the fastboot flash avb_custom_key avb_pkmd.bin command].

**Device State Locked (Unlockable)**

Since all these tasks are carried out after flashing the ROM, you can now boot to the OS and have the ROM up and running in a locked bootloader ecosystem! While that’s all well and good, what if you want to unlock the bootloader for some reason? Well, in such cases, one would generally use the bootloader unlocking command to get the job done.

However, this might not get the job done and could complicate matters even more as your device still has the custom avb_pkmd.bin file. So you’ll first have to erase this file and replace it with the stock one, only then can you proceed with the bootloader unlocking process. This in turn should also fix the Fastboot Mode Device State Locked (Unlockable) issue in the Fastboot Mode. So without any further ado, let’s get started.


If possible, do take a backup of all the data on your device. 

To begin with, download and extract Android SDK Platform Tools on your PC.
Now enable USB Debugging & OEM Unlocking and connect your device to PC.
Then open the Command Prompt inside the platform-tools folder and type in:

`adb reboot bootloader`

After that, type in the below command to unlock the bootloader on your device:

`fastboot flashing unlock`


Use the Volume key to highlight Unlock Bootloader and press the Power key to confirm
Once the bootloader is unlocked, you should boot the device back to the Fastboot Mode.
Once that’s done, erase the custom Android Verified Boot key using the below command:

`fastboot erase avb_custom_key`

Once done, you may now flash the stock firmware via the Android Flash Tool/script file.
That’s it. These were the steps to fix the Fastboot Mode Device State Locked (Unlockable). 
