---
title: Install the latest Volatility pkg release on a Stable Debian 
updated: 2018-09-09 10:38
---

Suppose you have a forensic machine that runs a Stable version of Debian "Stretch", and you feel you are constrained to an old version of Volatility if you install it from the Debian Stable repository.

Well, there is an alternative. Beside from the **Stable** release repository, Debian disposes of a **Testing** repository dedicated for the next stable release, while the **Unstable** repository contains the packages that have been introduced to the Debian System.

The life cycle of a package propagation in the Debian development workflow is as follows: → experimental → maybe move it to the Unstable repository or Not  → if unstable → testing → stable.

I personally choose a bleeding edge version of Volatility that we can get from the Unstable repository following the next steps :

We configure the Package Manager in a way to tell him, that we want to always install the Stable releases of packages, in order to not to break the stability of the system. So we create a configuration file for apt.
```
sudo nano /etc/apt/apt.conf.d/99defaultrelease
```
We write the following line in 99defaultrelease :
```
APT::Default-Release "stable";
```
Then we define a new repository source, the unstable one :
```
sudo nano /etc/apt/sources.list.d/unstable.list
```
To which we add the following line :
```
deb http://ftp.de.debian.org/debian/ unstable main contrib non-free
```
Now, an update of the package index is necessary :
```
sudo apt-get update
```
You need to check the version of the package Volatility you are using and from which repository :
```
apt-cache policy volatility
```
To proceed to a simulated installation of the latest release version of volatility, use the option -t unstable to target the unstable repository.
```
sudo apt-get -s -t unstable install volatility
```
Finally, just remove the option -s to install the latest volatility properly.
```
sudo apt-get -t unstable install volatility
```

References :
 - https://wiki.debian.org/DebianReleases
 - https://wiki.debian.org/DebianUnstable
 - https://serverfault.com/questions/22414/how-can-i-run-debian-stable-but-install-some-packages-from-testing