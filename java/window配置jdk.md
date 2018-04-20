
# window配置jdk

1. jdk安装完成后，复制jdk的安装路径

```
C:\Program Files\Java\jdk-10
```

2. 右键"计算机"--->"属性"

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqgmx3bryij30pa0gqn10.jpg)

3. 单击"环境变量"

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqgmz0wyefj30bt0cft9p.jpg)

4. 在"系统变量"中点击"新建"

> ![](https://ws1.sinaimg.cn/large/006tNc79gy1fqgn0jyzedj30ay0bgjs9.jpg)

5. 变量名输入"JAVA_HOME",变量值输入之前复制的jdk的目录

> ![](https://ws3.sinaimg.cn/large/006tNc79gy1fqgn3qky1nj30a1046dg9.jpg)

6. 在"系统变量"中找到"Path"，点击"编辑"

> ![](https://ws4.sinaimg.cn/large/006tNc79gy1fqgn6x6c6bj30b10bd0tm.jpg)

7. 在"变量值"前面加入",;%JAVA_HOME%\bin;"

```
,;%JAVA_HOME%\bin;
```

> ![](https://ws4.sinaimg.cn/large/006tNc79gy1fqgn8pb028j309y046mxl.jpg)

8. 打开命令行，输入"javac"

```
C:\Users\linlianyu>javac
```

> ![](https://ws2.sinaimg.cn/large/006tNc79gy1fqgndy2hlij30it0n9q5q.jpg)
