---
layout: post
title: apk 签名 
category: 技术技巧 
tags: [android]
keywords: apk 签名
---

####Apk在Ubuntui(Linux)下的签名

    假设当前拿到手的apk的名称为 ccpal_unsigned.apk

#####Step 1. 生成 keystore 

    # 你可以替换
    # 1. demo.keystore  ==> yourname.keystore
    # 2. demo  ==> android.keystore to your alias name
    # 注: keytool 是在$JAVA_HOME\bin 下
    #       20000 为有效期 20天
    keytool -genkey -v -keystore demo.keystore -alias demo -keyalg RSA -validity 20000
    # 或 
    keytool -genkey -alias demo -keyalg RSA -validity 4000000 -keystore demo.keystore


#####Step 2. 生成 apk 

    /*
        说明：
        -verbose 输出签名的详细信息
        -keystore  demo.keystore 密钥库位置
        -signedjar demor_signed.apk demo.apk demo.keystore 
            a. 签名后产生的文件demo_signed，
            b. 要签名的文件demo.apk
            c. 密钥库demo.keystore 的别名.
    */
    jarsigner -verbose -keystore demo.keystore -signedjar ccpal_signed.apk ccpal_unsigned.apk demo
    
#####Step 3. 简单优化签名后的资源文件 

    # 对齐资源文件
    zipalign -v 4 ccpal_signed.apk ccpal_final.apk
    # 检验是否对齐
    zipalign -c -v 4 ccppal_final.apk
 

###问题
>如果出现 jarsigner: unable to sign jar: java.util.zip.ZipException: invalid entry compressed size 这样的错误
>>那么 导出 apk 的时候, 选择 Android Tools -> Export UnSigned Appication Package. 
