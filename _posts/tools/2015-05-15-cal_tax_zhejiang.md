---
layout: post
title: 税后工资计算小工具
category: 工具
tags: [python]
keywords: 税后计算， 工具 
description: 用于浙江工资计算
---
## 用于浙江工资计算
```python
#!/usr/bin/python
#-*- coding=utf-8 -*-
import sys

# 浙江个人所得税计算
print "扣除三险一金后实际到手，应实际到手工资:" + str(sys.argv[1])
ori = float(sys.argv[1])

x = ori - 3500
print "用于个人所得税计算时的工资:" + str(x if x > 0 else ori)

res = 0
if x > 0 and x <= 1500 :
    res = x * 0.03
elif x > 1500 and x <=4500:
    res = x * 0.1 - 105
elif x > 4500 and x <=9000:
    res = x * 0.2 - 555
elif x > 9000 and x <=35000:
    res = x * 0.25 - 1005

print "个人所得税:" + str(res)
print "税后工资:" + str(ori - res)
```
