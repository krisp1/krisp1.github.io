---
layout: post
title: AWUS036ACH Automated Driver Install Script
subtitle: Bash Script to automate install of AWUS036ACH Wireless Alfa drivers instead of manually running every command. Works on Kali Linux/Debian Systems 
#thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [realtek, alfa, aircrack-ng]
author: kp
---

⚠️ This repository is not compatible with Hyper-V!
Please avoid using Hyper-V — use VirtualBox, VMware, or native hardware instead.
Overview

This bash script automates the installation of Realtek wireless drivers for the AWUS036ACH on Linux systems. It performs the following tasks:

    Checks for the Linux distribution.
    Installs git if not present.
    Updates the system.
    Installs kernel headers necessary for building the driver.
    Installs Realtek drivers.
    Clones the rtl8812au repository from Aircrack-ng.
    Compiles the drivers.
    Prompts for a reboot to apply changes.
    Optionally removes any existing driver installations.

Prerequisites

    The script must be run as root. Use sudo or log in as the root user.
    Supported Linux distributions:
        Debian-based (e.g., Debian, Ubuntu)
        Fedora-based (e.g., Fedora, RHEL)

Usage
Download the script or copy its content into a file.
Clone the repository:
~~~
git clone https://github.com/Khatcode/AWUS036ACH-Automated-Driver-Install
cd AWUS036ACH-Automated-Driver-Install
~~~

Make the script executable:
~~~
chmod +x Alfasetup.sh
~~~
Run the script as root:
~~~
sudo ./Alfasetup.sh
~~~
or combine the commands:

git clone https://github.com/Khatcode/AWUS036ACH-Automated-Driver-Install && cd AWUS036ACH-Automated-Driver-Install && chmod +x Alfasetup.sh && sudo ./Alfasetup.sh

Script Steps

    Root Check:
        Verifies if the script is run with root privileges.

    Distribution Detection:
        Identifies the Linux distribution to use the appropriate package manager (apt-get or dnf).

    Git Installation:
        Checks for the presence of git and installs it if necessary.

    System Updates:
        Updates the system, upgrades packages, and performs a distribution upgrade.
        Automatically restarts services during package upgrades without user interaction.

    Kernel Headers Installation:
        Installs the necessary kernel headers required for building the driver.

    Realtek Drivers Installation:
        Installs Realtek wireless drivers using the detected package manager.

    Existing Driver Removal:
        Checks if a version of the driver is already installed.
        Prompts the user to remove the existing installation if found, which helps avoid conflicts.

    Additional Drivers Installation:
        Clones the rtl8812au repository from Aircrack-ng and compiles the drivers.

    Executable Building:
        Compiles the necessary rtl8812 executable files into binary applications.

    Installation:
        Installs the compiled binaries into the appropriate locations on the file system.

    Reboot Prompt:
        Notifies the user that a system reboot is necessary to apply changes and initiates a countdown.

Note

    The script will prompt for a system reboot after completing the installation.
    It is recommended to remove any existing driver installations before proceeding with the new installation to ensure compatibility and avoid potential issues.
