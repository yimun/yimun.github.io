class: center, middle
# SQL 入门

yimulinwei@gmail.com

---


## 概念

### 数据库
数据仓库，运行于服务器上
一个数据库由多张表组成

### 关系型数据库
是创建在关系模型基础上的数据库，借助于集合代数等数学概念和方法来处理数据库中的数据。现实世界中的各种实体以及实体之间的各种联系均用关系模型来表示

---
### 表
一个关系型数据库由许多表组成，表的结构都是二维的
![](/image/14962314547095.jpg)


#### 字段
关系表中每一列的定义就是字段，字段也是查询操作中的一个主要对象

#### 记录
对应表中每一行

---


### SQL
SQL 是所有**关系型数据库**的数据库语言，包括`SQL Server、Oracle、MySQL、Sybase` 以及 `Access` 等等, 功能包括:
- DSL 数据库操纵语言
- 数据库结构定义
- 数据增删改查操作
- 存储过程

---

## 查询 SELECT
SELECT 语句用于从表中选取数据。
结果被存储在一个结果表中（称为结果集）。
```sql
SELECT 列名称(字段名) FROM 表名称

SELECT * FROM 表名称
```

---

### SELECT
Persions表：
![](/image/14962324341893.jpg)


执行：
```sql
SELECT LastName,FirstName FROM Persons
```

返回：
![](/image/14962323544204.jpg)


---

### SELECT * 
Persions表：
![](/image/14962324248626.jpg)

执行：
```sql
SELECT * FROM Persons
```

结果：
![](/image/14962324004645.jpg)


---

## 条件查询
语法：
```sql
SELECT 列名称 FROM 表名称 WHERE 列 运算符 值
```

常用运算符：

| 操作符 | 描述 |
|:-------:|:-----:|
| = | 等于 |
| <> | 不等于 |
| > | 大于 |
| = | 大于等于 |
| <= | 小于等于 |
| BETWEEN | 在某个范围内 |
| LIKE | 搜索某种模式 |


---

### 实战
"Persons" 表
![](/image/14962327701456.jpg)


执行：
```sql
SELECT * FROM Persons WHERE City='Beijing'
```

结果：
![](/image/14962328071325.jpg)

---
### 练习
"Persons" 表
![](/image/14962327701456.jpg)

执行：
```sql
SELECT * FROM Persons WHERE FirstName='Bush'

SELECT * FROM Persons WHERE Year>'1965'
```

---

## AND/OR
"Persons" 表
![](/image/14962327701456.jpg)

执行：
```sql
SELECT * FROM Persons WHERE City='Beijing' AND Year>'1975'
SELECT * FROM Persons WHERE (City='London' OR City='Beijing') AND Year<1980
```


