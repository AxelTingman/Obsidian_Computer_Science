#Operating_System/Linux/Arch_Linux 

From Learn Linux on YouTube.
## Check internet status and IP
1. Type `ip addr show`.

To check internet connection to a website, type `ping XXX` . Replace XXX withthe address of the website

## Connect to wifi
1. Type `iwctl`. The prompt will become green and show `[iwd]`.
2. Type `device list` to show devices available on the computer. If you see a device on the list you cna connect to wifi.
3. Type `station XXX scan` Replace XXX with the name of the wifi device.
4. `station XXX get-networks`
5. `station XXX connect "YYY"`
6. Type the passphrase.

## Prepare the harddisk without UEFI
1. Type `fdisk -l` to see info about the harddisks available on the computer.
2. Type `fdisk /dev/sda` Replace `/dev/sda` if you want to install on another disk.
3. Type `o`
4. Type `n`
5. Press enter to accept defaults.
6. type `t`
7. Type `8e`
8. Type `a`
9. Type `w`
10. Type `pvcreate --dataalignment 1m /dev/sda1`
11. Type `vgcreate volgroup0 /dev/sda1`
12. Type `lvcreate -L 30GB volgroup0 -n lv_root`
13. Type `lvcreate -l 100%FREE volgroup0 -n lv_home`
14. Type `modprobe dm_mod`
15. Type `vgscan`
16. Type `vgchange -ay`
17. Type `mkfs.ext4 /dev/volgroup0/lv_root`
18. Type `mount /dev/volgroup0/lv_root /mnt`
19. Type `mkfs.ext4 /dev/volgroup0/lv_home`
20. Type `mkdir /mnt/home`
21. Type `mount /dev/volgroup0/lv_home /mnt/home`
22. Type `mnt/etc
23. Tyoe `genfstab -U -p /mnt >> /mnt/etc/fstab
24. Type `cat /mnt/etc/fstab` to check if successful.

## Prepare the harddisk with UEFI

## Install applications and kernel
1. type `pacstrap -i /mnt base`
2. press enter to confirm
3. type `arch-chroot /mnt`
4. type `pacman -S linux linux-headers linux-lts linux-lts-headers`. This line installs both the long term support version of the linux kernel and the bleeding edge version. 

## Installing Grub without UEFI
1. type `pacman -S grub dosfstools os-prober mtools`
2. press enter to confirm
3. type `grub-install --target=i386-pc --recheck /dev/sda`
...