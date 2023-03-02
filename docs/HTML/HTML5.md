# HTML：5

## 网页结构

```html
<!-- 告诉浏览器当前的文件是一个网页 -->
<!DOCTYPE html>
<!-- 整个网页的根目录 -->
<html lang="en">
<!-- 头标签：声明这个网页的元数据，用来说明数据的数据 -->
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML5网页</title>
</head>
<!-- 网页实体标签 -->
<body>

</body>

</html>
```



## 常用标签

###  字体标签`<font>`

`<font> `标签在 HTML 4 中用于指定字体、字体大小和文本颜色。 

```html
<font face="verdana" color="green" size="2">This is some text!</font>
```

`face`：文本的字体。

`color`：文本的颜色。

`size`：文本字体。



### 标题标签`<h>`

由`<h1>` ~ `<h6>`,数字越大，字体越小。

```html
<h1>这是一个标题</h1>
```

本质是`<font>` + `<b>`。



### 字体加粗标签`<b>`

```html
<b>加粗文本</b>
```



### 居中标签`<center>`

```html
<center>文本被居中了</center>
```



### 文本斜体标签`<i>`

```html
<i>这是一个斜体文本</i>
```



### 水平分割线`<hr>`

```html
<hr>
```



###段落标签`<p>`

```html
<p>这是第一个段落<p>
<p>这是第二个段落<p>
<p>这是第三个段落<p>
```



### 特殊字符

[>>>> 点我跳转](https://www.w3school.com.cn/html/html_entities.asp)


### 列表标签

####`<dl><dt><dd>`

```html
<dl>                
        <dt>上层</dt>
        <dd>下层</dd>
        <dd>下层</dd>
</dl>
```

效果：

​	上层

​		下层

​		下层

`<dd>`标签有缩进效果



#### 有序标签

```html
<ol>
    <li>一</li>
    <li>二</li>
    <li>三</li>
</ol>
```

















































