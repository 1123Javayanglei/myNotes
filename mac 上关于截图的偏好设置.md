# mac 上关于截图的偏好设置	
## 改变存储的截图类型
```shell
defaults write com.apple.screencapture type jpg(文件类型)
```
## 取消日期
```shell
defaults write com.apple.screencapture "include-date" 0
```
## 设置截图名字
```shell
defaults write com.apple.screencapture name screen(要保存的文件的名字)
```
效果
- screen.png
- screen (2).png
- screen(3).png
## 随机截图名字
#### 作用
每分钟给随机三个字母用来当作文件名
#### 步骤
1. 在终端中输入crontab -e
2. 按 a
3. 粘贴代码
```shell
* * * * * /usr/bin/openssl rand -base64 3 | xargs defaults write com.apple.screencapture name
```
4. 按esc

5. 输入 :wq 用来保存退出

## 最后一步
```shell
killall SystemUIServer
```
## 参考
> [知乎](https://zhuanlan.zhihu.com/p/73725126)
> [博客](https://stefanxo.com/random-screenshot-names-on-mac-os-x/)