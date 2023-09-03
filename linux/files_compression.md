# files compression

1. using gzip and gunzip
```commandline
gzip <filename> # deletes <filename> and produces a <filename>.gz 
gunzip <filename>.gz # deletes <filename>.gz and produces a <filename> 
```

2. using bzip2 and bunzip2
```commandline
bzip2 <filename> # deletes <filename> and produces a <filename>.bz2 
bunzip2 <filename>.gz # deletes <filename>.bz2 and produces a <filename> 
```

3. using xz and unxz
```commandline
xz <filename> # deletes <filename> and produces a <filename>.xz
unxz <filename>.gz # deletes <filename>.xz and produces a <filename> 
```

4. if you want to combine many files, use ```tar```.
```commandline
tar cf <archivename>.tar <filename1> <filename2> ... # it produces a <archivename>.tar and keeps other files intact.
tar xf <archivename>.tar # it extracts the files from <archivename>.tar and keeps <archivename>.tar intact.
```
if you want to combine, and also compress files using gzip, use ```-z``` flag or ```-b``` flag for using bzip2 algorithm.
```commandline
tar cfz <archivename>.tar.gz <filename1> <filename2> ... # create file
tar xf <archivename>.tar.gz # extracts files without the need to unzip them first.
```
if you want to append new files to the current tar file, use ```-r``` flag.