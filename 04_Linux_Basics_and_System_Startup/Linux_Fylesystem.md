# Linux Filesystems

- Different types of filesystems supported by Linux
    - Conventional disk filesystems: `ext3, ext4, XFS, Btrfs, JFS, NTFS, vfat, exfat, etc...`
    - Flash storage filesystems: `ubifs, jffs2, yaffs, etc...`
    - Database filesystems
    - Special purpose filesystems: `procfs, sysfs, tmpfs, squashfs, debugfs, fuse, etc...`
    - Case-sensitive

## Partitions and Filesystems

- A partition is a dedicated subsection of physical storage media
- A filesystem is just a method of storing and accessing files.

|                   | WINDOWS                    | LINUX          |
| :---------------------- | :------------------------- | :--------------- |
| Partition             | Disk1 | `/dev/sda1`      |
| Filesystem type               | NTFS/VFAT     | EXT3/EXT4/XFS/BTRFS...        |
| Mounting parameters | DriveLetter              | MountPoint |
| Base folder (Where OS is stored) | `C:\`       | `/`         |


## Filesystem Hierarchy Standard

![alt text](image-3.png)

[_Filesystem Hierarchy Standard_](https://refspecs.linuxfoundation.org/FHS_3.0/fhs-3.0.pdf)

