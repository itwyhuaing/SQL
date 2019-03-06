# SQLite


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


##### 参考

* [SQL 菜鸟](http://www.runoob.com/sql/sql-intro.html)
