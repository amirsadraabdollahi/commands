# Manage file permissions and ownership

1. users and group
```commandline
whoami # get current user
groups # get joined groups for current groups
id # ids for current user
```
when creating a user, in some distribution of linux, it is added to a group with the same name.

you can also find users in ```etc/passwd``` with some corresponding information and ```etc/group``` for groups.

2. permissions follow below format:
from first to last:

- ```d``` for directory, ```-``` for file
- next three for owner user: ```rxw``` or ```-``` instead of each
- next three for group: ```rxw``` or ```-``` instead of each
- next three for other: ```rxw``` or ```-``` instead of each

3. change permissions for files 
```commandline
chmod <3digits> <filename>
chmod 775 script.sh
chmod u+rwx,g+rwx,o+rx <filename> # get permissions. u stand for user(owner), g for group and o for others.
chmod g-w,o-x <filename> # take permissions
```
```-R``` flag for recursively set permission for files in a directory.
- 1: x
- 2: w
- 4: r

so when you want to set a group of permission with the respective access, you can some those codes for each.
for example rwx=7, rw-=6, -wx=3, ---=0, ...

first digit is for the owner, second for the group and third for others.

4. change owner of files
```commandline
chown user:group <filename>
```
```-R``` flag for recursively change owner of files in a directory.

5. add user to group
```commandline
usermod -aG sudo jadi # add user jadi to group sudo
```
since a user can have many groups, they can change their default group to a specific one with ```newgrp``` command.
```commandline
newgrp <groupname> 
```

6. other permissions

if you set ```s``` instead of ```x``` in permissions, whenever a user runs the file, it assumes that root user runs the file.
```commandline
chmod u+s <filename>
chmod g+s <filename>
```

the ```t``` permission is sticky. it means that no one can delete the file except its owner.
```commandline
chmod +t <filename>
```

7. permissions for new files
there is a concept that can use for setting default permission for new created files. it named ```umask```.
for set this, use ```umask <value>``` command.

```666-umask=default_permission```
