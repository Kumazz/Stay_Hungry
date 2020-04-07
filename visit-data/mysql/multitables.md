# 多表操作
### 概念
&emsp;&emsp;**常用字段属性**
<table>
    <tr>
        <th rowspan="2">属性</th>
        <th colspan="2">释义</th>
    </tr>
    <tr>
        <td>foreign key</td>
        <td>外键，节约空间，约束保证数据一致性</td>
    </tr>
</table>
&emsp;&emsp;**案例**
```sql
    CREATE TABLE userinfo(
        uid tinyint auto_increment primary key,
        name varchar(20),
        constraint fk_user_depar foreign key ("department_id") references department("id")
    ) ENGINE = 'innodb' DEFAULT CHARSET = 'utf8';
    
    CREATE TABLE department(
        id tinyint auto_increment primary key,
        title varchar(20)
    ) ENGINE = 'innodb' DEFAULT CHARSET = 'utf8';


```








































