---
layout: post
title: vim 及 插件 常用命令 
category: 技术技巧 
tags: [vim]
keywords: vim
description: vim 命令备忘 
---
####vim
    
    ctrl+w h j k l  #多窗口时切换
    
    :%!xxd  #查看16进制
    :%!xxd -r  #将16进制文件转回去
    
    zf #在选中文字后进行折叠
    zi #取消所有折叠
    zo #打开当前折叠

####vundle

    BundleInstall(!) #安装(更新)插件
    BundleClean(!) #确认(自动)清理vimrc中没有写明的插件
    BundleList #会显示vimrc里面填写的所有插件名称 

####Bundle "Emmet" Html 编辑工具

    "html:5<c-y>," #插入模式下,生成html结构

    "div#23>ul.123+span.123<c-y>," #结构如下
        <div id="23">
            <ul class="123"></ul>
            <span class="12"></span>
        </div>3   

####Bundle "The-NERD-tree"

    NERDTree #打开目录树
    # 目录树上的操作
    r 刷新
    s 多个文件时,垂直打开文件
    i 多个文件时,水平打开文件

####Firefox的插件 Vimperator

    
