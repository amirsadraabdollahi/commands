# files management

1. wildcards
- ```*``` means every string
- ```?``` means any single character
- ```[ABC]``` matches A, B, C
- ```[a-k]``` matches a, b, c, ..., k (both lower-case and capital)
- ```[0-9a-z]``` matches all digits and numbers
- ```[!x]``` means not x

2. get list of current dir files
```commandline
ls # all files
ls * # all files
ls *.txt # files with txt format
ls .. # files of parent dir
ls -ltrh # get <long timeSorted reversed humanReadable> ls of files
ls -R # recursive ls
```

3. copy files or dir
```commandline
cp <path_to_file1> <path_to_file2> ... <destination_path>
cp -r <path_to_folder> <destination_path> # cp recursively
```

4. move and rename file
```commandline
mv <path_to_file1> <destination_path>
```

5. remove files
```commandline
rm <file>
rm -r <dir>
rm -r -i <dir> # remove interactively
```

6. create or update file
```commandline
touch <filename> # it creates a file, if the filename doesn't exists, but if the file exists, it updates the date of the file modification.
touch -d 11am <filename> # change the modification date of the file to specific time.
# use -t to specify the date with another format.
touch -r <filename2> <filename> # use <filename2> as a reference for <filename> modification date.
```

7. make or remove dir
```commandline
mkdir <dirname>
mkdir -p <dirname1>/<dirname2>/<dirname3> # create dirname3 in specified path, and create parent dir if needed.
rmdir <dirname> # just remove empty dir
```

8. knowing file's contents and informations
```commandline
file <filename>
```

9. professional copy using ```dd```
```commandline
man dd :))) # learn how to use it in it's manual.
```

10. finding files
```commandline
find . # find all files in the current directory
find . -name "x" # find files named x
find . -iname "*x*" # find files which have x in their name and ignore case.
find . -size 0b # find empty files
find . -empty # find empty files
find . -exec ... # exec command is executing command on the finded files. read it's manual to learn more.
```



