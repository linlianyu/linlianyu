# mac下完全卸载mysql

> mac下的myaql安装包中只有安装文件，没有卸载文件，所以只能通过终端命令来进行卸载

1. 打开终端

2. 输入一下命令

```
sudo rm /usr/local/mysql  
sudo rm -rf /usr/local/mysql*  
sudo rm -rf /Library/StartupItems/MySQLCOM  
sudo rm -rf /Library/PreferencePanes/My*
sudo rm -rf ~/Library/PreferencePanes/My*  
sudo rm -rf /Library/Receipts/mysql*  
sudo rm -rf /Library/Receipts/MySQL*  
sudo rm -rf /var/db/receipts/com.mysql.*
```
