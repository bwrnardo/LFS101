# The Boot Process

![The Boot Process](image.png)

## Bios
- Basic Input/Output System
- The first step
- Is stored on a read-only-memory (ROM) chip on the motherboard
- After, the boot process in controlled by the OS

## Boot Loader
- Usually stored on the storage device
- In the boot sector (BIOS/MBR systems) or EFI partition
- Keeps track of the date and time even when the power is off
- most common boot loaders are `GRUB` and `ISOLINUX`
- Responsible for loading the kernel image and the initial RAM disk or filesystem
- Responsible for launching Linux

![alt text](image-1.png)

- The size of the MBR is 512 bytes

## The Initial RAM Disk

- The initramfs filesystem imagem contains programs and binary files that perform all actions nedded to mount the proper root fylesystem

![alt text](image-2.png)

