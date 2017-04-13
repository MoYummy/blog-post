---
layout:     post
title:      "Setup Ruby on Centos"
date:       2016-11-29 13:37:00+0800
categories: [ruby]
tags:       [ruby,centos]
---

Install ```RVM```
~~~
sudo -i
yum groupinstall -y development # or yum groupinstall -y 'development tools'
gpg2 --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -L get.rvm.io | bash -s stable
usermod -aG rvm administrator # usermod -aG rvm [user]
~~~

Install ```Ruby```
~~~
rvm install 2.3.1 # rvm install [version]
rvm use 2.3.1
~~~

Check by
~~~
id # uid=502(administrator) gid=502(administrator) groups=502(administrator),5669(rvm)
ruby -v # ruby 2.3.1p112 (2016-04-26 revision 54768) [x86_64-linux]
irb # 2.3.1 :001 > 
~~~
(id number may be different depending on machine)
