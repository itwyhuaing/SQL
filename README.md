# SQLite

##### 了解

* SQL，指结构化查询语言，全称是 Structured Query Language。
* CURD 是一个数据库技术中的缩写词，一般的项目开发的各种参数的基本功能都是CURD。作用是用于处理数据的基本原子操作。它代表创建（Create）、更新（Update）、读取（Retrieve）和删除（Delete）操作。
* 能力

  > SQL 面向数据库执行查询

  > SQL 可从数据库取回数据

  > SQL 可在数据库中插入新的记录

  > SQL 可更新数据库中的数据

  > SQL 可从数据库删除记录

  > SQL 可创建新数据库

  > SQL 可在数据库中创建新表

  > SQL 可在数据库中创建存储过程

  > SQL 可在数据库中创建视图

  > SQL 可以设置表、存储过程和视图的权限

* SQL 对大小写不敏感：例如 SELECT 与 select 是相同的。


##### 常用 SQL 命令 /语句

* 命令

> 增创建新数据库

```
CREATE DATABASE
```


> 修改数据库

```
ALTER DATABASE
```


> 创建新表

```
CREATE TABLE
```


> 变更（改变）数据库表

```
ALTER TABLE
```


> 删除表

```
DROP TABLE
```


> 创建索引（搜索键）

```
CREATE INDEX
```


>  删除索引

```
DROP INDEX
```


> 从数据库中提取数据

```
SELECT
```



> 更新数据库中的数据

```
UPDATE
```


> 从数据库中删除数据

```
DELETE
```


> 向数据库中插入新数据

```
INSERT INTO
```


* 语句

```
select column_name,column_name from table_name;
select * from table_name;

select distinct column_name,column_name from table_name;

// 这里运算符有 : =、<>/!=、>、<、>=、<=、BETWEEN、LIKE、IN
select column_name,column_name from table_name where column_name operator value; （逻辑运算的优先级： not、and、or）

// 排序查询
select column_name,column_name from table_name order by column_name,column_name asc|desc;


insert into table_name values (value1,value2,value3);
insert into table_name (column1,column2,column3) values (value1,value2,value3);


update table_name set column1=value1,column2=value2;
update table_name set column1=value1,column2=value2 where some_column=some_value;


delete from table_name;
delete * from table_name;
delete from table_name where some_column=some_value;
```

> 建 Person 表

```
create table if not exists Person (
id integer primary key autoincrement,
name text,
age  integer,
addr text,
man  real,
)
```

> 增 - 插入一条数据

```
insert into Person (name,age,man,addr) values ("开发者WYH",68,true,"ShenZhen")

```

> 删 - 删除一条数据

```
delete from Person where name = "开发者WYH"
```

> 删 - 删除表

```
delete table Person
```


> 改/更新

```
update Person set name = "开发者WYH2" where id = 8
```


> 查 - 查所有列数据

```
select * from Person
```


> 查 - 单个条件

```
selet * from Person where name = "开发者WYH"
```


> 查 - 多个条件

```
select * from Person where age = 88 or addr = "深圳"
select * from Person where age = 88 and addr = "深圳"
```


> 查 - 查列数据

```
select age from Person
select distinct age from Person
```


> 添加属性/字段

```
alter table Person add column uniCode integer
```


> 删除属性/字段（部分数据库系统不准许该操作）

```
alter table Person drop column age
```


> 修改已存在的数据类型

```
alter table Person alter column age text
```


> 计算数据库中所有数据条数

```
select count(*) from Person
select count(distinct name) from Person
```

##### 工具

* Datum - 应用商店提供，可用于查看本地数据库。
* Sequel Pro - Apple 提供，可连接远程数据库。


##### 参考

* [SQL 菜鸟](http://www.runoob.com/sql/sql-intro.html)
* [CoreData应用简介](https://github.com/itwyhuaing/OC-WYH/tree/master/DataStore/CoreData应用简介)
* [Realm应用简介](https://github.com/itwyhuaing/OC-WYH/tree/master/DataStore/Realm应用简介)
