---
layout: post
title: tomcat 的问题
category: 工具
tags: [server]
keywords: java tomcat
---

#### Error listenerStart 或者 是显示详细的错误

可以在WEB-INF/classes目录下新建一个文件叫logging.properties

    handlers = org.apache.juli.FileHandler, java.util.logging.ConsoleHandler  
      
    ############################################################  
    # Handler specific properties.  
    # Describes specific configuration info for Handlers.  
    ############################################################  
      
    org.apache.juli.FileHandler.level = FINE  
    org.apache.juli.FileHandler.directory = ${catalina.base}/logs  
    org.apache.juli.FileHandler.prefix = error-debug.  
      
    java.util.logging.ConsoleHandler.level = FINE  
    java.util.logging.ConsoleHandler.formatter = java.util.logging.SimpleFormatter  

