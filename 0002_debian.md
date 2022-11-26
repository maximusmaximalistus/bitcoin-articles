# !!In construction!!

# Overview:
This guide will install Debian Linux OS in HDD, external hard drive or USB stick, both in EFI and Legacy BIOS.

It uses LVM on LUKS 

https://wiki.archlinux.org/title/dm-crypt/Encrypting_an_entire_system#LVM_on_LUKS

```
+-----------------------------------------------------------------------+ +----------------+
| Logical volume 1      | Logical volume 2      | Logical volume 3      | | Boot partition |
|                       |                       |                       | |                |
| [SWAP]                | /                     | /home                 | | /boot          |
|                       |                       |                       | |                |
| /dev/MyVolGroup/swap  | /dev/MyVolGroup/root  | /dev/MyVolGroup/home  | |                |
|_ _ _ _ _ _ _ _ _ _ _ _|_ _ _ _ _ _ _ _ _ _ _ _|_ _ _ _ _ _ _ _ _ _ _ _| | (may be on     |
|                                                                       | | other device)  |
|                         LUKS2 encrypted partition                     | |                |
|                           /dev/sda1                                   | | /dev/sdb1      |
+-----------------------------------------------------------------------+ +----------------+
```

The boot partition will not be encrypted!!


## Language, location, locales, keyboard and network.

![alt text](./images/VirtualBox_Debian_11.5-1.png)

![alt text](./images/VirtualBox_Debian_11.5-2.png)

![alt text](./images/VirtualBox_Debian_11.5-3.png)

![alt text](./images/VirtualBox_Debian_11.5-4.png)

![alt text](./images/VirtualBox_Debian_11.5-5.png)

![alt text](./images/VirtualBox_Debian_11.5-6.png)

![alt text](./images/VirtualBox_Debian_11.5-7.png)

![alt text](./images/VirtualBox_Debian_11.5-8.png)

![alt text](./images/VirtualBox_Debian_11.5-9.png)

## Users.

![alt text](./images/VirtualBox_Debian_11.5-10.png)

![alt text](./images/VirtualBox_Debian_11.5-11.png)

![alt text](./images/VirtualBox_Debian_11.5-12.png)

![alt text](./images/VirtualBox_Debian_11.5-13.png)

![alt text](./images/VirtualBox_Debian_11.5-14.png)

![alt text](./images/VirtualBox_Debian_11.5-15.png)

## Partitioning. 
### BIOS boot area, EFI partition and /boot partition.

![alt text](./images/VirtualBox_Debian_11.5-16.png)

![alt text](./images/VirtualBox_Debian_11.5-17.png)

![alt text](./images/VirtualBox_Debian_11.5-18.png)

![alt text](./images/VirtualBox_Debian_11.5-19.png)

![alt text](./images/VirtualBox_Debian_11.5-20.png)

![alt text](./images/VirtualBox_Debian_11.5-21.png)

![alt text](./images/VirtualBox_Debian_11.5-22.png)

![alt text](./images/VirtualBox_Debian_11.5-23.png)

![alt text](./images/VirtualBox_Debian_11.5-24.png)

![alt text](./images/VirtualBox_Debian_11.5-25.png)

![alt text](./images/VirtualBox_Debian_11.5-26.png)

![alt text](./images/VirtualBox_Debian_11.5-27.png)

![alt text](./images/VirtualBox_Debian_11.5-28.png)

![alt text](./images/VirtualBox_Debian_11.5-29.png)

![alt text](./images/VirtualBox_Debian_11.5-30.png)

![alt text](./images/VirtualBox_Debian_11.5-31.png)

![alt text](./images/VirtualBox_Debian_11.5-32.png)

![alt text](./images/VirtualBox_Debian_11.5-33.png)

![alt text](./images/VirtualBox_Debian_11.5-34.png)

![alt text](./images/VirtualBox_Debian_11.5-35.png)

![alt text](./images/VirtualBox_Debian_11.5-36.png)

![alt text](./images/VirtualBox_Debian_11.5-37.png)

![alt text](./images/VirtualBox_Debian_11.5-38.png)

![alt text](./images/VirtualBox_Debian_11.5-39.png)

![alt text](./images/VirtualBox_Debian_11.5-40.png)

### LUKS.

![alt text](./images/VirtualBox_Debian_11.5-41.png)

![alt text](./images/VirtualBox_Debian_11.5-42.png)

![alt text](./images/VirtualBox_Debian_11.5-43.png)

![alt text](./images/VirtualBox_Debian_11.5-44.png)

![alt text](./images/VirtualBox_Debian_11.5-45.png)

![alt text](./images/VirtualBox_Debian_11.5-46.png)

![alt text](./images/VirtualBox_Debian_11.5-47.png)

![alt text](./images/VirtualBox_Debian_11.5-48.png)

![alt text](./images/VirtualBox_Debian_11.5-49.png)

![alt text](./images/VirtualBox_Debian_11.5-50.png)

### LVM.

![alt text](./images/VirtualBox_Debian_11.5-51.png)

![alt text](./images/VirtualBox_Debian_11.5-52.png)

![alt text](./images/VirtualBox_Debian_11.5-53.png)

![alt text](./images/VirtualBox_Debian_11.5-54.png)

![alt text](./images/VirtualBox_Debian_11.5-55.png)

![alt text](./images/VirtualBox_Debian_11.5-56.png)

![alt text](./images/VirtualBox_Debian_11.5-57.png)

![alt text](./images/VirtualBox_Debian_11.5-58.png)

![alt text](./images/VirtualBox_Debian_11.5-59.png)

![alt text](./images/VirtualBox_Debian_11.5-60.png)

![alt text](./images/VirtualBox_Debian_11.5-61.png)

![alt text](./images/VirtualBox_Debian_11.5-62.png)

![alt text](./images/VirtualBox_Debian_11.5-63.png)

![alt text](./images/VirtualBox_Debian_11.5-64.png)

![alt text](./images/VirtualBox_Debian_11.5-65.png)

![alt text](./images/VirtualBox_Debian_11.5-66.png)

![alt text](./images/VirtualBox_Debian_11.5-67.png)

![alt text](./images/VirtualBox_Debian_11.5-68.png)

![alt text](./images/VirtualBox_Debian_11.5-69.png)

![alt text](./images/VirtualBox_Debian_11.5-70.png)

![alt text](./images/VirtualBox_Debian_11.5-71.png)

![alt text](./images/VirtualBox_Debian_11.5-72.png)

![alt text](./images/VirtualBox_Debian_11.5-73.png)

![alt text](./images/VirtualBox_Debian_11.5-74.png)

![alt text](./images/VirtualBox_Debian_11.5-75.png)

![alt text](./images/VirtualBox_Debian_11.5-76.png)

![alt text](./images/VirtualBox_Debian_11.5-77.png)

![alt text](./images/VirtualBox_Debian_11.5-78.png)

### Installing the base system. 

![alt text](./images/VirtualBox_Debian_11.5-79.png)

![alt text](./images/VirtualBox_Debian_11.5-80.png)

![alt text](./images/VirtualBox_Debian_11.5-81.png)

![alt text](./images/VirtualBox_Debian_11.5-82.png)

![alt text](./images/VirtualBox_Debian_11.5-83.png)

![alt text](./images/VirtualBox_Debian_11.5-84.png)

![alt text](./images/VirtualBox_Debian_11.5-85.png)

## First boot.

Just boot your new install immediately after finishing the installation process. Don't remove nothing of your system beside the installation DVD or CD if you use them for installation. If you used a USB stick don't remove it, because this can change the layout of the disks in your system.

![alt text](./images/VirtualBox_Debian_11.5-86.png)

![alt text](./images/VirtualBox_Debian_11.5-87.png)

![alt text](./images/VirtualBox_Debian_11.5-88.png)

![alt text](./images/VirtualBox_Debian_11.5-89.png)

If you have already a EFI partition on your system, this setup will use it instead the one you created in the partition process. 

But that can be changed. 

## Issues with GRUB.
### Adding your user to sudo group.

![alt text](./images/VirtualBox_Debian_11.5-91.png)

![alt text](./images/VirtualBox_Debian_11.5-92.png)

![alt text](./images/VirtualBox_Debian_11.5-93.png)

Restart.

### Install GRUB on the EFI partition of the storage device you used.

![alt text](./images/VirtualBox_Debian_11.5-100.png)

![alt text](./images/VirtualBox_Debian_11.5-101.png)

![alt text](./images/VirtualBox_Debian_11.5-102.png)

![alt text](./images/VirtualBox_Debian_11.5-103.png)

![alt text](./images/VirtualBox_Debian_11.5-104.png)

![alt text](./images/VirtualBox_Debian_11.5-105.png)

![alt text](./images/VirtualBox_Debian_11.5-106.png)

![alt text](./images/VirtualBox_Debian_11.5-107.png)

![alt text](./images/VirtualBox_Debian_11.5-108.png)

![alt text](./images/VirtualBox_Debian_11.5-109.png)

![alt text](./images/VirtualBox_Debian_11.5-110.png)

![alt text](./images/VirtualBox_Debian_11.5-111.png)

![alt text](./images/VirtualBox_Debian_11.5-112.png)

![alt text](./images/VirtualBox_Debian_11.5-113.png)

![alt text](./images/VirtualBox_Debian_11.5-114.png)

![alt text](./images/VirtualBox_Debian_11.5-115.png)

![alt text](./images/VirtualBox_Debian_11.5-116.png)

![alt text](./images/VirtualBox_Debian_11.5-117.png)

![alt text](./images/VirtualBox_Debian_11.5-118.png)

![alt text](./images/VirtualBox_Debian_11.5-119.png)

![alt text](./images/VirtualBox_Debian_11.5-120.png)

Restart.

### Install GRUB on the BIOS boot area of the storage device you used. So you can boot this storage device in a system without EFI (optional).
(...)
