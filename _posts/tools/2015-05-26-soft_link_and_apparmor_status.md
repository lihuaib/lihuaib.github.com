---
layout: post
title: mysql soft link and apparmor_status
category: 工具
tags: [linux]
keywords: mysql soft link apparmor_status
---
## 问题
> 当对 mysql 的db 建立 soft link的时候, 读取数据总是 permission deny, 即使用户都是mysql

```bash
cd /var/lib/mysql
mv dbname /home/yourame/dbname
ln -sf /home/yourname/dbname dbname
```

## 解决
> 问题是AppArmor 造成的
参考[这篇文章解决方案](http://serverfault.com/questions/404007/symbolic-link-to-mysql-database)

```bash
sudo vim /etc/apparmor.d/usr.sbin.mysqld
# add two lines
/home/yourname/ r,
/home/yourname/** rwk,
udo apparmor_parser -r /etc/apparmor.d/usr.sbin.mysqld
```
