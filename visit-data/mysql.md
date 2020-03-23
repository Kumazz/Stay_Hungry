# MySQL
### 概念
&emsp;&emsp;**MySQL**是一个流行的关系型数据库的DBMS，目前属于 Oracle 旗下，在 WEB 应用方面 MySQL 是最好的应用软件之一
### 自启动
&emsp;&emsp;**windows环境:** 【右键 计算机/此电脑】-> 【管理】-> 【服务和应用程序】-> 【服务】-> 【找到 MySQL】-> 【右键 选择属性】-> 【启动类型 改为 自动】
&emsp;&emsp;**linux环境:**
```sql
    cp /usr/local/mysql/support-files/mysql.server /etc/init.d/mysqld            # 拷贝并重命名
    chmod +x /etc/init.d/mysqld         # 赋予执行权限
    chkconfig --add mysqld              # 添加到服务
    chkconfig --list                    # 显示服务，找到 mysqld 服务查看，如果 3、4、5 是on/开启即成功
    chkconfig --level 345 mysqld on     # 如果是关闭则输入此命令
    reboot                              # 重启服务器
    netstat -na | grep 3306             # 如果看到有监听说明成功
```
![](/assets/20180702190816838.png)















