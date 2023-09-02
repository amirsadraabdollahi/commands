# String Stream
stream is a sequence of bytes.

streams are divided into 3types:
1. stdin: input stream, which provides input for commands.
2. stdout: output stream, which displays output from commands.
3. stderr: error stream, which displays error output from commands.
---
1. display file contents
```commandline
cat <file1> <file2> ...
```
```commandline
zcat <file.txt.gz>
xzcat <file.txt.xz>
bzcat <file.txt.bz>
gzcat <file.txt.gz>
```
these commands use to display files, which are zip in specific format.

2. paginating content of a file
```commandline
less <file.txt>
```

3. octal dump content of a file 
```commandline
od <file.txt>
od -c <file.txt> # interpret each group of bit
od -a <file.txt> # interpret each group of bit like -c but in different format
```

4. file splitting into some chunks
```commandline
split -l 2 <file.txt> # 2lines 2lines splitting
split -n 2 <file.txt> # split file into 2file
split -b 10 <file.txt> # split file into 10bytes chunks
...
```
it produces some files, which you can specify its name format by providing some flags.

5. get head and tail of a file.
```commandline
head <file.txt>
tail <file.txt>
# by default it provides us with 10lines.
# use -f flag for follow the file content. live streaming
```

6. split file into columns
```commandline
cut -f2 -d, <file.txt> # give second field with comma delimiter for each line. 
```

7. show text with line number
```commandline
cat -n <file.txt>
nl <file.txt>
```

8. sort your file based on first character (or number or other things) of each line.
```commandline
sort <file.txt> # it has many useful flags
```

9. get uniq lines of a file. remember that ```uniq``` command just work on sorted files.
```commandline
uniq <file.txt>
uniq -c <file.txt> # show the repeated times of each line
```

10. combine files line by line. de facto, it concat xth line of all files.
```commandline
paste <file1.txt> <file2.txt>
```

11. change your file based on complicated expressions.
```commandline
sed 's/AB/CD/' <file.txt> # it change every first AB with CD in each line.
sed 's/AB/CD/g' <file.txt> # it change every AB with CD in each line. g means global.
```

12. words count of a file.
```commandline
wc <file.txt> # newlines words bytes( or characters) filename
wc -l <file.txt> # just count of newlines.
```

13. using of ```-``` in pipes.
```commandline
pipe1 | command - command
# dash is the output of pipe1 as a file
```

14. get hash of a file.
```commandline
md5sum <file.txt>
sha256sum <file.txt>
sha512sum <file.txt>
```