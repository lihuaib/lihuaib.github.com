---
layout: post
title: iptables 常用命令
category: 工具 
tags: [linux]
keywords: linux
description: 常用命令集合 
---

### 屏蔽某个ip (接受某个IP 将上面的 DROP 改为 ACCEPT)

    iptables -I INPUT -s 121.41.22.25 -j DROP

    将刚才屏蔽的删除
    sudo iptables -D INPUT -s 122.235.164.218 -j DROP


### 查看 iptables 当前的规则

    sudo iptables -L -n  

