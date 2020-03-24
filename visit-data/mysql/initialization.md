# 初始
### 用户管理


```sql
    CREATE USER '用户名'@'数据库ip' IDENTIFIED BY '密码';             # 创建新用户
    RENAME USER '用户名'@'数据库ip' TO '新用户名'@'数据库ip';           # 修改用户
    SET PASSWORD FOR '用户名'@'数据库ip' = PASSWORD('新密码');        # 修改密码
    DROP USER '用户名';                                             # 删除用户
    

```
**注意:** @ 左右不能有空格
### 授权管理
**常用权限一览表**  
|权限名|说明  |
|:---:|:---:|
|1    |2    |

* **初阶操作**

```sql
    SHOW GRANTS FOR '用户名'@'数据库ip';                              # 查看用户权限
    GREANT 权限1,权限2 ON 数据库.表 TO '用户名'@'数据库ip';              # 授权
    REVOKE 权限 ON 数据库.表 FROM '用户名'@'数据库ip';                  # 取消权限
```
* **高阶操作**
    * 权限 
    




### 修改密码
&emsp;&emsp;**windows 环境**忘记 root 密码，进行修改(找回)

```sql
    net stop mysql                         # 停止 MySQL 服务
    cd x:mysql-8.0.16-winx64\bin           # 进入可执行文件目录
    mysqld --skip-grant-tables;            # 跳过权限表认证
    新打开一个 DOS 窗口再次进入可执行文件目录
    update user set password=password("新密码") where user="root";# 给 root 设置新密码
    flush privileges;                     # 刷新权限
    quit;                                 # 退出
```
&emsp;&emsp;**linux 环境**忘记 root 密码，进行修改(找回)，其它 linux 环境自行百度

```sql
    service mysqld stop                   # 关闭 MySQL 服务
    vi /etc/my.cnf                        # 修改 MySQL 配置文件
    skip-grant-tables                     # 在 mysqld 下标签下添加这命令
    按 esc ,输入 :wq                       # 保存退出
    service mysqld start                  # 重启 MySQL 服务
    mysql -u root                         # 进入 MySQL
    use mysql;                            # 连接 Mysql
    UPDATE mysql.user SET authentication_string=password('新密码') where user='root';    # 修改密码
    flush privileges;                     # 刷新权限
    exit;                                 # 退出
    service mysql start                   # 启动 MySQL 服务
    mysql -u root -p                      # 连接 MySQL
    
```
### 自启动
&emsp;&emsp;**windows 环境:** 【右键 计算机/此电脑】-> 【管理】-> 【服务和应用程序】-> 【服务】-> 【找到 MySQL】-> 【右键 选择属性】-> 【启动类型 改为 自动】
&emsp;&emsp;**linux 环境:**
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




















