---
title: Encrypted Debian Install
description: 
published: true
date: 2021-09-25T17:23:38.851Z
tags: 
editor: markdown
dateCreated: 2021-09-25T17:19:15.700Z
---

# Encrypted Debian Install (UEFI, No LVM, KDE Plasma) - Complete setup


# 1- Create the bootable media


Note: To avoid any issue, always use the [non-free firmware iso](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/). For Debian 11 it's `firmware-11.0.0-amd64-netinst.iso` from [Here](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/11.0.0+nonfree/amd64/iso-cd/).

## Make the bootable media:

Use [Ventoy](https://ventoy.net/) or dd:

```
dd bs=4M if=path/to/debian.iso of=/dev/sdx status=progress oflag=sync
```


# 2- Installation

## Locale and keyboard layout

Language: English
Location: Your location (in my case: other/Europe/France)
Locale: en_US.UTF-8
Keymap: Your keymap (in my case: French)

## Hostname and users

Hostname: debian
Domain name: [Blank Value] (remove `home`)
Root: Give it a strong password
Full name of the user account: [Blank Value]
Username of the user account: Choose an username
Password: Give it a strong password


## Partitioning

(If asked: Force UEFI installation: YES)

Partition method: Manual

Choose a your drive
Create partition table

Choose "FREE SPACE" of this drive
Create a new partition
Size: `500 MB`
Begining
Name: [Empty Value]
Use as EXT4 jounrnaling file system"
Mount as /boot
Click "Done setting up the partition"

Choose "FREE SPACE" of this drive
Create a new partition
Size: `500 MB`
Begining
Name: [Empty Value]
Use as "EFI System Partition"
Click "Done setting up the partition"


Choose "FREE SPACE" of this drive
Create a new partition
Size: all available (default value)
Name: [Empty Value]
Use as "Physical volume for encryption"
Erase data: no
Click "Done setting up the partition"

## Encryption

Configure encrypted volumes
Write the changes: YES
Create encrypted volumes
Choose the crypto partition
Finish
Encryption passphrase: Choose one
Done

Choose the encrypted volume
Mount point /
Click "Done setting up the partition"
Done

Click "Finish partitioning and write changes to disk"

When asked to setup swap, choose "No" (we'll setup a swapfile later, that way our swap will be encrypted)
Write the changes to disk

## Installation

Mirror country: Choose a country with good internet near you
Choose deb.debian.org
Proxy: [blank]

Participate in the package usage survey: No

Software to install:

- KDE Plasma
- standard system utilities

Untick everything else (including "Debian desktop environment")

# 3- Post-Install

TODO