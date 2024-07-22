# LFS
## DAY 1
- Get a VM
    - [QEMU](https://www.qemu.org/)
    - Download [arch linux](https://archlinux.org/download/)
        - Install arch linux
            - Setup storage.
                - \`fdisk /dev/sda \` and follow the prompts.
            - Setup pacman mirrors using reflector.
            - \` pacstrap /mnt base linux linux-firmware vim networkmanager ly i3-wm xorg neofetch htop grub \`.
            - enable services networkmanager, ly 
            - fstab, user, passwd, timedatectl, locale-gen
            - grub
                - grub-install /dev/sda
                - grub-mkconfig -o /boot/grub/grub.cfg
