# 多表操作
### 概念
&emsp;&emsp;**常用字段属性**

&emsp;&emsp;**案例**
```sql
    CREATE TABLE userinfo(
        uid tinyint auto_increment primary key,
        name varchar(20),
        department_id int,
        constraint fk_user_depar foreign key ("department_id") references department("id")
    ) ENGINE = 'innodb' DEFAULT CHARSET = 'utf8';
    
    CREATE TABLE department(
        id tinyint auto_increment primary key,
        title varchar(20)
    ) ENGINE = 'innodb' DEFAULT CHARSET = 'utf8';


```








































