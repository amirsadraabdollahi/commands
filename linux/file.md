# file

1. for locating the file or command

```commandline
which <command> # -a flag makes it more informative
whereis <command> # gets more information
type <command> # gets the command type
locate <filename or cammand>
find . -maxdepth 1 -user jadi -group <group-x> # with -user and -group you can specify owner of files to find. 
```

2. for getting the link dynamic dependencies of an executable file
```commandline
ldd <executable filename or command>
```

3. for getting information of a file or command
```commandline
file <filename>
```

4. PATH

the shell search directory in PATH for executing a command.

the ```PATH``` variable is a combination of directories separated with ```:```.

add directory to PATH:
```commandline
export PATH=$PATH:/usr/new/dir
```