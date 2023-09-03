# Redirecting Streams

stream is a sequence of bytes.

streams are divided into 3types:
0. _stdin_: input stream, which provides input for commands.
1. _stdout_: output stream, which displays output from commands.
2. _stderr_: error stream, which displays error output from commands.

_**the corresponding code to these streams are 0, 1, 2.**_

1. redirect STDOUT to a file.
```commandline
ls > file.txt # if the file exists, it overwrites it's content.
ls >> file.txt # append standard output to the end of the file.txt.
```

2. redirect STDERR to a file.
```commandline
ls x* 2> file.txt # if the file exists, it overwrites it's content.
ls x* 2>> file.txt # append standard error to the end of the file.txt.
```

3. concat redirections
```commandline
ls x* j* > stdout.txt 2> stderr.txt # it sends the ```ls x* j*``` standard errors to the stderr.txt and standards outputs to the stdout.txt. overwrites if exists.
ls x* j* >> stdout.txt 2>> stderr.txt # it sends the ```ls x* j*``` standard errors to the stderr.txt and standards outputs to the stdout.txt. appends if exists.
```

4. redirect both STDERR and STDOUT to a file.
```commandline
ls x* j* &> std.txt # overwrites if exists
ls x* j* &>> std.txt # appends if exists.
```

5. redirect STDIN from a file.
```commandline
command < file.txt # get file.txt content as an input to the command.
command <> file.txt # get file.txt content as an input to the command and write the output of command to it (file.txt).
```

6. it also possible to use ```&0```, ```&1``` and ```&2``` to refer to the target of STDIN, STDOUT and STDERR.
in this case ```ls > file1 2>&1``` means redirect standard output to file1 and standard error to same place as stdout which is file1 in our case.

7. sending to null
In linux, /dev/null works like an abyss. you can send anything there, and it will be disappeared without being any burden on your system.
```commandline
ls j* x* > file1 2>/dev/null
```

8. it is good to know about here-documents.
help: it uses ```<<``` for its purpose. search to learn more about it.