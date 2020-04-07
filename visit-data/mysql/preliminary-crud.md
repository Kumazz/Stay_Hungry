# 初阶操作
### 概念
&emsp;&emsp;**常用数据类型** 
<table>
    <tr>
        <th rowspan="2">类型</th>
        <th colspan="2">内容</th>
        <th colspan="3">释义</th>
    </tr>
    <tr>
        <td>整型</td>
        <td>tinyint、int、bigint</td>
        <td>整型，根据有无符号、数据大小选择类型</td>
    </tr>
    <tr>
        <td>浮点型</td>
        <td>float、double、decimal(10,2)</td>
        <td>单精度、双精度一般不怎么精确，采用 decimal(总数,位数)</td>
    </tr>
    <tr>
        <td>字符串类</td>
        <td>char(10)、varchar(10)</td>
        <td>char(字节长度)与varchar区别在于后者节省空间，但是速度较慢</td>
    </tr>
</table>

&emsp;&emsp;**常用字段属性** 
<table>
    <tr>
        <th rowspan="2">属性</th>
        <th colspan="2">释义</th>
    </tr>
    <tr>
        <td>signer / unsigner</td>
        <td>有符号 / 无符号</td>
    </tr>
    <tr>
        <td>null / not null</td>
        <td>可以空值 / 不可为空</td>
    </tr>
    <tr>
        <td>auto_increment</td>
        <td>自增(唯一列)，与主键搭配</td>
    </tr>
    <tr>
        <td>primary key</td>
        <td>主键，约束(唯一列且不能为空)、加速查找</td>
    </tr>
</table>

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
    CREATE DATABASE IF NOT EXISTS 数据库名;                        # 创建数据库如果该库不存在
    CREATE DATABASE IF NOT EXISTS 数据库名 DEFAULT CHARSET = '编码';  # 创建数据库并指明编码
    ALTER DATABASE 数据库名 CHARACTER SET '编码';                   # 修改编码
```

### 单表操作
&emsp;&emsp;**初阶操作**
```sql    
    SHOW TABLES;                                       # 显示(查看)数据表
    CREATE TABLE tbname(column_name column_type) DEFAULT CHARSET = 'utf8';      # 创建数据表
    DROP TABLE tbname;                                  # 删除数据表
    
    DELETE FROM tbname;                                 # 清空表内数据保留表
    TRUNCATE TABLE tbname;                              # 清空数据，推荐使用，速度快适合删除大量数据
```
&emsp;&emsp;**高阶操作**

```sql
    CREATE TABLE tbname(colname coltype) ENGINE = 'innodb' DEFAULT CHARSET = 'utf8';        # 支持事务回滚操作
    
```

### 数据操作

```sql
    SELECT * FROM tbname;                              # 显示(查看)数据
    INSERT INTO tbname(colname) VALUES(data)           # 对应字段插入数据
    
```



















