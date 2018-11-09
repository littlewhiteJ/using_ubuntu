## how to clear the disk in ubuntu

**usually be out of memory in disk**

**there are a few methods to work out that problem**

get the information from the [website](https://www.linuxdashen.com/debianubuntu%E6%B8%85%E7%90%86%E7%A1%AC%E7%9B%98%E7%A9%BA%E9%97%B4%E7%9A%848%E4%B8%AA%E6%8A%80%E5%B7%A7)

1. sth about delete the package

```
sudo apt-get remove <package-name>

sudo apt-get purge <package-name>
```
instruction with **remove** can delete the package but the config_file or other things would not be deleted

so use purge is better... well, i think.

2. clear the .deb package

when your software is installed, the .deb package is of no use...usually

they are in **/var/cache/apt/archives**

use 
```
du -sh /var/cache/apt/archives
```
to find out them

and use 
```
sudo apt-get clean
```
or
```
sudo apt-get autoclean
```
**autoclean** clean the .deb package whose software is deleted now

and **clean** clean all the .deb packages

3. delete the orphan

sometimes when you use **apt-get** some supported packages would be installed at the same time

if your software is deleted, they become orphans

so we should delete them

you can use
```
sudo apt-get autoremove
```
that instruction can only delete the packages installed by **apt-get**

you can use a tool **deborphan**
```
sudo apt-get install deborphan
deborphan
deborphan | xargs sudo apt-get purge -y
```

4. delete the obsolete(out of style) packages

it means the packages cannot be found in **/etc/apt/sources.list**

so we should delete them

use 
```
sudo aptitude search ?obsolete
```
then it would show a list of the obsolete packages

than use 
```
sudo apt-get purge [that package]
```

5. delete the log

we can use tool **ncdu** to list the logs 

```
sudo apt-get install ncdu

sudo ncdu /var/log

```
use 
```
sudo dd if=/dev/null of=/var/log/shadowsocks.log
```
/dev/null is 

emmm...

like a black hole...

6. baobab

here comes a useful tool **baobab**

you can find out which software eat your memory by it **easily**

7. debian-goodies

it is also useful

```
sudo apt-get install debian-goodies
dpigs -H
```

or see more lines

```
dpigs -H --lines=20
```

8. ubuntu-tweak
```
sudo apt-get install gdebi

sudo gdebi ubuntu-tweak*.deb
```

it is wonderful and easy to use



