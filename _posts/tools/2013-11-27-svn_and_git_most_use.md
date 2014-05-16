---
layout: post
title: svn 和 git 常用命令 
category: 工具
tags: [项目管理]
keywords: svn,git 
description: svn 和 git 在项目中常用的命令
---

####设置不用输入密码

    ~/.subversion/config 
        修改 # store-passwords = no
          为 store-passwords = yes

####比较两个版本: 比如 602 和 712(最新)

    svn diff -r602:712 或者 svn diff -r602:HEAD(最新)
     

####在服务器上建一个tag或者branch

    svn cp -m 'msg.' svn+ssh://serverpath1  svn+ssh://serverpath2
    

####从服务器下载svn/git代码 checkout/clone

    svn co svn+ssh://serverpath1 localfolder
    git clone path localfolder 
    ## 或者
    git pull https://github.com/lihuaib/pseudocrypt.git

####提交代码

    svn ci -m 'this is msg' 
    git commit -m 'this is msg' # 提交到本地
    ## git 提交到服务器
    git push https://github.com/lihuaib/pseudocrypt.git master

####回滚

    svn merge -r712:602 [filename] #然后需要提交 
    git reset –hard commit versionname

####查看当前svn/git目录信息

    svn info

####将work copy出的版本合并到原来的版本上

    # 将 a 的代码 merge 到 b 中
    svn merge branches_name@version branches_name .

