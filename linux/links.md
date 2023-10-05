# Hard Links and Soft Links

1. create link

hard link points to the inode of the file. but soft link points to the exact file, so it has different inode.
get inode of files with ```ls -i```
```commandline
ln myfile hard_link # by default it makes hard link
ln -s myfile soft_link # this create soft link
```

2. remove link

```commandline
unlink hard_link
unlink soft_link
```

3. find links
```commandline
find . -type l # find links in current directory
```

in the discription of the file, if the first character is ```l```, then it is a link.