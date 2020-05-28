### tocmat 提示构件未成功部署
#### 可以运行tomcat的配置文件
###### 构件
- <img src="https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-25%20下午10.02.18G2jUh6.png" alt="截屏2020-05-25下午10.02.18G2jUh6" style="zoom:50%;" />
- ![截屏2020-05-25下午9.55.46gIx84X](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-25%20下午9.55.46gIx84X.png)
###### Facet
- 	![截屏2020-05-25下午9.57.53m8QqGe](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-25%20下午9.57.53m8QqGe.png)
###### 模块
- ![截屏2020-05-25下午9.57.53m8QqGe](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-25%20下午9.57.53m8QqGe.png)
- ![截屏2020-05-25下午9.59.07GgVnHV](https://gitee.com/Java1123yanglei/myPictureNew/raw/master/uPic/截屏2020-05-25%20下午9.59.07GgVnHV.png)

### 找到原因了
```java
@WebServlet(name = "Day004ServletGetAll",urlPatterns = "day04/getAll")
// day04/getAll 应该写为 /day/04/getAll
```