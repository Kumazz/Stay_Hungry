# Database
### 概念
&emsp;&emsp;**Database:** 数据库，数据的仓库，依据 "数据结构" 来组织数据
&emsp;&emsp;**DBMS:** 数据库管理系统，一种实现数据管理的程序软件，例如: Mysql数据库、MongoDB数据库
&emsp;&emsp;**ACID:** 数据库事务特性，分别是 **A**tomic原子性，**C**onsistency 一致性，**I**solation 隔离性，**D**urability 持久性
&emsp;&emsp;**CAP:** 分布式系统基本需求，分别是 **C**onsistency 一致性，**A**vailability 可用性，**P**artition tolerance 分区容错性
### 类型
&emsp;&emsp;**关系型数据库:** 采用关系型模型来组织数据的数据库
&emsp;&emsp;&emsp;关系模型指的是二维表格模型，关系型数据库就是由二维表及其之间的联系所组成的一个数据组织
&emsp;&emsp;&emsp;代表: 甲骨文公司[ Oracle、Mysql]、微软公司[SQL Server(MS SQL)、ACCESS]、DB2、SQLite、MariaDB[MySQL的分支]等
&emsp;&emsp;**非关系型数据库:** NoSQL，基于"非关系模型"、分布式的且一般不遵循ACID原则的数据存储系统
&emsp;&emsp;&emsp;代表: 列模型，以一列为一个记录，数据即索引，IO速度快主要为分布式数据库，**面向可扩展性的分布式数据库**，如: HBase
&emsp;&emsp;&emsp;&emsp;&emsp; 键值对模型，存储的数据是键值对，**面向高性能并发读写的key-value数据库**，如: Redis,MemchacheDB
&emsp;&emsp;&emsp;&emsp;&emsp; 文档类模型，以文档来存储数据主要是JSON，**面向海量数据访问可以快速查询数据**，类似"键值对"，如: MongoDB
&emsp;&emsp;&emsp;&emsp;&emsp; 其他，用于对海量数据进行近实时的处理和分析处理，**面向搜索数据内容的搜索引擎**，可用于机器学习和数据挖掘，如: Splunk,Elasticsearch
### 优缺
&emsp;&emsp;**关系型数据库优点:** 采用二维表结构容易理解，通用的SQL语言操作方便，丰富的完整性减低了数据冗余和数据不一致的概率易于维护
&emsp;&emsp;**非关系型数据库优点:** 根据需求添加字段，成本低查询速度快效率高，扩展性高
&emsp;&emsp;**关系型数据库缺点:** 硬盘 I/O 决定了读写请求用户并发性高低，效率低在横向扩展升级时要停机维护和数据迁移性能欠佳
&emsp;&emsp;**非关系型数据库缺点:** 只能存储简单的数据，没有存储过程断电易丢失数据，不支持SQL不提供对事务的处理
### 对比
&emsp;&emsp;**成本:** NoSQL基本是开源软件简单易部署较为便宜
&emsp;&emsp;**查询速度:** NoSQL数据存储于缓存之中，不经过SQL层解析；关系型数据库将数据存储在硬盘中，查询速度远不及NoSQL数据库
&emsp;&emsp;**存储数据格式:** NoSQL存储格式有基础类型以及对象或集合各种格式，而关系型数据库只支持基础类型
&emsp;&emsp;**扩展性:** NoSQL数据之间没有耦合性容易水平扩展；关系型数据库因多表查询机制的限制导致扩展艰难
&emsp;&emsp;**持久存储:** NoSQL数据主要存在缓存中不适合持久存储
&emsp;&emsp;**数据的一致性:** NoSQL的数据有可能处于一个中间态的数据只强调数据最终一致性


