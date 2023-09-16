# file system integrity

1. get free space of a disk. ```du``` is disk usage and ```df``` is disk free.
```commandline
df <disk> -TH # -T is to show Type and -H is for human readable. by default check for all disks if not provided
du <directory> # shows the disk usage in the current directory by default
```

#### switches for du:

- s: summary
- h: human readable (power of 1024)
- H: human readable (power of 1000)
- max-depth <int>: calculates all but show only 2 directories depth

2. check your file system in disk using ```fsck <disk>```
```commandline
ls /sbin/*fsck* # see all fs checks
fsck /dev/sda1 # it will run appropriate filesystem check
```

3. get more info of your disk
```commandline
tune2fs -l /dev/sda1 
```

