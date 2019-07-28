---
title: Acquire Debian Volatile Memory using LiME
updated: 2018-10-20 10:38
---

This article will walk you through the steps to simply acquire Debian Volatile Memory using Linux Memory Extractor (LiME).

To do so, you need to install the package **lime-forensics-dkms**. DKMS stands for Dynamic Kernel Module Support (DKMS), which means here that our package enables generating a Linux kernel module dedicated to our kernel version.
```
sudo apt install lime-forensics-dkms
```
After that, you can see that a Linux module has been built for our kernel and installed in the directory /lib/modules/4.9.0-8-amd64/updates/dkms/.

<img src="/assets/lime.png" />

The loadable kernel module is **lime.ko**. Now, you can insert the module into the Linux kernel and dump the memory to a file, by typing the following command :
```
sudo insmod /lib/modules/4.9.0-8-amd64/updates/dkms/lime.ko "path=/home/sim4n6/ram.bin format=raw"
```
A file called **ram.bin** is being generated which corresponds to the dump of the volatile memory in a raw file format.

When the file is completely generated, the loaded kernel should be removed from the Linux kernel by executing the following command.
```
sudo rmmod lime
```