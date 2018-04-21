# 自己搭建ssr服务器教程

## 前记

&#8195;&#8195;本文借鉴自[《自建ss服务器教程》](https://github.com/Alvin9999/new-pac/wiki/%E8%87%AA%E5%BB%BAss%E6%9C%8D%E5%8A%A1%E5%99%A8%E6%95%99%E7%A8%8B)

1. 购买vps服务器

- vps服务器必须选择国外的，香港的也可以

- 国际知名的vps服务器提供商vultr，按小时收费，不怕被封ip

- 服务器系统选择centos 6

2. 购买完服务器后，使用ssh连接服务器

- window使用软件"Xshell"来连接

- mac和linux可以使用命令"ssh root@ip address"

```
linlianyus-MacBook-Air:~ linlianyu$ ssh root@ip address
```

3. 部署ssr脚本

- 在服务器中输入下面的命令

```
[root@localhost linlianyu]# yum -y install wget
[root@localhost linlianyu]# wget -N --no-check-certificate https://softs.fun/Bash/ssr.sh && chmod +x ssr.sh
```

4. 安装ssr服务端

- 输入"bash ssr.sh"

```
[root@qyi-5ad41ca79caad ~]# bash ssr.sh
```

- 输入数字1安装ssr

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqguczxpgrj30dm0btq6m.jpg)

- 设置端口号(随意)

> ![](https://ws3.sinaimg.cn/large/006tNc79gy1fqguec1321j30cs015aad.jpg)

- 设置密码

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqgughr4icj30em01c0t3.jpg)

- 设置账号加密方式

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqguiwmggaj30hw0ewdm8.jpg)

- 进行混淆插件的设置

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqgumtxfdgj30jz0f7gso.jpg)

- 设置限制的设备数

> ![](https://ws3.sinaimg.cn/large/006tNc79gy1fqgupl5h7kj30jx06pn16.jpg)

- 安装完成，屏幕上会显示出所有的配置信息

> ![](https://ws4.sinaimg.cn/large/006tNc79gy1fqgurkw45hj30ka0cb0vr.jpg)

5. 在手机或是电脑上面下载ssr客户端

- [window](https://github.com/shadowsocksr-backup/shadowsocksr-csharp/releases)

- [mac](https://github.com/shadowsocksr-backup/ShadowsocksX-NG/releases)

- [android](https://github-production-release-asset-2e65be.s3.amazonaws.com/98545200/57cc1dc0-81f2-11e7-9793-8bdb755b5a6a?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20180419%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20180419T031356Z&X-Amz-Expires=300&X-Amz-Signature=851c8b8dee2d983e181d3f3bbc5b0a122a55e6d6b1b51061625e506c0c21808e&X-Amz-SignedHeaders=host&actor_id=29535839&response-content-disposition=attachment%3B%20filename%3Dshadowsocksr-release.apk&response-content-type=application%2Fvnd.android.package-archive)

- [linux](https://github.com/erguotou520/electron-ssr/releases)
