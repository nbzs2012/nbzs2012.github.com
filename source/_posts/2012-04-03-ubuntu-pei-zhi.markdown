---
layout: post
title: "Ubuntu 配置"
date: 2012-04-03 20:02
comments: true
categories: 
---
## ubuntu 基本调整

回到传统桌面

	sudo apt-get install gnome-session-fallback

删除ibus, 安装 fcitx 2012.4.3 v4.2.1, 五笔拼音

	sudo apt-get remove ibus
	sudo add-apt-repository ppa:fcitx-team/nightly
	sudo apt-get update
	sudo apt-get install fcitx
	sudo apt-get install fcitx-table-wbpy

****

## 安装 rvm 

参考[这篇文章](http://www.the-tech-tutorial.com/?p=1868)

基本的安装库支持

	sudo apt-get install build-essential git-core curl libmysqlclient16-dev nodejs

安装 rvm 

	sudo bash -s stable < <(curl -s https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer)
	umask g+w
	source /etc/profile.d/rvm.sh
	rvm requirements

根据上面显示的ruby安装步骤

	sudo apt-get install build-essential openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-0 libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev ncurses-dev automake libtool bison subversion

修改所有权

	sudo chown -R [user]:[user] /usr/local/rvm	

安装 ruby 1.9.2 , 并设置为默认 ruby 版本

	ruby install 1.9.2
	source "/usr/local/rvm/scripts/rvm"
	rvm --default use 1.9.2

在 .bashrc 末尾添加, 以便每次打开终端时自动运行 

	source /etc/profile.d/rvm.sh

****

## Sublime Text 2 

参考:

* Sublime 入门文档[Lucifr](http://lucifr.com/139225/sublime-text-2-tricks-and-tips/#package_control)

下载:

* [linux 64 开发版](http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%202%20Build%202190%20x64.tar.bz2) 2012.4.3 v2190

* [linux 64 beta](http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%202%20Build%202181%20x64.tar.bz2) 2012.4.3 v2181

