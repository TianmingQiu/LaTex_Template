# Linux Notes
## For 14.04 + Win 7 installation:
1. 百度经验：win7+Ubuntu3.04双系统安装方法
2. 分四个分区的时候。第一个主分区“/”要最后做，否则会显示不可用。第四个分区给第一个分区预留下空间大小即可。 （**分区的时候给\boot多分一点，至少800M**,/root要足够大，70G+，/home都可以不要挂出来，/boot在双系统的情况下要单独挂载，ubuntu默认是放在/root下的）
3. 装完之后改一下root密码，并修改启动项顺序
4. 所需的ultraISO和镜像均在移动硬盘里
5. [Other Tips](http://blog.csdn.net/fuchaosz/article/details/51882935)  

## Ubuntu重装笔记(双系统卸载ubuntu)
### Method1
拿优盘做成启动盘之后直接擦分区，“-”去挂载，重新分配
### Method2
1. 更改win7的引导，因为安装的时候使用Ubuntu引导windows，如果直接擦除Ubuntu，会无法进入win  
具体更改方法如下：通过管理员身份，运行cmd。 访问mbrfix(可以直接把可执行文件放在user根目录下)  
执行：MbrFix /drive 0 fixmbr /win7 /yes  
然后重启试试，看看是不是跳过了ubuntu直接引导win7  
2. 使用分区工具，擦除原有ubuntu，不需要分配盘符，显示空闲即可，可以调整原win7的D盘，来给Ubuntu扩容  
3. 回到安装步骤  

## Sougou Pinyin Input Tips
Ubuntu搜狗输入法安装方法：
1. 直接在软件中心安装.deb 
2. 更改输入法为fcitx为全局 [Guide](http://blog.csdn.net/tao_627/article/details/24119037)
3. ficitx configuration 添加，去掉only show current language [Guide](http://jingyan.baidu.com/article/54b6b9c0eedd252d583b4714.html)

## 添加德语输入：
- 在搜狗输入法的配置中，找到fictix设置，添加英语（with AltGr dead key）

## Wireless device cannot be detected on ThinkPad E470
- The reason is the version of **linux kernel** is too low(BE CAREFUL! The linux kernel version is different from ubuntu system version), the original version is 4.4.0. So the most urgent thing is to upgrade the kernel version at least up to **4.14.x.x**
- How to upgrade linux kernel version? See this [guide](http://blog.csdn.net/csdn_duomaomao/article/details/77668946)
- **ATTENTION!** amd64 means for 64bit, actually, go to this link and download the latest kernel version: [link](http://kernel.ubuntu.com/~kernel-ppa/mainline/drm-intel-next/)

```
$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/drm-intel-next/2018-04-14/linux-headers-4.16.0-997_4.16.0-997.201804132201_all.deb

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/drm-intel-next/2018-04-14/linux-headers-4.16.0-997-generic_4.16.0-997.201804132201_amd64.deb

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/drm-intel-next/2018-04-14/linux-image-4.16.0-997-generic_4.16.0-997.201804132201_amd64.deb
```
1. 去官网ubuntu linux kernel直接点击下载，amd64位
2. dpkg安装
3. 然后下载网卡驱动

## Install driver for RLT8812CE
- [Driver Install Guide](https://ubuntuforums.org/showthread.php?t=2371149&page=3)

```
1. Download driver directory from this repo:https://github.com/endlessm/linux/tr...less/rtl8821ce. 
2. You can do it by this link: https://minhaskamal.github.io/DownGi...less/rtl8821ce
3. Unpack zip archive.
4. Change the Makefile. Line "export TopDIR ?= ..." to export "TopDIR ?= PATH TO EXTRACTED DIRECTORY". (without $, maybe try this DIR: /lib/modules/4.16.0-997-generic/kernel/net/wireless/)
$ make
$ sudo make install
$ sudo modprobe -a 8821ce
```

- The above link works iff your linux version is right, unless you cannot **make** successfully.

## 优盘空间变小
- [百度经验](https://jingyan.baidu.com/article/b24f6c82dddece86bee5da67.html)


## Upgrade Ubuntu System Version
- From 14.04 LTS to 16.04 LTS: [CSDN Guide](http://blog.csdn.net/chszs/article/details/51236572)
- The above link for the last step, maybe just type:```$ sudo update-manager``` without ```-d```.

## [Ubuntu VPN](https://www.cnblogs.com/LinkT/p/6087634.html)
```
$ sudo apt-get install network-manager-openconnect-gnome
```
## [GRUB time](https://www.jianshu.com/p/f3c3beb7f205)

## alt-tab 2 windows switchers

## [Ubuntu_NVIDIA](https://blog.csdn.net/u012759136/article/details/53355781)
confirmed that in GCP, Michael's instruction fixed the issue.
Here is the commands I used:
```
sudo apt-get purge nvidia*
sudo add-apt-repository ppa:graphics-drivers
sudo apt-get update
sudo apt-get install nvidia-390

sudo reboot
```

…after reboot:
```
lsmod | grep nvidia 
```


https://devtalk.nvidia.com/default/topic/1000340/cuda-setup-and-installation/-quot-nvidia-smi-has-failed-because-it-couldn-t-communicate-with-the-nvidia-driver-quot-ubuntu-16-04/3


https://blog.csdn.net/u012759136/article/details/53355781

## bashrc 修改，取消注释`force_color_prompt=yes`
