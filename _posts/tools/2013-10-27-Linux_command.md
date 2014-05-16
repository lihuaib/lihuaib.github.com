---
layout: post
title: Linux 以及 Ubuntu 常用命令 
category: 工具 
tags: [linux]
keywords: linux, ubuntu 
description: 常用命令集合 
---
##ls 自己会忘记的一些常用命令如下

####用户操作

    sudo passwd root #启用root 账户
    sudo passwd -l root #禁用root 账户
    sudo passwd -u root #重新启用root 账户

####SSH操作

    ssh -qTfnN -D 端口 user_name@host_home #firefox addon AutoProxy

####解压和压缩

    unrar x xxx.rar newfolder #解压文件到newfolder文件夹
    unzip apache-tomcat-7.0.50.zip #解压

    tar -zcvf /tmp/etc.tar.gz /etc #压缩 将/etc 目录压缩
    tar xzvf apache-tomcat-7.0.50.tar.gz #解压

    jar cvf foldera.war ./foldera  # war 压缩
    jar xvf foldera.war  # war 解压

####连接有线网络
 
    sudo pppoeconf 

####安装bundle 程序
 
    sudo ./filename.bundle 

####查找包含某个字符串的文件
 
    egrep -ir  "(scan_qr)" ./*  #在当前的目录下遍历查找
 
 ####Linux command get tomcat process id by name

    ps -ef | grep tomcat6 | grep java | awk ' { print $2 } '
    

