# MySQL
### 概念
&emsp;&emsp;**MySQL**是一个流行的关系型数据库的DBMS，目前属于 Oracle 旗下，在 WEB 应用方面 MySQL 是最好的应用软件之一
### 安装(windows环境,mysql版本8.0.16)
&emsp;&emsp;**windows:** https://dev.mysql.com/downloads/mysql/
&emsp;&emsp;**linux:** yum install mysql-server
&emsp;&emsp;**源码安装:** 下载的文件是压缩包，将其解压后(如解压在C盘根目录)进入文件夹在 bin 目录下进行命令操作
### 调试
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
    c:mysql-8.0.16-winx64\bin
    mysql -u root -p                # 连接MySQL服务器，-u 为用户，-p 为 password
```












