### mac idea 配置tomcat
###### 一、下载安装tomcat
> [往期博客](https://www.cnblogs.com/javayanglei/p/12924235.html)

###### 二、有一个 javaWeb项目
1. [新建javaWeb项目](https://www.cnblogs.com/javayanglei/p/12937781.html)
2. [普通java项目转web项目](https://www.cnblogs.com/javayanglei/p/12938798.html)
3. 创建一个javaWeb项目 ,参考第一条，只是在第二步的时候选中java Web就行
###### 三、完善web项目
1. 在WEB-INF 下新建两个文件夹，lib(存放jar包)和classes(存放编译后的文件)![截屏2020-05-22 下午6.26.37](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午6.26.37PEth4B.png)
2. 打开项目结构设置 ![](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午6.31.15Se0Mcl.png)
3. 配置classes文件夹路径![截屏2020-05-22 下午6.47.34](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午6.47.343fngcy.png)
4. 配置lib文件夹路径 ![截屏2020-05-22 下午6.50.32](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午6.50.32J81iKL.png) 
![截屏2020-05-22 下午6.53.57](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午6.53.577zfNft.png)![截屏2020-05-22 下午6.59.13](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午6.59.13DLWaql.png)
###### 四、tomcat项目部署

1. 配置tomcat
![](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.23.14vRLZez.png)

![截屏2020-05-22 下午7.29.05](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.29.05vHAexR.png)

![截屏2020-05-22 下午7.32.05](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.32.05InZIQ7.png)

![截屏2020-05-22 下午7.34.32](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.34.3286zrsF.png)

![截屏2020-05-22 下午7.36.46](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.36.46WRf0Hw.png)

![截屏2020-05-22 下午7.38.14](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.38.14G2nHYR.png)

![截屏2020-05-22 下午7.39.37](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.39.37knAV3T.png)

###### 五、创建servlet

1. 创建![截屏2020-05-22 下午7.42.50](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.42.50QE35D4.png)

![截屏2020-05-22 下午7.45.52](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.45.52VV2Rrl.png)

![截屏2020-05-22 下午7.45.59](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.45.59kUojFD.png)
2. servlet中简单代码
```java
package com.yanglei.servlet;

import java.io.IOException;

/**
 * @author yang
 *
 * WebServlet 注解
 * name 是名字
 * urlPatterns 是访问的路径
 *
 */
@javax.servlet.annotation.WebServlet(name = "helloServlet",urlPatterns = "/day1/hello")
public class HelloServlet extends javax.servlet.http.HttpServlet {
    @Override
    protected void doPost(javax.servlet.http.HttpServletRequest request, javax.servlet.http.HttpServletResponse response) throws javax.servlet.ServletException, IOException {
        System.out.println("hello servlet");
        request.getRequestDispatcher("/index.jsp").forward(request,response);
    }

    @Override
    protected void doGet(javax.servlet.http.HttpServletRequest request, javax.servlet.http.HttpServletResponse response) throws javax.servlet.ServletException, IOException {
        doPost(request, response);
    }
}
```
3. 测试![截屏2020-05-22 下午7.54.26](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-22%20下午7.54.264aBDqn.png)
###### 五、参考
> [波波烤鸭 IntelliJ IDEA2019实现Web项目创建示例](https://www.jb51.net/article/185713.htm)


