# Mac配置selenium3.md

---

## 前记

&#8195;&#8195;本文借鉴自[Mac 下配置 Python3 和 Selenium3 环境](https://blog.csdn.net/yilovexing/article/details/80701580)

---

1. 下载浏览器驱动包[（下载链接）](https://github.com/mozilla/geckodriver/releases/tag/v0.24.0)

2. 将下载的文件解压,然后移动至/usr/bin目录下

```
linlianyus-MacBook-Air:~ linlianyu$ sudo cp /Users/linlianyu/Downloads/geckodriver/usr/bin/

ps:当你拷贝如果报一个错 Operation not permitted（不允许操作），这是因为 Mac 系统启用了SIP（System Integerity Protection），导致root用户也没有修改权限。

我们可以屏蔽掉这个功能，具体做法是：

1.重启电脑

2.command + R 进入recover模式

3.点击最上方菜单使用工具，选择终端

4.运行命令csrutil disable

5.当出现successfully字样，代表关闭成功！
```

3. 配置环境变量

```
vim ~/.bash_profile
```

```
export PATH=$HOME/bin/:$PATH
```

![](https://ws2.sinaimg.cn/large/006tKfTcgy1g0gqex74o3j30fv0cn753.jpg)

```
linlianyus-MacBook-Air:~ linlianyu$ source ~/.bash_profile
```

#
