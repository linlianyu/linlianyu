# Mac上装python的pip安装包时，显示-bash: pip: command not found

## 问题原因

- 这个错误是表示还未安装 pip,因为 Mac 上的 python 是不自带 pip 的,需要自己手动安装

## 方法

```
curl 'https://bootstrap.pypa.io/get-pip.py' > get-pip.py
sudo python get-pip.py
sudo easy_install pip
```
