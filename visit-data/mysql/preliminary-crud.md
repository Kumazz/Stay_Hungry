# 初阶操作
### 概念
&emsp;&emsp;**CURD:** **C**reate 创建、**U**pdate 更新、**R**etrieve 读取和 **D**elete 删除
&emsp;&emsp;**SQL 命令**不区分大小写(命令建议大写)，表和数据库名小写，命令以 ; 结尾
&emsp;&emsp;**注释:** 单行注释 -- ；多行注释 /**/
### 其它
```sql
    net start mysql                        # 启动 MySQL 服务
    net stop mysql                         # 停止 MySQL 服务
    quit/exit 或者 CMD+D                    # 退出

```
### 数据库操作
    * 初阶操作
```sql
    SHOW DATABASES;                                     # 显示数据库
    USE 数据库名;                                        # 使用(进入)数据库
    CREATE DATABASE 数据库名;                            # 创建新数据库
    DROP DATABASE 数据库名;                              # 删除数据库
```
**查看用户,主机:** SELECT user,host FROM user;      
    * 高阶操作


```sql

```


### 数据表操作

```sql    
    SHOW TABLES;                                       # 显示数据表
    CREATE TABLE tbname(column_name column_type)       # 创建数据表
    DROP TABLE tbname                                  # 删除数据表
```
### 案例
&emsp;&emsp; 创建一个商品库，有一张存了各种水果信息的表，水果信息如下


```

```












