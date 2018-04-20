# 使用vmware安装凤凰os

---

 本文借鉴自[《VMware 12安装凤凰os》](https://jingyan.baidu.com/article/20095761dce379cb0721b41b.html)

---

1. 下载[PhoenixOS](https://pan.baidu.com/s/15mPo7Sh7fUjQeFBBG4s5VA)

2. 新建一个虚拟机，具体的配置自己设置

3. 选择"installation"

> ![](https://ws2.sinaimg.cn/large/006tKfTcgy1fqhrh1fqixj31400p0dmq.jpg)

4. 选择"create/modify partitions"新建分区表，回车

> ![](https://ws2.sinaimg.cn/large/006tKfTcgy1fqhriwvbjuj31400p0ta4.jpg)

5. 询问是否使用GPT分区，选择"no"

> ![](https://ws4.sinaimg.cn/large/006tKfTcgy1fqhrl10lvzj31400p0wfy.jpg)

6. 进入分区工具，选择"new"，然后回车

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhro39nj6j31400p0ta2.jpg)

7. 选择"primary"，然后回车

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhrqu0pvij31400p0dh8.jpg)

8. 设置分区大小，直接回车，将所有空间分配给分区

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhrrzd7mpj31400p0gmz.jpg)

9. 将这个分区设置为可引导的,选择"Bootable",然后回车，

> ![](https://ws4.sinaimg.cn/large/006tKfTcgy1fqhrudgtiaj31400p0abp.jpg)

10. 选择"write",然后回车

> ![](https://ws1.sinaimg.cn/large/006tKfTcgy1fqhrvstwtaj31400p0gn2.jpg)

11. 输入"yes"，然后回车

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhrwx8yi1j31400p03zw.jpg)

12. 选择"quit"，然后回车

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhrxrfm91j31400p00u4.jpg)

13. 选择新建的分区sda1，然后回车

> ![](https://ws2.sinaimg.cn/large/006tKfTcgy1fqhryu0f00j31400p0wfw.jpg)

14. 设置分区的格式,选择"ext4"，然后回车

> ![](https://ws1.sinaimg.cn/large/006tKfTcgy1fqhs13smlrj31400p0400.jpg)

15. 选择"yes"，然后回车

> ![](https://ws4.sinaimg.cn/large/006tKfTcgy1fqhs2kwvatj31400p0q4h.jpg)

16. 是否安装EFI应到，选择"skip"，然后回车

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhs2zbmotj31400p0gn3.jpg)

17. 是否安装grub，选择"yes",然后回车

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhs3idbxij31400p0myn.jpg)

18. 重启，选择"reboot"

> ![](https://ws4.sinaimg.cn/large/006tKfTcgy1fqhs5b7er2j31400p0wg0.jpg)

19. 在grub菜单中，使用键盘输入"e",然后再输入"e"

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhs99uq2kj31400p0q4d.jpg)

> ![](https://ws1.sinaimg.cn/large/006tKfTcgy1fqhs9lkpk0j31400p0ta8.jpg)

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhs9roelnj31400p0wfv.jpg)

20. 在末尾输入"nomodeset",然后回车，返回上一级界面

> ![](https://ws1.sinaimg.cn/large/006tKfTcgy1fqhsc25p15j31400p0gmz.jpg)

21. 键盘输入"b",即可进入系统

> ![](https://ws3.sinaimg.cn/large/006tKfTcgy1fqhscj6jhkj31400p0jsx.jpg)

##  注意事项

- 每次重启凤凰系统的虚拟机，都要重复19-21的操作
