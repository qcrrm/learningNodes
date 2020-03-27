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

