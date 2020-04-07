# 初阶操作
### 数据库操作
&emsp;&emsp;**初阶操作**
```sql
    SHOW DATABASES;                     # 显示(查看)数据库
    USE 数据库名;                        # 使用(进入)数据库
    CREATE DATABASE 数据库名;            # 创建新数据库
    DROP DATABASE 数据库名;              # 删除数据库
```
**查看用户,主机:** SELECT user,host FROM user;

&emsp;&emsp;**高阶操作**

```sql
    CREATE DATABASE IF NOT EXISTS 数据库名; # 创建数据库如果该库不存在
    CREATE DATABASE IF NOT EXISTS 数据库名 DEFAULT CHARSET = '编码' # 创建数据库并指明编码
    ALTER DATABASE 数据库名 CHARACTER SET '编码' # 修改编码
```

### 数据表操作

```sql    
    SHOW TABLES;                                       # 显示(查看)数据表
    CREATE TABLE tbname(column_name column_type) DEFAULT CHARSET = 'utf8'      # 创建数据表
    DROP TABLE tbname                                  # 删除数据表
```

### 数据操作

```sql
    SELECT * FROM tbname;                              # 显示(查看)数据
    
```



















