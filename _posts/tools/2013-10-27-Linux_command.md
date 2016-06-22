---
layout: post
title: Linux 以及 Ubuntu 常用命令 
category: 工具 
tags: [linux]
keywords: linux
description: 常用命令集合 
---
# ls 自己会忘记的一些常用命令如下

### 用户操作

    sudo passwd root #启用root 账户
    sudo passwd -l root #禁用root 账户
    sudo passwd -u root #重新启用root 账户

### 增加某个用户的组别，原来是 group1 现在要是 group1 group2

    usermod -a -G group2 user

### 解压和压缩

    unrar x xxx.rar newfolder #解压文件到newfolder文件夹
    unzip apache-tomcat-7.0.50.zip #解压

    tar -zcvf /tmp/etc.tar.gz /etc #压缩 将/etc 目录压缩
    tar xzvf apache-tomcat-7.0.50.tar.gz #解压
    unzip -O CP936 xxx.zip   #将windows 的zip 加压 无乱码

    jar cvf foldera.war ./foldera  # war 压缩
    jar xvf foldera.war  # war 解压

### 安装bundle 程序

    sudo ./filename.bundle 

### 查找包含某个字符串的文件
 
    egrep -ir  "(scan_qr)" ./*  #在当前的目录下遍历查找
 
### Linux command get tomcat process id by name

    ps -ef | grep tomcat6 | grep java | awk ' { print $2 } '
    
### 后台运行程序

    ## method 1
    command &

    ## method 2
    nohup command > error.log
    ctrl-z

### diff 两个文件夹

    diff -ruNa f1 f2
    diff -ruNa -x \*.class -x \*.dex -x \*.jar -x \*.apk -x \*.cache android_2_2_0 ../trunk/android/project > diff
    
### 启动画面

    sudo update-alternatives --config default.plymouth
    sudo update-initramfs -u 

### 制作gif


    安装 
    sudo apt-get install imagemagick mplayer gtk-recordmydesktop

    使用 gtk-recordmydesktop 录制并保存文件为 out.ogv

    执行如下命令將 out.ogv 分解成单帧图片 
    mplayer -ao null out.ogv -vo jpeg:outdir=.

    执行如下命令將单帧图片压缩成 gif 图片 
    convert *.jpg out.gif

    执行如下命令將 gif 图片进行压缩 
    convert out.gif -fuzz 10% -layers Optimize optimized.gif
    

### 制作gif

    长宽都放缩为原来的50%
    for jpgfile in `ls` ; do convert $jpgfile -resize %50 new_$jpgfile ; done

### 常用软件的诊断修复

    # 查看firefox 的错误追踪
    strace -o err.txt firefox 

### vpn 连接

    sudo apt-get install pptp-linux
    sudo pptpsetup --create testvpn --server 123.45.67.88 --username kk --password fku --encrypt --start

    pon testvpn <-- VPN的“连接名称"
    poff <-- 断开VPN连接 

### 安装 oracle  

    $ sudo update-alternatives --install /usr/bin/java java /opt/jdk1.8.0_51/bin/java 700  
    $ sudo update-alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_51/bin/javac 700  
    $ sudo update-alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_51/bin/jar 700  

    sudo update-alternatives --config java  

### genymotion

    #regist virtual box
    sudo /etc/init.d/vboxdrv setup

### android studio 查看 shal

    cd ~/.android
    keytool -list -keystore debug.keystore
    密钥  android

### 查看端口进程

    netstat -apn | grep 8080 # 包括进程
    netstat -tln  # 只查看端口

### 跟踪命令的执行

    mac
        dtruss

    ubuntu:
        pstrace        

    定位输出
       command > out.file 2>&1     

    将当前的进程加入 dtruss
        sudo dtruss -fp 2218 // 2218 是进程编号

### Linux 抓包 tcpdump

    tcpdump -p -vv -s 0 -w /sdcard/capture.pcap
