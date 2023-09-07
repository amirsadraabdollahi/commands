# Pipe

with pipe (|), you can send output of a command as an input of other command.

1. the ```xargs``` utility reads space, tab, newline, ... delimited strings and execute provided command on all of them.
```commandline
ls | xargs echo # executes echo <filename> for each filename
ls | xargs -I FILENAME echo this is FILENAME file # can define variable of your input
```

2. redirect into file(s) and display on terminal
```commandline
ls | tee file1 file2 ... # redirects ls output to file1 and file2 and also show on terminal
```