---
layout: post
title: awk 常用命令
category: 工具 
tags: [linux]
keywords: linux
description: 常用命令集合 
---

### 从 pd 文件， 打印每行包含 123456 的行

    awk '$0 ~ /123456/ {print $0}' pd  > tt 

    # 不包含
    awk '$0 !~ /123456/ {print $0}' pd  > tt 

