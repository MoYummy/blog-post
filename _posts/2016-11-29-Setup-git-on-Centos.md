---
layout:     post
title:      "Setup git on Centos"
date:       2016-11-29 14:00:00+0800
categories: [git]
tags:       [centos,git]
---

Install ```git```
~~~
sudo -i
yum install git
~~~

Create ssh key
~~~
cd ~
mkdir .ssh
chmod 700 .ssh
cd .ssh
ssh-keygen # enter, enter, enter
mv id_rsa moyummygit
mv id_rsa.pub moyummygit.pub
cat moyummygit.pub # "ssh-rsa [blahblahblah]== [blahblah]"
~~~

Create or edit ```~/.ssh/config```
~~~
Host github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/moyummygit
~~~

Add ssh key to your github account through ```https://github.com/settings/keys```

Try cloning a git through protocol
~~~
git clone git@github.com:MoYummy/Ruby.git
~~~

Try ```ssh -vT git@github.com``` for trouble shooting
