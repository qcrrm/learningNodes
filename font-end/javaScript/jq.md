js与jq的区别

js是网页的脚本语言，而jq是基于js语言封装的一个前端框架



### readonly/disabled

```
$('input').attr('readonly', 'readonly');
$('input').removeAttr("readonly");
$('input').attr('readonly', '');

```

```
$('input').attr('disabled', 'disabled');
$('input').removeAttr("disabled");

```





disabled表单不会提交，readonly表单会提交