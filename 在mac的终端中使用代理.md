##### 一. 下载和配置ClashX
*  下载 [项目地址](https://github.com/Dreamacro/clash/) 

* 安装 

* 配置 [地址](https://renzhe.cloud/user/tutorial?os=mac&client=clashx)
***

##### 二.找到ClashX的配置文件
* 路径 /Users/用户名/.config/clash/config.yaml
* 查看 config.yaml 文件
* 找到一行 socks-port:7881

***

##### 三. 下载安装proxychains
```shell
# 下载安装
brew install proxychains-ng
# 配置文件所在的位置
/usr/loacl/etc/proxychains.conf
```
##### 四.配置 proxychains
######   1. 关闭[SIP](https://support.apple.com/zh-cn/HT204899)
* mac关机
* 开机后按住 command + r ,一直到看到Apple标志或者旋转的地球后停止
* 选择左上方的 实用工具 > 终端
* 输入 csrutil disable
* 重启
###### 2.重启之后，打开终端
```shell
# 输入命令
csrutil status
# 若显示以下内容，说明关闭成功
System Integrity Protection status: disabled
# 如果需要打开SIP，关机后按com+r重启后再选择实用工具>终端，输入
csrutil enable
```
###### 3.编辑proxychains的配置文件
```shell
# 打开并编辑文件
vim /usr/local/etc/proxychains.conf
# 更改，将结尾的 socks4 127.0.01 9095 改为
socks5 127.0.0.1 7891
```

***
##### 参考
> [国光](https://www.sqlsec.com/2019/12/macos.html#toc-heading-15)
> [少数派](https://sspai.com/post/55066)
