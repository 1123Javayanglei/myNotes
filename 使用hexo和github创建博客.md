## 在mac上使用hexo和github创建博客
### 配置hexo
* 前提 安装node.js 和 git
```shell
# 安装node和git
brew install node git
# 安装完成之后测试，查看版本
node -v
npm -v  
git --version
```
* 安装hexo
```shell
	# 下载安装
	npm instll -g hexo-cli
	# 查看版本
	hexo -v
```
* 配置hexo
```shell
# 创建一个目录，放博客文件
mkdir blog
# cd 到 blog目录
cd blog
# 初始化目录
hexo init
# 补全文件
npm install
```
* 测试hexo
```shell
# 生成静态网页
heox g
# 本地预览,关闭用control+c 
hexo s
# 打开浏览器 输入 localist:4000/ 查看博客
```
***
### 二、关联github
* [登陆github账号](https://github.com/)
* 点击右上角头像旁边的 + 号，选择 New repositroy
* 填写表单
	* “Repository name” 填 你的账户名.github.io
	* “Description” 项目描述，随便写
	* “public or private” 公开还是私有随便选
	* “README” 也勾选上 	
* 关联GitHub和本地hexo博客
	* 打开gihub，点击头像，点击settings
	* 点击 SSH and GPG keys，点击 New SSH key
	* title 随便写，停留在key
```shello
# 本地生成ssh key
ssh-keygen -t rsa -C "随便输入点啥"
# 查看ssh key, 把此时的输出内容放在 key 那边
cat ~/.ssh/id_rsa.pub
# 测试，如果出现你的用户名，则是成功了
ssh -T git@github.com
# 打开博客根目录下的_config.yml 文件
vim _config.yml
# 修改最后一行的配置，把 repo后的网址改为你的github项目的地址
deploy:
type: git
repo: git@github.com:1123Javayanglei/1123Javayanglei.github.io.git
branch: master
```
***
### 三、写文章、发布文章
```shell
# 写文章
hexo n "标题"
# 会在 bolg/sourse/_posts 下生成一个 "标题".md 的文件，写他
# 生成静态网页
hexo g
# 发布到git ，输入 用户名.github.io 就可以访问了
hexo d
```
***
### 四、参考
> [知乎](https://zhuanlan.zhihu.com/p/35668237)
> [hexo官网](https://zhuanlan.zhihu.com/p/35668237)
