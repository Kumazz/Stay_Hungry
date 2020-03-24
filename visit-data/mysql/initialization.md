### 安装( mysql版本8.0.16 )
&emsp;&emsp;**windows / mac os:** https://dev.mysql.com/downloads/mysql/
&emsp;&emsp;**linux:** yum install mysql-server
&emsp;&emsp;**源码安装:** 下载的文件是压缩包( .zip等，不是.msi)，将其解压后(如解压在C盘根目录)进入文件夹在 bin 目录下进行命令操作
### windows 环境调试
&emsp;&emsp;**初始化**
```sql
    cd c:mysql-8.0.16-winx64\bin    # 进入可执行文件目录
    mysqld --initialize-insecure    # 默认未设置 root 密码
```
&emsp;&emsp;**启动服务**
```sql
    c:mysql-8.0.16-winx64\bin       # 进入可执行文件目录
    mysqld                          # 启动MySQL服务
```
&emsp;&emsp;**连接服务**
```sql
    c:mysql-8.0.16-winx64\bin       # 进入可执行文件目录
    mysql -u root -p                # 连接MySQL服务器，-u 为用户，-p 为 password
    直接回车                         # 提示输入密码，因未设置密码直接回车即可
```
&emsp;&emsp;**连接成功**
![](/assets/46084A22BF0D4C669D71B4B76D53BBD1.png)
#### 添加变量环境
&emsp;&emsp;**目的:** 解决重复进入可执行文件目录执行启动操作，解决直接命令启动MySQL
&emsp;&emsp;**方法:** 【右键 计算机/此电脑】-> 【属性】-> 【高级系统设置】-> 【高级】-> 【环境变量】-> 【系统变量】-> 【找到变量名 Path 双击】-> 【将MySQL的 bin 目录路径追加到变量值中(末尾即可),记得用 ; 隔开】
&emsp;&emsp;**测试:**
```sql
    mysqld                        # 启动 MySQL 服务
    mysql -u root -p              # 连接 MySQL 服务器
```
### linux 环境调试
```sql
    yum install mysql-server                # 安装
    mysql.server start                      # 启动服务
    mysql -h host -u user -p                # 连接
    ```
### mac os 添加环境变量
```shell
    vim ~/.bash_profile                            # 终端输入
    export PATH=$PATH:/usr/local/mysql/bin         # 在最后添加 export
    按 esc，输入 :wq 
    source ~/.bash_profile                         # 让环境变量生效
    mysql -u root -p                               # 连接 MySQL 服务器
```
![](/assets/1584932817487.jpg)
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
    按 esc ，输入 :wq                      # 保存退出
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




















