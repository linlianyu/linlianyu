# 安装mysql

1. 打开终端

2. 安装mysql客户端

```
# yum install mysql
```

安装过程中会有提示输入y和n，输入y回车就行

3. 安装mysql-devel

```
# yum install mysql-devel
```

4. 查看yum库下是否有有mysql-server

```
# yum -y list mysql-server
```

如果没有的话就自己下载下来

```
# wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
# rpm -ivh mysql-community-release-el7-5.noarch.rpm
```

5. 安装mysql-server

```
# yum install mysql-server
```

6. 修改mysql配置文件

```
# vim /etc/my.cnf
```

在[mysqld]中加入character-set-server=utf8

```
character-set-server=utf8
```

![](https://ws1.sinaimg.cn/large/006tKfTcly1frot99q5j4j30lk0ewq5j.jpg)

7. 启动mysql

```
# service mysqld start
```

![](https://ws3.sinaimg.cn/large/006tKfTcgy1frotcwn4ofj30dt012mxa.jpg)

8. 登录mysql

```
# mysql -u root -p
```

由于刚安装完成，所以还没有密码，当提示输入密码的时候直接回车会好了

9. 修改密码

- 切换到mysql数据库

```
mysql> use mysql;
```

- 设置密码

```
mysql> UPDATE user SET password=password("密码") WHERE user='root';
```

- 刷新权限

```
mysql> FLUSH PRIVILEGES;
```
