### @PathVariable @RequestParam

`@PathVariable`用于获取路径参数, `@ReqeustParam`用于获取查询参数

```
@GetMapping("/student/{grade}/list");
public Object listStudent(
	@PathVariable("grade") Long grade,
	@ReqeustParam("value="classes")String classes
){

}
```

请求url：`/student/9/list?classes=2`

取到的数据为`grade=9, classes=2`