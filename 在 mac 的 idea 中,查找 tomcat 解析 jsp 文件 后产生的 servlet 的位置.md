## 在 mac 的 idea 中,查找 tomcat 解析 jsp 文件 后产生的 servlet 的位置

> intelliJ Idea在每次启动Tomcat服务器的时候都会修改CATALINA_BASE

### 查看tomcat的CATALINA_BASE
```shell
catalina
# 输出信息
Using CATALINA_BASE:   /usr/local/Cellar/tomcat/9.0.35/libexec
# 这就是tomcat的CATALINA_BASE
Using CATALINA_HOME:   /usr/local/Cellar/tomcat/9.0.35/libexec
Using CATALINA_TMPDIR: /usr/local/Cellar/tomcat/9.0.35/libexec/temp
Using JRE_HOME:        /usr/local/opt/openjdk
···
```
### 查看idea修改后的CATALINA_BASE
开启tomcat后在服务器信息中找
![text1w9ggrp](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/text1w9ggrp.png)	

### 在访达中查找 /Users/yang/Library/Caches/JetBrains/IntelliJIdea2020.1/tomcat/未命名_javase_26
![var8zgvCym](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/var8zgvCym.png)

