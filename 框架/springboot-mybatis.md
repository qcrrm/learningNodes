## 添加依赖



```xml
<!-- mybatis整合springboot包 -->
<dependency>
    <groupId>org.mybatis.spring.boot</groupId>
    <artifactId>mybatis-spring-boot-starter</artifactId>
    <version>2.1.3</version>
</dependency>
```

jdbc依赖包

```
<!-- https://mvnrepository.com/artifact/com.microsoft.sqlserver/sqljdbc4 -->
<!-- sqlserver的jdbc依赖包 -->
<dependency>
    <groupId>com.microsoft.sqlserver</groupId>
    <artifactId>sqljdbc4</artifactId>
    <version>4.0</version>
</dependency>

<!-- mysql的jdbc依赖包 -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <scope>runtime</scope>
</dependency>
```



```
<!--  -->
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid</artifactId>
    <version>1.1.22</version>
</dependency>
```



## 配置文件yml

```yml
spring:
	datasource:
		url: 
		username: 
		password: 
mybatis:
	mapper-locations: classpath: mapper/*.xml
	configuration:
        map-underscore-to-camel-case: true
```

```prop

```

