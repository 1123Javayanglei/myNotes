## 解决git clone 卡顿的问题
> 众所周知，国内因为不可描述的原因，git clone 特别卡,今天搞了很久，终于解决了，下面是方法
***
##### 第一步 把github项目迁移到码云
  1. 获取要迁移GitHub项目的 Web Url:在项目首页点击"clone or download",点击复制就有了
  1. 在码云上新建一个项目: 在主页点击"+"，选择"从GitHub导入仓库"，填写"Git 仓库url地址",就是刚复制的
    
***
##### 第二步 本地clone码云仓库
   1. 复制码云仓库的web url地址
   1. 打开终端
   1. 进入想要放置项目的仓库
   1. 拉取
   ```shell script
git clone 码云仓库webUrl地址
```
   1. 输入码云账号的用户名和密码
***
##### 第三步 迁移本地码云仓库到GitHub
  * 移除码云远端 
```shell script
git remote remove origin
```
  * 添加GitHub远端
   ```shell script
git remote add origin GitHub的webRul地址
```
   * 推送到GitHub的master(若有多个分支则多次推送)
   ```shell script
git push -u origin master
``` 
***
> 参考 https://blog.csdn.net/qq598535550/article/details/87870931

   