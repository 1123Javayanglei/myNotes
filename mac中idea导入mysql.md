## Mac中idea导入Mysql

##### 第一步 
从[Mysql](https://dev.mysql.com/downloads/connector/j/)下载zip包，解压后得到jar文件

##### 第二步
在项目的目录下建立一个lib目录，用来放jar文件
<img src="https://gitee.com/Java1123yanglei/myImages/raw/master/uPic/截屏2020-05-15%20下午10.33.50fNq4rU.png" alt="目录结构" style="zoom:50%;" />

##### 第三步
添加到path
文件 -> 项目结构(cmd+;) -> 模块 -> 项目名称 -> 依赖 -> 添加(加号) -> 选择jars或目录 -> 选择 lib下的jar文件 -> 应用 -> 确定
![示意图](https://img-blog.csdnimg.cn/20191206110900598.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1lhbmdsZWlfMQ==,size_16,color_FFFFFF,t_70)