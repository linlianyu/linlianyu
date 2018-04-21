# mac的隐藏小技巧

## 前言

mac的终端是拥有很强大的功能，本文就来说几个终端的使用小技巧

1. 遇到不会读的生词(单词、中文皆可)，可以使用"say 单词"

```
$ say hello
```

2. Finder卡死了，可以使用"killall Finder"

```
$ killall Finder
```

3. 下载大文件时，想要关闭电脑的屏幕，但不希望电脑休眠，可以使用下面的命令

```
$ pmset displaysleep 时间
```

4. 修改LaunchPad的布局

- 调整行数

```
$ defaults write com.apple.dock springboard-rows -int 7
```

- 调整列数

```
$ defaults write com.apple.dock springboard-columns -int 7
```

- 重启LaunchPad

```
$ defaults write com.apple,dock ResetLaunchPad -bool TRUE;killall Dock
```

5. mac硬盘文件变灰色图标

```
$ xattr -l 文件
$ xattr -d com.apple.FinderInfo 文件
```
