---
layout: post
title: svn 和 git 常用命令 
category: 技术技巧 
tags: [项目管理]
keywords: svn,git 
description: svn 和 git 在项目中常用的命令
---
####比较两个版本: 比如 602 和 712(最新)

    svn diff -r602:712 或者 svn diff -r602:HEAD(最新)
     

####在服务器上建一个tag或者branch

    svn cp -m 'msg.' svn+ssh://serverpath1  svn+ssh://serverpath2
    

####从服务器下载svn/git代码 checkout/clone

    svn co svn+ssh://serverpath1 localfolder
    git clone path localfolder 

####提交代码

    svn ci -m 'this is msg' 
    git commit -m 'this is msg' 

####回滚

    svn merge -r712:602 [filename] #然后需要提交 
    git reset –hard commit versionname

####查看当前svn/git目录信息

    svn info

