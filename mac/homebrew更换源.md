# homebrew更换源

## 前言


&#8195;&#8195;由于brew默认的源是存放在github上，所以国内访问很慢，所以我们可以选择更换为国内提供的更新源，来提高我们的访问速度
&#8195;&#8195;本文转载自[《更换Homebrew的更新源》](https://musoucrow.github.io/2017/03/29/brew_changing/)

## 替换更新源

> 此处推荐中科大的更新源，以下为替换方法

1. 替换"brew.git"

```
$ cd "$(brew --repo)"
$ git remote set-url origin https://mirrors.ustc.edu.cn/brew.git
```

2. 替换homebrew-core.git

```
$ cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
$ git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
```

3. 替换homebrew-bottles

```
$ echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
$ source ~/.bash_profile
```

4. 应用生效

```
$ brew update
```

## 如果之前折腾过homebrew，导致homebrew有问题的，可以尝试以下方法

1. 诊断Homebrew的问题

```
$ brew doctor
```

2. 重置brew.git设置

```
$ cd "$(brew --repo)"
$ git fetch
$ git reset --hard origin/master
```

3. homebrew-core.git同理

```
$ cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
$ git fetch
$ git reset --hard origin/master
```

4. 应用生效:

```
$ brew update
```

## 重置更新源

> 重置回官方源

1. 重置brew.git

```
$ cd "$(brew --repo)"
$ git remote set-url origin https://github.com/Homebrew/brew.git
```

2. 重置homebrew-core.git:

```
$ cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
$ git remote set-url origin https://github.com/Homebrew/homebrew-core.git
```

3. 应用生效

```
$ brew update
```

## 后记

1. 可以使用"brew upgrade"将现有的软件包更新到最新，这样便能看出速度的变化

```
$ brew upgrade
```

2. 使用"brew cleanup"将旧的软件安装包进行清理

```
$ brew cleanup
```
