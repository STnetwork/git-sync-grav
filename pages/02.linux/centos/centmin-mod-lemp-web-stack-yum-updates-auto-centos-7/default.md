---
title: 'CENTMIN MOD LEMP WEB STACK - YUM Updates Auto - CentOS 7'
date: '21-01-2018 06:41'
process:
    markdown: true
    twig: true
twig_first: true
twitterenable: true
twittercardoptions: summary
articleenabled: false
musiceventenabled: false
orgaenabled: false
orga:
    ratingValue: 2.5
orgaratingenabled: false
eventenabled: false
personenabled: false
musicalbumenabled: false
productenabled: false
product:
    ratingValue: 2.5
restaurantenabled: false
restaurant:
    acceptsReservations: 'yes'
    priceRange: $
facebookenable: true
---

[MINITOC]

<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/linux"><span class="icon is-small"><i class="fa fa-linux"></i></span><span>Linux</span></a></li>
    <li><a href="/linux/centos"></i></span><span>CentOS</span></a></li>
    <li><a href="#"></i></span><span>LEMP WEB STACK - CentminMod - CentOS 7 - YUM Updates Auto</span></a></li>
  </ul>
</nav>

---

* [Introduction](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#introduction)
	* [Prerequisites](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#prerequisites)
	* [Yum Update](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#yum-update)
* [Centmin Mod LEMP Stack Install on CentOS](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#centmin-mod-lemp-stack-install-on-centos)
	* [Edit color bash](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#edit-color-bash)
	* [Add a Domain Name’s Nginx Vhost Configuration](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#add-a-domain-names-nginx-vhost-configuration)
	* [CENTMIN MOD Geting Started Guide](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#centmin-mod-geting-started-guide)
	* [Auto Updating Centmin Mod Code](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#auto-updating-centmin-mod-code)
	* [Auto Yum - Yum Cron](/linux/centos/centmin-mod-lemp-web-stack-yum-updates-auto-centos-7#auto-yum-yum-cron)

----

## Introduction

You will be able to install a LEMP on CentOS 7 by following this article.
[Centmin Mod LEMP](http://centminmod.com/) is a Linux, Nginx, MariaDB MySQL & PHP-FPM web stack for CentOS 6.x & CentOS 7.x with a shell menu based installer. The shell based menu allows Nginx & PHP version management - upgrading or downgrading Nginx & PHP or setting up Nginx vhosts and much more.

Centmin Mod auto installs Nginx server on CentOS Linux with the following:

* Nginx
* PHP-FPM
* MariaDB
* PHP opcode cache : Zend OpCache, APC Cache, Xcache
* Memcached Server + Memcache
* Libmemcached + Memcached PHP Extension
* Multi-threaded compression: pigz, pbzip2, lbzip2, plzip, p7zip (optional)
* CSF Firewall
* Pure-FTPD Virtual FTP User support

Shell Based Menu :

```
--------------------------------------------------------
     Centmin Mod Menu 123.09beta01 centminmod.com
--------------------------------------------------------
1).  Centmin Install
2).  Add Nginx vhost domain
3).  NSD setup domain name DNS
4).  Nginx Upgrade / Downgrade
5).  PHP Upgrade / Downgrade
6).  XCache Re-install
7).  APC Cache Re-install
8).  XCache Install
9).  APC Cache Install
10). Memcached Server Re-install
11). MariaDB MySQL Upgrade & Management
12). Zend OpCache Install/Re-install
13). Install/Reinstall Redis PHP Extension
14). SELinux disable
15). Install/Reinstall ImagicK PHP Extension
16). Change SSHD Port Number
17). Multi-thread compression: pigz,pbzip2,lbzip2...
18). Suhosin PHP Extension install
19). Install FFMPEG and FFMPEG PHP Extension
20). NSD Install/Re-Install
21). Update - Nginx + PHP-FPM + Siege
22). Add Wordpress Nginx vhost + Cache Plugin
23). Update Centmin Mod Code Base
24). Exit
--------------------------------------------------------
Enter option [ 1 - 24 ]
```

### Prerequisites
* VPS or Local Machine on CentOS 6.x & CentOS 7.x
* Connection Internet on the machine
* Some knowledges in Linux


###  Yum Update

It's much better to do `Yum update` before like that we save time.

``` sh
yum -y update && yum -y upgrade
```

----

## Centmin Mod LEMP Stack Install on CentOS

It's a quick curl installer method, it's easy just one line. This line will install automatically the lastest version.

``` bash
yum -y update; curl -O https://centminmod.com/betainstaller.sh && chmod 0700 betainstaller.sh && bash betainstaller.sh
```

### Edit color bash

Personally, I like change the Color Bash, in this case, it will be in green. Edit `.bashrc` in your User folder, then reboot the machine to apply the color.

``` bash
vim .bashrc
export PS1="\e[1;32m[\u@\h \W]\$ \e[m "
```

### Add a Domain Name's Nginx Vhost Configuration

``` apache
cd /usr/local/src/centminmod
./centmin.sh
option #2
```

### CENTMIN MOD Geting Started Guide

``` bash
hostnamectl set-hostname stnetwork.fr
hostnamectl status
nano /etc/hosts
service network restart
```

[CENTMIN MOD Geting Started Guide]: https://centminmod.com/getstarted.html
[CENTMIN MOD Geting Started Guide][]


### Auto Updating Centmin Mod Code

``` bash
mkdir -p /root/tools
nano /root/tools/updatecm.sh
#!/bin/bash
branchname=123.09beta01
cd /usr/local/src/centminmod
git stash
git pull
git log -1
```

``` bash
chmod +x /root/tools/updatecm.sh
15 */3 * * * /root/tools/updatecm.sh 2>/dev/null
```


### Auto Yum - Yum Cron

``` bash
yum -y install yum-cron
chkconfig yum-cron on
systemctl enable yum-cron.service
email_to=your@email.com
```

```
EMAIL=your@email.com
sed -i "s|^email_to = root|email_to = ${EMAIL}|" /etc/yum/yum-cron.conf
sed -i 's|^update_messages = no|update_messages = yes|' /etc/yum/yum-cron.conf
sed -i 's|^download_updates = no|download_updates = yes|' /etc/yum/yum-cron.conf
sed -i 's|^apply_updates = no|apply_updates = yes|' /etc/yum/yum-cron.conf
sed -i 's|^emit_via = stdio|emit_via = email|' /etc/yum/yum-cron.conf

sed -i "s|^email_to = root|email_to = ${EMAIL}|" /etc/yum/yum-cron-hourly.conf
sed -i 's|^update_cmd = default|update_cmd = security|' /etc/yum/yum-cron-hourly.conf
sed -i 's|^update_messages = no|update_messages = yes|' /etc/yum/yum-cron-hourly.conf
sed -i 's|^download_updates = no|download_updates = yes|' /etc/yum/yum-cron-hourly.conf
sed -i 's|^apply_updates = no|apply_updates = yes|' /etc/yum/yum-cron-hourly.conf
sed -i 's|^emit_via = stdio|emit_via = email|' /etc/yum/yum-cron-hourly.conf   

egrep '^email_to|^update_messages|^download_updates|^apply_updates|^emit_via' /etc/yum/yum-cron.conf
egrep '^email_to|^update_cmd|^update_messages|^download_updates|^apply_updates|^emit_via' /etc/yum/yum-cron-hourly.conf
service yum-cron restart
```
