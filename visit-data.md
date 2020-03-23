# Database
### 概念
&emsp;&emsp;**Database:** 数据库，数据的仓库，依据 "数据结构" 来组织数据
&emsp;&emsp;**DBMS:** 数据库管理系统，一种实现数据管理的程序软件，例如: Mysql数据库、MongoDB数据库
&emsp;&emsp;**ACID:** 数据库事务特性，分别是 **A**tomic原子性，**C**onsistency一致性，**I**solation隔离性，**D**urability持久性
&emsp;&emsp;**CAP:** 分布式系统基本需求，分别是 **C**onsistency一致性，**A**vailability可用性，**P**artition tolerance分区容错性
### 类型
&emsp;&emsp;**关系型数据库:** 采用关系型模型来组织数据的数据库
&emsp;&emsp;&emsp;关系模型指的是二维表格模型，关系型数据库就是由二维表及其之间的联系所组成的一个数据组织
&emsp;&emsp;&emsp;代表: 甲骨文公司[ Oracle、Mysql]、微软公司[SQL Server(MS SQL)、ACCESS]、DB2、SQLite、MariaDB[MySQL的分支]等
&emsp;&emsp;**非关系型数据库:** NoSQL，基于"非关系模型"、分布式的且一般不遵循ACID原则的数据存储系统
&emsp;&emsp;&emsp;模型: 列模型，以一列为一个记录，数据即索引，IO速度快主要为分布式数据库，**面向可扩展性的分布式数据库**，如: HBase
&emsp;&emsp;&emsp;&emsp;&emsp; 键值对模型，存储的数据是键值对，**面向高性能并发读写的key-value数据库**，如: Redis,MemchacheDB
&emsp;&emsp;&emsp;&emsp;&emsp; 文档类模型，以文档来存储数据主要是JSON，**面向海量数据访问可以快速查询数据**，类似"键值对"，如: MongoDB
&emsp;&emsp;&emsp;&emsp;&emsp; 其他，用于对海量数据进行近实时的处理和分析处理，**面向搜索数据内容的搜索引擎**，可用于机器学习和数据挖掘，如: Splunk,Elasticsearch
### 对比
&emsp;&emsp;**关系型数据库:** 采用二维表结构容易理解，通用的SQL语言操作方便，丰富的完整性减低了数据冗余和数据不一致的概率易于维护
