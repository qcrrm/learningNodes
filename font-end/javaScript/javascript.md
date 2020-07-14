https://www.w3school.com.cn/js/index.asp

```javascript
document.getElementById("").innerHTML = ""

document.getElementById("").style.fontSize=""

document.getElementById("").src=""
```

### 常见的HTML事件

| 事件        | 描述                     |
| ----------- | ------------------------ |
| onclick     | 用户点击了HTML元素       |
| onmouseover | 把鼠标移动到HTML元素     |
| onmouseout  | 鼠标移开HTML元素         |
| onkeydown   | 用户按下键盘按键         |
| onload      | 浏览器已经完成了页面加载 |
| onchange    | HTML元素已被改变         |

### 转义字符

| 代码 | 结果       |
| ---- | ---------- |
| \b   | 退格键     |
| \f   | 换页       |
| \n   | 新行       |
| \r   | 回车       |
| \t   | 水平制表符 |
| \v   | 垂直制表符 |
| \\'  | '          |
| \\"  | "          |
| \\\  | \          |

### 字符串方法

```javascript
var txt=  "ACBDefg Deqwe";
var sln = txt.length;
//indexOf()查找字符串中的字符串位置 首次出现的索引
var pos = txt.indexOf("De");
//lastIndexOf() 最后一次出现的索引
var lastPos = txt.lastIndexOf("De");
//未找到，返回-1

//search() indexOf()的区别
//search() 方法无法设置第二个开始位置参数。
//indexOf() 方法无法设置更强大的搜索值（正则表达式）。
```

### 提取部分字符串

```
slice(start,end)//如果某个参数为负，则从字符串的结尾开始计数
substring(start,end)//无法接受负索引
substr(str,end)//第二个参数是被提取部分的长度

replace("a","b");
// 不会改变调用它的字符串，只会返回一个新的字符串。
// 只替换首个匹配
// 对大小写敏感
// 使用/i执行大小写不敏感处理

toUpperCase() toLowerCase()
concat()//连接两个或多个字符串

trim() 删除字符串两端的空白符

split()将字符串转换为数组

```

### 数字

### 数组

```
var points = new Array(40, 100, 1, 5, 25, 10); // 差
var points = [40, 100, 1, 5, 25, 10];          // 优
Array.isArray(); //判断是否是数组
```

```
jion()//方法可以将所有的数组元素结合成为一个新字符串
pop() //从数组中删除最后一个元素
push() //向数组结尾处添加一个新的元素
shift() //删除首个数组元素,并把所有其他元素"位移"到更低的索引
unshift() //在数组头部添加新元素
splice(2,0,"","");//向数组添加新项
//2定义了添加新元素的位置
//0定义了应删除的多少元素
//其余参数定义要添加的新元素
concat() //合并先有的数组来创建一个新的数组
slice() //裁剪数组



```

```
sort() //数组排序
reverse() ///方法反转数组中的元素
```

```
forEach(); //为每个数组元素调用一次函数
//三个参数 项目值，项目索引，数组本身

reduce();
//四个参数,总数,项目值,项目索引,数组本身

every(); //检查所有数组是否通过测试
//三个参数 
项目值
项目索引
数组本身

indexOf(); //在数组中搜索元素值并返回其位置

lastIndexOf()

find(); 
```

### 日期

```
var date = new Date();
//Tue Apr 07 2020 16:08:07 GMT+0800 (中国标准时间)

new Date();
new Date(year,month,day,hours, minutes, seconds,milliseconds)
new Date(milliseconds)
new Date(date string)
```



### 选择器





