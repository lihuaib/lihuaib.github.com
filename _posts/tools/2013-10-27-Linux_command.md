---
layout: post
title: Linux 以及 Ubuntu 常用命令 
category: 技术技巧 
tags: [linux]
keywords: linux, ubuntu 
description: 常用命令集合 
---
##ls 自己会忘记的一些常用命令如下

####用户操作

    sudo passwd root #启用root 账户
    sudo passwd -l root #禁用root 账户
    sudo passwd -u root #重新启用root 账户
    
    sudo adduser [username] #创建新用户
    sudo passwd [username] #为新用户创建密码
    userdel [username] #delete user

####SSH操作

    ssh -qTfnN -D 端口 user_name@host_home #firefox addon AutoProxy

####解压和压缩

    unrar x xxx.rar newfolder #解压文件到newfolder文件夹


####连接有线网络
   
    sudo pppoeconf 
