---
title: 那些记不住的SQL语句
abbrlink: 40bbf072
date: 2020-09-13
categories:
 - 学习
tags:
 - sql
---

!!! note SQL是啥
    是用于访问和处理数据库的标准的计算机语言

<!-- more -->

作为一个正在学习的Coder，不会一些`SQL`语句怎么行呢~~

## 最常用的

JAVA(MyBatis)里得用...

### 查找

```sql
SELECT * FROM <table_name>
SELECT * FROM <table_name> WHERE <field_name> = <value>
```

### 添加

```sql
INSERT INTO <table_name>(<field_name>) VALUES(<value>)
```

### 更新

```sql
UPDATE <table_name> SET <field_name>=<value> where <field_name> = <value>
```

### 删除

```sql
DELETE FROM <table_name>
DELETE FROM <table_name> where <field_name> = <value>
```

### 排序

```sql
SELECT * FROM <table_name> ORDER BY <field_name> [DESC]
```

## 不常用

我有可视化工具还需要这个吗!!

### 创建数据库

```sql
CREATE DATABASE <db_name>
```

### 删除数据库

```sql
DROP DATABASE <db_name>
```

### 创建表

```sql
CREATE TABLE <table_name>(<col> <type> [not null] [primary key],...)
```

### 删除表

```sql
DROP TABLE <table_name>
```
