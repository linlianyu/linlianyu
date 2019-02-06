# 修改root密码

1. 重启linux系统主机，在出现引导界面时，按下键盘e键进入内核编辑界面

![](https://ws1.sinaimg.cn/large/006tNbRwgy1fxddf7ig8mj30nw0e8q3o.jpg)

<center>Linux系统引导界面</center>

![](https://ws1.sinaimg.cn/large/006tNbRwgy1fxddiyzpimj30oq0eddhl.jpg)

<center>内核编辑界面</center>

2. 在linux16参数的最后面追加"rd.break"参数,然后按下"Ctrl+X"组合键来运行修改后的内核程序

![](https://ws1.sinaimg.cn/large/006tNbRwgy1fxddp8htw9j30pz0f640q.jpg)

3. 进入到系统的紧急救援模式

![](https://ws2.sinaimg.cn/large/006tNbRwgy1fxddqm5v3qj30qe08tgml.jpg)

<center>Linux系统的紧急救援模式</center>

4. 依次输入以下命令

```
mount -o remount,rw /sysroot
chroot /sysroot
passwd
touch /.autorelabel
exit
reboot
```

![](https://ws2.sinaimg.cn/large/006tNbRwgy1fxddztixofj30l3081js4.jpg)
