---
layout: post
title: 网络命令
category: 工具 
tags: [linux]
keywords: linux, network 
description: 常用命令集合 
---

####SSH操作

    ssh -qTfnN -D 端口 user_name@host_home #firefox addon AutoProxy

####连接有线网络
 
    sudo pppoeconf 

#### ftp 命令  -- 输入ftp 进入ftp

    ### for windows_NT
    #login
    open xmg15.host.25.com

    #mput upload folder
    mput /home/jlee/test_foler
        
#### 端口扫描
    nmap -sT 192.168.1.108

#### 端口关闭
    sudo service smbd stop # 关闭是 445/tcp open  microsoft-ds 和 139/tcp open  netbios-ssn
    sudo service vmware stop # 关闭是 902/tcp open  iss-realsecure

