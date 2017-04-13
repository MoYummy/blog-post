---
layout:     post
title:      "Setup docker on Centos"
date:       2017-02-04 16:30:00+0800
categories: [docker]
tags:       [docker,centos]
---

~~~
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://docs.docker.com/engine/installation/linux/repo_files/centos/docker.repo
sudo yum makecache fast
sudo yum -y install docker-engine
sudo service docker start
sudo chkconfig docker on
cut -d: -f1 /etc/group|grep docker
sudo usermod -a -G docker [user]
sudo reboot -f
~~~

Then try pulling an image like

~~~
docker pull jenkins
~~~
