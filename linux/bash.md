# bash

1. get the type of commands
```commandline
type <command>
type cd
type ls
```

2. go direct to user home
```commandline
cd
cd ~
cd $HOME
```

3. get data from your system
```commandline
uname
uname -a # get all info
```

4. special character ```*```. the star is name of all files in the current dir.
```commandline
echo *
# print file names concatinated with space
```

5. get environment variables
```commandline
env
```

6. which, whereis, whatis
```commandline
which <command>
whereis <command>
whatis <command>
```

7. reload your bash.
```commandline
bash
```
this command actually run another shell on top of the prior one.
with ```ctrl+d``` or ```exit``` you can exit from it.

8. change your prompt
```commandline
PS1=WhateverYouWant
```

9. PATH environment variable use to specify where to find the command binary file.
the content of this env separate with ```:``` . The lower index, the higher priority.

10. run the last command
```commandline
!!
```

11. run the last command that has <word> in it
```commandline
!<word>
!ping
```

12. run the command in x-th place of ```.bash_history``` file
```commandline
!x # x is a number. for example, !31 run 31th command in .bash_history file
```