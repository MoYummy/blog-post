---
layout:     post
title:      "Change yum mirror on Centos"
date:       2016-01-26 10:47:00+0800
categories: [stuff]
tags:       [centos]
---

Pick a mirror on ```http://mirror-status.centos.org/``` (e.g. ```mirror.vastspace.net```)

Backup
~~~
ls /etc/yum.repos.d/ # CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-fasttrack.repo  CentOS-Media.repo  CentOS-Vault.repo
sudo cp /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak
sudo vi /etc/yum.repos.d/CentOS-Base.repo
~~~

Update via ```vim``` commands
~~~
:%s/^#base/base/g
:%s/^mirror/#mirror/g
:%s/mirror.centos.org/mirror.vastspace.net/g
:wq
~~~
