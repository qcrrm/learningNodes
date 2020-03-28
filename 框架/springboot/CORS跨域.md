## Spring项目配置CORS的几种方式

WebMvcConfigurerAdapter已过时，替代的是WebMvcConfigurer接口。

### Controller方法上添加CORS配置

注解

@CrossOrigin

```
@CrossOrigin(value = "*", maxAge = 3600)
@RequestMapping(value = "/test01", method = RequestMethod.POST)
public Object login() {
    Result result = new Result();
    result.setCode(200);
    result.setData("访问成功");
    return result;
}
```

### 全局配置-实现接口WebMvcConfigurer

```
@Configuration
@EnableWebMvc
public class WebConfig implements WebMvcConfigurer {
    @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/**")
                .allowedOrigins("*")
                .allowedMethods("*")
                .allowedHeaders("*");
        WebMvcConfigurer.super.addCorsMappings(registry);
    }
}
```

/**代表任何

### 全局配置-@Bean



## 登录验证用Filter还是Interceptor

## Interceptor两次