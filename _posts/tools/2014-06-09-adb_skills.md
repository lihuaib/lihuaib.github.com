---
layout: post
title: adb 常见命令
category: 工具 
tags: [android]
---

### 启动一个程序

    # adb shell am start -a android.intent.action.MAIN -c android.intent.category.LAUNCHER -n pgk_name/startc_class
    adb shell am start -a android.intent.action.MAIN -c android.intent.category.LAUNCHER -n com.tudou.android/com.tudou.ui.activity.WelcomeActivity


### adb 截图

    adb shell /system/bin/screencap -p /sdcard/screenshot.png
    adb pull /sdcard/screenshot.png ./screenshot.png
    
    #脚本调用 ./snapshot 1.jpg
    #!/bin/bash
    adb shell /system/bin/screencap -p /sdcard/$1
    adb pull /sdcard/$1 ./$1
    


