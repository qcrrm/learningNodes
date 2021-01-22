执行顺序：yml文件会先加载，而后加载properties会覆盖yml文件

```yml
server:
  port: 8080
  servlet:
  context-path: /y
```

