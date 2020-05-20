## mac 安装mysql

#### 下载
去官方下下载 [官网](https://dev.mysql.com/downloads/mysql/)

#### 安装
现在之后有一个dmg包，点击安装，一直下一步就行
再设置个密码，没了

#### 配置到zsh
```shelll
echo export PATH=$PATH:/usr/local/mysql/bin >> ~/.zshrc
# 环境变量
echo alias mysqlstart='sudo /usr/local/mysql/support-files/mysql.server start' >> ~/.zshrc
echo  alias mysqlstop='sudo /usr/local/mysql/support-files/mysql.server stop' >> ~/.zshrc
# 启动和关闭的别名
```