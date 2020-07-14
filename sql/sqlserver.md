添加字段

```
alter table table_name add column varchar(255)
```

修改字段名

```
exec sp_rename 'table_name.old_column_name','new_column_name','column'
```

