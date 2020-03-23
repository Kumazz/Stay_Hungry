### 安装( mysql版本8.0.16 )
&emsp;&emsp;**windows:** https://dev.mysql.com/downloads/mysql/
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
![](/assets/1584932817487.jpg)
#### 添加变量环境
&emsp;&emsp;**目的:** 解决重复进入可执行文件目录执行启动操作，解决直接命令启动MySQL
&emsp;&emsp;**连接服务**

### linux 环境调试














