---
layout: post
title: Apache常用配置 
category: 工具 
tags: [apache]
keywords: apache
---

## 配置用户名和密码登陆， 并且采用系统用户   

    step1: aptitude -y install libapache2-mod-authnz-external pwauth

    step2: vi /etc/apache2/sites-available/test.conf

        AddExternalAuth pwauth /usr/sbin/pwauth
        SetExternalAuthMethod pwauth pipe
        <Directory /var/www/html/auth-pam>
            #SSLRequireSSL
            AuthType Basic
            AuthName "PAM Authentication"
            AuthBasicProvider external
            AuthExternal pwauth
            require valid-user
        </Directory>

    step3: mkdir /var/www/html/test

    step4: a2ensite auth-pam

    step5: /etc/init.d/apache2 restart
