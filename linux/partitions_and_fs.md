# partitions and filesystems

1. get disks
```commandline
lsblk
ls -l /dev/ | grep "^b" # blocks started with b
```

2. editing partition tables

### fdisk
this is for bios systems
```commandline
fdisk -l /dev/sdb # shows all partitions
fdisk /dev/sda # goes to interaction shell. type m for help.
```
for uefi systems use ```gdisk``` instead.

### parted
parted is a GNU tool to edit partitions. its main advantages is to resize defined partitions.
```gparted``` is a graphical tool for managing your disk and partitions.

### partition formatting
format your partitions using ```mkfs``` (and ```mkswap``` for swap).
```commandline
mkfs -t ext3 /dev/sda1
```
see ```ls /sbin/mkfs*``` for different types of fs.