# Database
### 概念
&emsp;&emsp;**Database:** 数据库，数据的仓库，依据 "数据结构" 来组织数据
&emsp;&emsp;**DBMS:** 数据库管理系统，一种实现数据管理的程序软件，例如: Mysql数据库、MongoDB数据库
&emsp;&emsp;**ACID:** 数据库事务特性，分别是 **A**tomic原子性，**C**onsistency一致性，**I**solation隔离性，**D**urability持久性
### 类型
&emsp;&emsp;**关系型数据库:** 采用关系型模型来组织数据的数据库
&emsp;&emsp;&emsp;关系模型指的是二维表格模型，关系型数据库就是由二维表及其之间的联系所组成的一个数据组织
&emsp;&emsp;&emsp;代表: 甲骨文公司[ Oracle、Mysql]、微软公司[SQL Server(MS SQL)、ACCESS]、DB2、SQLite、MariaDB[MySQL的分支]等
&emsp;&emsp;**非关系型数据库:** NoSQL，基于"非关系模型"的数据库
&emsp;&emsp;&emsp;模型: 列模型，以一列为一个记录，数据即索引，IO速度快主要为分布式数据库，如: HBase
&emsp;&emsp;&emsp;&emsp;&emsp; 键值对模型，存储的数据是键值对，如: Redis,MemchacheDB
&emsp;&emsp;&emsp;&emsp;&emsp; 文档类模型，以文档来存储数据，类似"键值对"
