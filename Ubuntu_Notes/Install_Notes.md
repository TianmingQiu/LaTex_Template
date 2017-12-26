#Linux Notes
## For 14.04 + Win 7 installation:
From Evernotes;

## Sougou Pinyin Input Tips

## Wireless device cannot be detected on ThinkPad E470
- The reason is the version of **linux kernel** is too low(BE CAREFUL! The linux kernel version is different from ubuntu system version), the original version is 4.4.0. So the most urgent thing is to upgrade the kernel version at least up to **4.14.x.x**
- How to upgrade linux kernel version? See this [guide](http://blog.csdn.net/csdn_duomaomao/article/details/77668946)
```
$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.12.9/linux-headers-4.12.9-041209_4.12.9-041209.201708242344_all.deb

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.12.9/linux-headers-4.12.9-041209-generic_4.12.9-041209.201708242344_amd64.deb

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.12.9/linux-image-4.12.9-041209-generic_4.12.9-041209.201708242344_amd64.deb
```


## Install driver for RLT8812CE
- [Driver Install Guide](https://ubuntuforums.org/showthread.php?t=2371149&page=3)

```
1. Download driver directory from this repo:https://github.com/endlessm/linux/tr...less/rtl8821ce. 
2. You can do it by this link: https://minhaskamal.github.io/DownGi...less/rtl8821ce
3. Unpack zip archive.
4. Change the Makefile. Line "export TopDIR ?= ..." to export "TopDIR ?= PATH TO EXTRACTED DIRECTORY".
$ make
$ sudo make install
$ sudo modprobe -a 8821ce
```
    
- The above link works iff your linux version is right, unless you cannot **make** successfully.


## Upgrade Ubuntu System Version
- From 14.04 LTS to 16.04 LTS: [CSDN Guide](http://blog.csdn.net/chszs/article/details/51236572)
- The above link for the last step, maybe just type:```$ sudo update-manager``` without ```-d```.