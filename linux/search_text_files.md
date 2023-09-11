# search text files

1. use grep to match regex for each line
```commandline
grep <regex> <file_or_filename_regex>
grep <regex> * # search regex within all files in the current directory.
cat <file> | grep <regex>
```
#### switches
- -c : just show the count of lines
- -v : reverse the search
- -n : show line numbers
- -l : show only file names which the regex matched within its context
- -i : case insensitive
- -r : recursively search all files in directory

2. egrep is extended grep which has some extra feature in writing regexes.
```commandline
grep -E <regex> <file>
egrep <regex> <file>
```

3. fgrep is fixed grep which doesn't consider input as regex and search for exact string in files
```commandline
fgrep <string> <file>
```

4. use regex in sed with ```-r``` switch