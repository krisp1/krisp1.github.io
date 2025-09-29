---
layout: post
title: Install guide for GraphineOS 
subtitle: GrapheneOS is a private and secure mobile operating system with great functionality and usability.
#thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [GraphineOS, android, AOSP, secure, mobile, google, pixel]
author: kp
---


As an alternative Android operating system, GrapheneOS doesn’t officially come pre-installed on any device.

The Android operating system is widely used across smartphones, tablets, smartwatches, smart TVs, and more, making it the most popular OS in the world. The customizable features and user-friendly options are the two main reasons for its widespread popularity. The Android ecosystem allows users to customize, install, and modify various files on their devices. 

If you have a compatible phone, you can install GrapheneOS yourself through a few relatively straightforward steps. To help you make the installation as smooth as possible, this guide will explain:

Which devices you can install GrapheneOS on
What other prerequisites you should meet
How to install GrapheneOS using the two available methods

**Can You Install GrapheneOS on Any Phone?**

You can’t install GrapheneOS on any device—it’s only available on a select few Google Pixel models with the necessary security hardware. The current list of supported devices includes:

Pixel 6 / 6a / 6 Pro
Pixel 7 / 7a / 7 Pro
Pixel 8 / 8a / 8 Pro
Pixel 9 / 9 Pro / 9 Pro XL / 9 Pro Fold
Pixel Fold
Pixel Tablet

This means you can’t install GrapheneOS on Samsung phones or other devices that support Android, even though the OS serves as Android’s security-focused counterpart.

Note that while older models like the Pixel 3 and Pixel 4 series also support GrapheneOS, they’re considered end-of-life devices. 

#### What Do You Need To Install GrapheneOS?

Installing GrapheneOS isn’t as simple as downloading and executing a specific file. The following table outlines the installation prerequisites besides a compatible Pixel phone:

**Prerequisites**

Download the GrapheneOS factory images ZIP and its signature for your model device from here: 
[GraphineOS](https://grapheneos.org/releases)


**Developer Options enabled**

On your Pixel, go to Settings > About, and tap Build number seven times to unlock Developer Options. Then, go to System > Developer Options and enable OEM unlocking to ensure the bootloader can be unlocked.

**Computer with USB ports**

You need a wired connection to install GrapheneOS. You can do so on any USB-enabled device with the following operating systems:

Windows 10/11
macOS (Ventura, Sonoma, Sequoia)
ChromeOS
GrapheneOS
Some Linux distributions (Ubuntu, Debian, Arch)
USB-C cable

Ideally, you’ll use the cable that came with your Pixel or another high-quality option that ensures a stable connection.

**Appropriate driver/software setup**

If you’re installing GrapheneOS on a Pixel 4a (5G) or later, you don’t need specific drivers  ( although you might ) because Windows 10/11 includes a generic fastboot driver. For older versions, you might need a dedicated driver.

**Latest OS and firmware versions**

While this isn’t a necessity, it’s best to update the phone’s stock OS and firmware for best results.

GrapheneOS installation removes all existing user data on your phone. That’s why you must back up your personal files and data beforehand. Once the process starts, your data will be unrecoverable.

There are two methods available for Installing GrapheneOS on your device.
Depending on your skills and tech background, you can choose between the two GrapheneOS installation options:

WebUSB-based installer (web installer for short)

Command-line installer (CLI)

Even if you’re tech-savvy and know your way around command-line tools, the web installer is objectively simpler. As some users might still prefer CLI, we’ll break down both options below.

1. How To Install GrapheneOS Using the Web Installer

The GrapheneOS web installer offers user-friendly guidance through the installation process. To access it, you should first boot your Pixel into bootloader mode. You can do this by:

Turning off your phone
Pressing and holding the volume down + power button
Once you see a red triangle and “Fastboot Mode,” connect your Pixel to the computer via USB. Then, visit grapheneos.org/install/web in your browser (Preferably Chrome, Edge, or Chromium).

The site will automatically detect that you’re in bootloader mode, after which you can start the installation process. Here are the steps you should follow:

Click Unlock bootloader on the web page. To confirm the unlocking, use the volume keys to navigate to “Yes” and press the power button.
Click Download release on the installer page and choose your device to download GrapheneOS factory images.
Go back to the installer page and click Flash release. Monitor the status in the installer and wait for the process to finish.
Click Lock bootloader in the installer to ensure maximum security.
Press the power button to boot into GrapheneOS.
If you run into any issues during the process, don’t panic. Encountering errors like your device not being found isn’t a major issue, and you can troubleshoot them in several ways, such as:

Using a different USB port or cable
Checking if OEM unlocking is enabled
Rebooting back into bootloader (using volume down + power)

2. Installing GrapheneOS Using CLI

While CLI GrapheneOS installation is more technical, the general steps are largely the same. The only difference is that you’ll use the command-line tools instead of a standard visual interface. It's really fairly straight forward and I personally found it simpler than the WebUSB-based installer installation option.

Specifically, you’ll first need the fastboot tool. 


**Download ADB and Fastboot with Installation on Windows 7, 8, 10, 11**

ADB Fastboot is a method to execute commands via PC for tasks like flashing firmware and unlocking bootloaders.

This section will guide you on downloading and installing ADB and Fastboot on Windows 7, 8, 8.1, Windows 10, and Windows 11.

**What is ADB?**

Android Debug Bridge (ADB) is a client-server program that allows users to easily connect an Android device and a Windows computer using the USB driver. As mentioned above, ADB is an important part of the Android Software Development Kit (Android SDK).

You can run an ADB command on your Android device via the Platform Tools using a computer to transfer files, install or uninstall apps, flash firmware, unlock the device bootloader, and more. It basically makes it easy for you to complete the required development work or even test some aspects on the Android handset.

**What is Fastboot?**

Fastboot is a protocol that usually upgrades the flashable file system on Android devices. This tool works as an alternative method to the recovery mode for implementing updates and installations. Whenever your device boots in the Fastboot mode, you can easily modify or tweak system image files from the PC via a USB connection.

These days most Android devices do support Fastboot mode and Google made it easy for users and developers to use the Android SDK Platform Tools to get the combined benefit of ADB and Fastboot.

Download and Install ADB and Fastboot on Windows 7, 8, 8.1, 10 and 11
The ADB and Fastboot tools are compatible with all Windows 7 / 8.1 / 8 / 10 versions for both the 32-bit and 64-bit. Now, you can follow the requirements and installation guide below.

Users can download and install ADB and Fastboot tools on Windows 7, 8, 10, and 11 to connect and manage Android devices efficiently by following specific requirements and steps. 






We all know that Android OS devices are easily customizable with the advantages of flashing custom firmware, installing custom recovery, flashing custom modules, unlocking the bootloader, flashing root access, and so on. If you’re new to flashing a third-party firmware or unlocking the bootloader, it’s better to use the PC’s ADB Fastboot (Platform Tools) to run commands to the connected Android device easily. ADB driver is also a necessary part of Android development.





***Requirements:***

You require a Windows computer and a USB data cable to connect your Android device.
Make sure to Turn On USB Debugging mode on your phone.
Open the Settings app on your phone.
Go to the About Phone section.
Tap on Build Number 7 times continuously to get a successful message that says, ‘You are now a developer.’ It means you’ve enabled Developer Mode on your device.
Now, go back to the Settings menu again, and tap on Developer Options.
Make sure to Turn On the Developer Options toggle at the top.
Then Turn On the USB Debugging toggle. If prompted, select Allow USB Debugging, and tap on OK.
Download and Install the latest USB Driver on your PC. Just run the installer program and follow the on-screen prompts to complete installing.
Download the Android SDK Platform Tools on the PC.
Charge your mobile device more than 50% to prevent shutdowns.
Download ADB and Fastboot Tools
ADB and Fastboot drivers for Windows, Linux, macOS: 

For Windows: https://github.com/fawazahmed0/Latest-adb-fastboot-installer-for-windows
For Linux: https://itsfoss.com/install-adb-fastboot-linux/
For macOS:  https://dl.google.com/android/repository/platform-tools-latest-darwin.zip

**Steps to Install ADB and Fastboot on Windows**

Now, you’re ready to get into the file copying or transferring process to your Android device via a computer with the help of ADB commands. So, without further ado, let’s proceed.

First, connect your Android device to your computer using the USB cable properly.
We assume you’ve already installed the Android USB Driver on your system. If not, do it now. [Important]
Obviously, you’ve enabled USB Debugging too. If not, do it right now. [Important]
Next, you have to extract the downloaded ADB and Fastboot Tools on your PC to a suitable place like the desktop screen or inside any folder/drive.

Open the extracted Android SDK Platform Tools (ADB and Fastboot Tools) folder.


Press and hold the Shift key + mouse right-click on an empty space inside the folder.
ADB and Fastboot Tools

It’ll open a context menu and you’ll have to select Open PowerShell window here. (On some PCs, it’ll look like Open command window here)

If prompted, click on Yes to open the command window.
Now, you’ll need to input the following ADB command and hit Enter to connect your Android device in the ADB Mode:

`adb devices`

Once you can see a specific device ID on the command prompt window, that means your device is successfully connected in ADB mode.
Now, you can proceed with your respective ADB commands, whatever you want to run.
Please be aware that if the connection is lost, you should re-enable the USB Debugging feature on your device and reconnect it using the USB data cable. Then, retry the Android SDK Platform Tools steps with the command line “adb devices” to ensure the mode is correct.