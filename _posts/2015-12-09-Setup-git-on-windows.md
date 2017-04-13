---
layout:     post
title:      "Setup git on windows"
date:       2015-12-09 11:08:00+0800
categories: [git]
tags:       [git, github]
---

Download and install ```http://www.git-scm.com/download/win```

Add to ```Path```
~~~
C:\Program Files\Git\cmd;
C:\Program Files\Git\bin;
~~~

Configure global
~~~
git config --global user.name "Mo Yummy"
git config --global user.email "mo.yummy@example.com"
git config --global push.default simple
~~~

Configre ssh key ```C:\Users\moyummy\.ssh\config```
~~~
Host github.com
    HostName github.com
    User Mo-Yummy
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/moyummy

Host git.enterprise.com
    HostName git.enterprise.com
    User Mo-Yummy-Enterprise
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/moyummyenterprise
~~~

Download and install ```http://winmerge.org/downloads/```

Create script ```C:\Program Files\Git\cmd\winmerge.sh```
~~~
#!/bin/sh
echo Launching WinMergeU.exe: $1 $2
"C:\Program Files (x86)\WinMerge\WinMergeU.exe" -e -ub -dl "Base" -dr "Mine" "$1" "$2"
~~~

Configure diff tool
~~~
git config --replace --global diff.tool winmerge
git config --replace --global difftool.winmerge.cmd "winmerge.sh \"$LOCAL\" \"$REMOTE\""
git config --replace --global difftool.prompt false
~~~

Try cloning a git
~~~
cd C:\github
git clone https://github.com/MoYummy/blog-post
git checkout master
~~~

Edit something and try diff
~~~
git difftool
~~~
