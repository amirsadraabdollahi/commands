# packages

**apt is the enrich version of apt-get**

1. updating the list of packages from the defined sources (in /etc/apt/sources.list)
```commandline
apt update
apt-get update
```
this command just update the list of packages and keep it somewhere in cache.

2. installing package
```commandline
apt install <package-name>
apt-get install <package-name>
```

3. simulating installation process
```commandline
apt install -s <package-name>
```
it just simulates the installation process.

4. download the packages and save it in the cache but not install
```commandline
apt-get install --download-only <package-name>
```

5. download just the package and not the dependencies
```commandline
apt-get download <package-name>
```

6. remove package but not dependencies
```commandline
apt-get remove <package-name>
```

7. remove package and its dependencies
```commandline
apt-get autoremove <package-name>
```

8. search for packages
```commandline
apt-cache search <name>
apt-cache search "<complex name>"
```
also, you can do these commands with apt
```commandline
apt search <name>
apt search "<complex name>"
```

9. upgrade installed packages
```commandline
apt-get upgrade
apt upgrade
```
these commands compare the installed packages with the package list in your local cache that you got from sources using ```apt update``` command. 

10. dpkg command is working with .deb files (the exact file of the packages)
```commandline
dpkg -i <x.deb>
# install
dpkg -I <x.deb>
# info
...
```

11. reconfiguring the package
```commandline
dpkg-reconfigure <package-name>
```

12. information of a package
```commandline
apt info <package-name>
```