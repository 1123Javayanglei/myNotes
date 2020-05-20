### 在mac环境下配置tomcat
##### 安装brew
```shell
# 安装homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
# 检查是否安装成功
brew
```
##### 安装tomcat
```shell
# 安装tomcat
brew install tomcat
# 检查是否安装成功
catalina 
# 开启tomcat
brew services start tomcat
# 用浏览器打开，如果出现一只猫，说明安装成功
http://localhost:8080/
```
##### idea配置tomcat
