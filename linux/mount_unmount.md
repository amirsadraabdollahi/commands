
# Mount and Unmount

1. mount disks
```commandline
mount <disk> <folder>
mount /dev/sda1 /media/mydisk
```

2. watch mount points
```commandline
mount
```

3. unmount disks
```commandline
umount <folder> # umount /media/mydisk
umount <disk> # umount /dev/sda1
```

4. mount with UUID
```commandline
lsblk -o +UUID # to get UUID of each block
mount UUID=<UUID> /media/mydisk # also you can do this by getting labels of a disk
```

5. use fstab for automatic mounting. in this case you should edit /etc/fstab file. It is like a table that shows what file system should be mounted where during the boot process.