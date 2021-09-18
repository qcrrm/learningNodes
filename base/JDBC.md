Java Data Base Connectivity

加载驱动程序

```
Class.forName(driveClass);
```

获取数据库连接

```
String url = "";
String username = "";
String passowrd = "";
Connection conn = DriverManager.getConnection(url,username,password);
```

创建对象

```
Statement stat = conn.createStatement();
PreparedStatement preparedStatement = conn.prepareStatement(sql);
```

