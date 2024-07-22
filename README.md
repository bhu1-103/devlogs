# LFS 
## DAY 1 
- Get a VM
    - [QEMU](https://www.qemu.org/)
        - Install qemu from package manager and setup qcow2 partition.
        - `qemu-img create -f qcow2 image.img 20G`
        - `qemu-system-x86_64 -enable-kvm -cdrom archlinux-2024.07.01-x86_64.iso -boot menu=on -drive file=image.img -m 2G -cpu host -netdev user,id=mynet0 -device e1000,netdev=mynet0`

    - Download [arch linux](https://archlinux.org/download/)
        - Install arch linux
            - Setup storage.
                - `fdisk /dev/sda` and follow the prompts.
            - Setup pacman mirrors using reflector.
            - ` pacstrap /mnt base linux linux-firmware vim networkmanager ly i3-wm xorg neofetch htop grub `.
            - enable services networkmanager, ly 
            - fstab, user, passwd, timedatectl, locale-gen
            - grub
                - grub-install /dev/sda
                - grub-mkconfig -o /boot/grub/grub.cfg

- [Start Reading](https://www.linuxfromscratch.org/lfs/view/stable/prologue/foreword.html)
