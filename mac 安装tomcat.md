###  mac 安装tomcat
##### 1 安装brew
> [官网](https://brew.sh/index_zh-cn)
```shell
# 需要科学上网
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
# 若没有科学上网，执行下面👇
git clone git://mirrors.ustc.edu.cn/homebrew-core.git//usr/local/Homebrew/Library/Taps/homebrew/homebrew-core --depth=1
git clone git://mirrors.ustc.edu.cn/homebrew-cask.git//usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask --depth=1
# 替换为国内源
cd "$(brew --repo)"
git remote set-url origin https://mirrors.ustc.edu.cn/brew.git
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-cask"
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-cask.git
# 切换为官方源
# 重置brew.git:
cd "$(brew --repo)"
git remote set-url origin https://github.com/Homebrew/brew.git
# 重置homebrew-core.git:
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://github.com/Homebrew/homebrew-core.git
```
#####  2安装tomcat
```shell
# 安装
brew install tomcat
# 检查是否安装成功
catalina -h
# 运行tomcat：
catalina run
# 或者
brew services start tomcat
# 重启tomcat
brew services restart tomcat
```