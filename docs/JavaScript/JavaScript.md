# JavaScript

## js基本介绍

- js主要用于网页的动态效果实现。
- js是基于对象和事件驱动的`脚本语言`，无需编译，由浏览器的js解析引擎解释执行。



## 导入方式

### 外部导入

通过自定义`.js`文件，通过`<script>`标签内的`src`加路径导入。

```
<script src="js.js" type="text/javascript"></script> 
```



### 内部导入

通过直接在`<script>`标签内自定义。但作用范围只在当前Html网页中。

```
<script type="text/javascript">

	// 代码逻辑

</script> 
```



## 语法

### 注释

``` 
//	单行注释

/*
	多行注释
*/
```



### 变量

通过`var`定义，由于`JS`是弱类型语言，所以不必定义专门的类型。



#### 原始数据类型

* number：数字、小数、NaN（不是数字的数字类型）
* strin：字符或字符串，由" "表示
* boolean：布尔类型：true（真）、false（假）。
* null：空，没有具体内容，只是一个占位符（空格不是）。
* undefined：未定义类型。没有定义后直接输出。



#### 引用类型

object：对象



### 运算符

#### 算数运算

 `+`、`-`、 `*`、 `/`、 `%`、 `++`、 `--`



#### 赋值运算符

`=`、 `+=`、 `-=`、 `*=`、 `/=`、 `%=`



#### 比较运算符

`>`、 `<` 、`>=` 、`<=` 、`!=` 、`==` 、`===` 、`!==`



#### 逻辑运算符

取反：`!` 且：` &&` 或： `||`



#### 三元运算

```
X ? y:z
// x 是一个表达式
// y 第一个分支
// z 第二个分支
```



### 流程控制

#### 判断语句

```
if() {
    
} else if (){
    ....
} else
```



#### 选择语句

```
switch (变量) {
    case 变量一: 执行语句；break;
    case 变量一: 执行语句；break;
    case 变量一: 执行语句；break;
    default: 语句一; break;	(其他)
}
```



#### 循环语句

#####  while:

```
while(条件语句) {
    循环体
}
```

在满足条件语句的情况下执行。

##### do while:

```
do {
    循环体
}while(条件语句)；
```

先执行循环体一次，然后在满足条件语句的情况下执行循环体。

##### for:

```
for (语句1; 条件语句2; 语句3) {
    循环体
}
```

语句1：定义一个变量，为循环的计数器

语句2：计数器的判断语句，为`false`的情况下不执行

语句3：一般为计数器自增，具体为`++i`。

**重点**：

* 在一般情况下，各种语句都可以没有，但要在循环体内加上结束循环提的语句。
* 循环可以用于制作猜数字。

##### 结束循环

```
break ---- 结束当前循环
continue ---- 结束当前一次循环
```

## 对象

### 数组

#### 数组的定义

##### 动态初始化：

由程序员自己定义数组的长度。

```
var a = new Array();	// 不指定长度。

var a = new Array(10)	// 长度为10。

var a = new Array(1, 2, 3)	// 元素为：1， 2， 3。
```

##### 静态初始化：

由系统定义长度。

```
var a = [1, 2, 3, 4];	// 系统自动分配长度：4。

var a = [];			   // 系统自动分配长度：0。
```

**与`Java`不同的是，`JS`由于是一个弱类型语言，所以一个数组内可以储存不同类型的元素。**



### 函数

函数其实是一个封装体，类似`Java`中的方法。

#### 定义

```
function 方法名 () {
    
    函数体；
    
    return;		// 返回值，当函数没有返回值的时候，可以不写。
}
```

**对于没有参数的函数，传参也可以运行。有参数的函数不传参也可以运行。而且，没有`Java`中的重载**

**（同一个函数名有不同的参数），只会执行最近的代码块。**



#### 函数调用

```
函数名（ [参数] ）；
```



#### 传参储存的数组

传参被储存于`arguments`数组中，所以有参、无参函数都能在异常状况下使用。



#### 动态数组

```
var arr = new Function(
				"参数1, 参数2",	// 方法参数 
				"方法体"		// 方法体
			)
演示：
var arr0 = new Function(
            "x, y",
            "return x +y;"
        )

alert(arr0(5, 8));
输出：13
```



#### 匿名函数

没有名字的函数

```
var arr = function (参数1， 参数2) {
    函数体；
    
    return
}
演示：
var arr = function (a, b) {
    return a + b;
}
alert(arr(2, 3));
结果：5
```



#### 函数输出：函数名、函数()、对象。

```

```



#### 全局变量、局部变量

全局变量：指在`script`标签中定义的变量，在`当前网页`或`导入JS文件`中使用。

局部变量：值在`函数内部`定义的变量，只在函数内部生效。



### Objeck

提供了所有对象的通用方法,类似Java中的父类。

####  通用方法

```
toLocaleString 
toString
valueOf
```



### String



### Array



### Date



### 自定义对象



### Math



### Global





## DOM/BOM

### DOM

DOM：文档对象模型。用于将`标记语言(HTML/XML)`包装成对象。包括内部的内容：`标签、标签属性、文本`。

​	     DOM并不是一个具体的解析技术，而是一个理论。技术叫其他名字。

文档：HTML、XML等

对象：封装了属性和行为的实例，能被直接调用。

模型：都具有的共同特性。

### DOM树

![](E:\BaiduNetdiskDownload\学习资料\笔记\img\QQ图片20230216192532.png)

DOM解析将会按照层级的方式将标签体现标签之间的关系，形成一个树状结构。

### DHTML

动态HTML，指动态的网页。由`HTML、CSS、DOM、JS`结合而成，目的的规范网页，要求以上结构都要出现在一张网页当中，不能通过外部导入的方式编写网页。目的是为了其他用户在使用网页的时候不需要额为导入其他文件。

HTML：网页的框架

CSS：网页的样式

DOM：封装对象，便于操作属性和行为。

JS：进行逻辑操作，定义网页的动态效果。

### BOM

BOM：浏览器对象模型。用于操作浏览器各个对象，使开发者便捷等待操作浏览器。



#### window 窗口对象

浏览器对象对应的就是window窗口对象。

window 对象表示打开的窗口

window 对象使`JS`中的顶层对象

window 对象无需创建，在`<body>`出现时就会被自动创建。



##### 方法

```
alert ();								// 在浏览器弹出一个提示框
演示：alert(100)/ alert("成功！")

confirm();								// 在浏览器弹出一个带确认、取消的对话框
演示： function textConfirm() {
            var a = confirm("你确定要删除吗");
            if (a) {
                alert("删除成功");
            } else {
                alert("取消成功");
            }
        }

prompt();								// 在浏览器弹出一个带输入框的提示框
演示：function textPrompt() {
            var vrr = prompt("请输入金额", 100);
            alert(vrr);
        }
        
open();									// 打开一个新的窗口，移动到新的窗口。
close();								// 关闭新的窗口（打开谁，关闭谁）
演示：var to;
        function textOpen() {
            to = open("https://bilibili.com/", "_blank");
        }
		
        function textClose() {
            to.close();
        }
如果打开两个窗口，第一个窗口的对象被新的窗口覆盖。所以，只能关闭最新打开的窗口。
打开的方式： _self: 本窗口  _blank: 新窗口（默认）

```



##### 定时器相关方法

```
一次定时器：
setTimeout([执行事件], [毫秒数])
clearTimeout(): 清除定时器

演示：
        var st;
        function textTimeout() {
            st = setTimeout("textOpen()", 3000);
        }

        function textClear() {
            window.clearTimeout(st)
        }

循环定时器：
setInterval([事件], [毫秒数])
clearInterval(): 清除定时器

演示：	  
	    var ti;
        function textInterval() {
            ti = setInterval("textOpen()", 3000);
        }

        function textCleatIn() {
            window.clearInterval(ti);
        }
```



#### 事件

#####鼠标点击相关：

​		onclick 		在用户用鼠标左键单击对象时触发。 

​		ondblclick 	当用户双击对象时触发。 

​		onmousedown 当用户用任何鼠标按钮单击对象时触发。 

​		onmouseup 	当用户在鼠标位于对象之上时释放鼠标按钮时触发。 

 

#####鼠标移动相关：

​		onmouseout  当用户将鼠标指针移出对象边界时触发。 

​		onmousemove 当用户将鼠标划过对象时触发。 

 

#####焦点相关的：

​		onblur 		在对象失去输入焦点时触发。 

​		onfocus 		当对象获得焦点时触发。

 

#####按键相关的：

​		onkeydown 	当用户按下键盘按键时触发。 

​		onkeyup 	当用户释放键盘按键时触发。 

​		onkeypress 	当用户按下字面键时触发。 

​	

#####其他：

​		onchange 	当对象或选中区的内容改变时触发。 

​		onload 		在浏览器完成对象的装载后立即触发。 

​		onsubmit 	当表单将要被提交时触发。 



#####例子

```
<button type="button" value="" onclick="事件（函数）">演示alert</button>

表示单击此按钮时执行事件

<button type="button" value="" ondblclick="事件（函数）">演示alert</button>

表示双击此按钮时执行事件
```

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>轮播图</title>
    <style>
        div {
        // 对齐方式-居中
            text-align: center;
        }
    </style>
    
    <script>
        var a = 1;
        function bdd() {
            a++;
            if (a > 3) {
                a = 1;
            }
            // 获取ID对应节点的对象，在后面的DOM方法会讲到
            var addd = document.getElementById("add");
            // 修改对象中的属性，使用了字符串拼接
            addd.src = "../../img/0" + a + ".jpg";
        }

        var ti;
        function textInterval() {
            ti = setInterval("bdd()", 1000);
        }
        
		// 每次页面加载的时候都会启动这个函数（自启动）。
        textInterval();
    </script>
</head>

<body>
    <div>
        <img id="add" src="../../img/01.jpg" alt="抱歉，无法显示图片" width="500px" height="200px">
    </div>
</body>

</html>
```



### windon属性

了解

#### navig

#### location

####history

#### screen



### document属性

要想操作页面产生动态效果，就要对DOM树中的节点进行操作（增、删、改）。所以，在操作之前就必须要获取节点。

```
当前节点对象.nodeName		// 获取节点名称

当前节点对象.nodeType		// 获取节点类型 1 -- 元素节点 2 -- 属性节点

当前节点对象.nodeValue	// 获取节点值
```



#### 方法

##### innerText\innerHTML 

获取/修改 元素内部的值。

````
var x = 当前节点对象.innerText;				// 获取纯文本
当前节点对象.innerText = "哔哩哔哩"			 // 修改文本

var x = 当前节点对象.innerHTML;				// 获取样式文本
当前对象节点.innerHTML = "<span syle="color: aquamarine">哔哩哔哩</span>"
										  // 修改文本样式
<head>										  
    <script>
        function sy() {
            var a = document.getElementById("sp1");

            var b = a.innerText;
            alert(b);					// 输出哔哩哔哩

            var c = a.innerHTML;
            alert(c);					// 输出
            							<span style="color: aquamarine;">哔哩哔哩</span>
        }

    </script>
</head>

<body>
    <div id="sp1">
        <span style="color: aquamarine;">哔哩哔哩</span>
    </div>
    <button type="submit" onclick="sy()">点我</button>
</body>
````

两个方法之间的区别：一个浏览器能解析样式，一个浏览器不解析样式。



####常规方法

##### 通过ID属性获取节点

```
var arr = getElementById("节点ID");				
```

获取的对象用一个变量储存起来（ID唯一，所以不用数组），之后调用对应函数对其操作。比如：

```
arr.src = "../indn.js"					// 修改节点标签中的src属性
```



##### 通过name属性获取节点

```
var arr = getElementsByName("节点name");
```

由于获取的节点不止一个（name属性的不唯一，所以用数组）。



##### 通过标签名获取节点

```
var arr = getElementsByTagName("标签名")；
```

与name属性获取一样，节点名有多个，所以使用数组。



#### 通过节点关系获取

#####  通过节点关系获取父节点

```
var arr = 当前节点对象.parentNode();
```

在DOM树中，显示每个节点的父节点只有一个，所以获取的是一个对象。



##### 通过节点关系获取子节点

````
var arr = 当前节点对象.childNodes();
````

子节点有多个，所以获取的是一个对象数组。但此函数不能忽略标签之间的空白元素，导致不能正常遍历数组。

推荐：

````
var arr = 当前节点对象.children();
````



##### 通过节点关系获取兄弟节点

上一个兄弟节点

```
var arr = 当前节点对象.previousSibling();
```

上一个相邻的兄弟节点只有一个，所以获取的是一个对象。但此函数不能忽略空白元素。

推荐：

```
var arr = 当前节点对象.previousElementSibling();
```



下一个兄弟节点

```
var arr = 当前节点对象.nextSibling();
```

同上述，不推荐

推荐：

```
var arr = 当前节点对象.nextElementSibling();
```

































































