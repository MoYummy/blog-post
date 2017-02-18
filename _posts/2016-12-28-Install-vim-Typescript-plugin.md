---
layout:     post
title:      "Install vim Typescript plugin"
date:       2016-12-28 01:29:00+0800
categories: [stuff]
tags:       [vim, typescript]
---
* Download `vim-plug`

~~~
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
~~~

* Download `typescript-vim plugin`

~~~
git clone https://github.com/leafgarland/typescript-vim.git ~/.vim/bundle/typescript-vim
~~~

* Add config of `typescript-vim` in `~/.vimrc`

~~~
call plug#begin('~/.vim/plugged')
Plug 'leafgarland/typescript-vim'
call plug#end()
~~~

* Open `vim` and enter `:PlugInstall`