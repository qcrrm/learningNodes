**环境：**

Linux version 3.10.0-957.21.3.el7.x86_64

mysql  Ver 8.0.18 for Linux on x86_64 (MySQL Community Server - GPL)

**启动mysqld服务，并设为开机自动启动命令**

```
systemctl start mysqld.service
systemctl enable mysqld.service
```

**重启mysql**

```
sytemctl restart mysqld
```

**进入mysql**

```
mysql -u root -p
```

## sql语句

**显示所有数据库**

```
show databases;
create database test;
use test;
```

**查询某个数据库下所有数据表名**

```
select table_name from information_schema.tables where table_schema = 'test';
```

**查看表结构**

```
desc student;
```

### 创建数据表

修改数据时自动添加时间

```sql
--defalut current_timestamp 
`gmt_create` datetime defalut current_timestamp comment '创建时间',
-- on update current_timestamp
`gmt_modified` datetime dafault current_timestamp on update current_timestamp comment '更新时间',
```

### 添加字段

```
alert table table_name add column_name varchar(20) not null
```



## 数据类型

| mysql   | java   |      |
| ------- | ------ | ---- |
| VARCHAR | String |      |
| CAHR    | String |      |
|         |        |      |
|         |        |      |
|         |        |      |
|         |        |      |
|         |        |      |
|         |        |      |
|         |        |      |

