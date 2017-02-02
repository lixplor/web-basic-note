# HTML简介

* `HTML`是`HyperText Markup Language`的缩写, 超文本标记语言
* html文档后缀有以下两种, 没有区别
    - `.html`
    - `.htm`
* html不是编程语言, 而是一种`标记`语言
* html不区分大小写, 推荐使用小写标签, 以后会强制使用小写
* html中多有连续的空格或空行都会被算作一个空格

## html结构

* 只有`<body>`部分会显示在浏览器中

```html
<!DOCTYPE html>                // 声明为HTML5
<html>                         // html页面根元素
<head>                         // 包含文档头部信息等
  <meta charset="utf-8">       // 元数据, 声明字符编码集
  <title>标题</title>          // 文档的标题
</head>
<body>                         // 包含可见的页面内容
  <h1>标题</h1>                
  <p>段落</p>
</body>
</html>
```

## html标签

* html标签是由尖括号包裹的关键词, 如`<html>`
* html标签通常成对出现, 分别为`开始标签`和`结束标签`, 如`<b></b>`
    - 也被称为`开放标签`和`闭合标签`
* 自封闭标签`<element/>`等同于`<element></element>`
* HTML5中, 自闭合标签没有结束标签, 也就是说不需要写结束时的`/`反斜杠: 如`<meta charset="utf-8">`

## html元素

* html元素和html标签通常表示相同的意思, 但严格来讲, 一个html元素包含了开始标签和结束标签


## html属性

* html元素可以设置属性, 属性可以在元素中添加附加信息, 属性一般描述与开始标签, 属性总是以名称=值的方式出现
* 属性值应该始终被包括在`""`内, 一般使用双引号, 单引号也可以使用, 但必须成对出现
* 属性名和属性值对大小写不敏感, 但推荐使用小写, 以后强制要求使用小写

## web浏览器

* web浏览器用于读取html文件, 并将其作为网页显示
* web浏览器并不直接显示html标签, 但可以使用标签来决定如何展现html页面


## html版本

|版本|发布时间|
|----|--------|
|HTML|1991|
|HTML+|1993|
|HTML 2.0|1995|
|HTML 3.2|1997|
|HTML 4.01|1999|
|XHTML 1.0|2000|
|HTML5|2012|
|XHTML5|2013|


## DOCTYPE声明

* DOCTYPE声明不区分大小写

```html
// html5
<!DOCTYPE html>

// html 4.01
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">

// xhtml 1.0
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```


## HTML样式-CSS

* 3种方式将CSS添加到HTML中
    - 内联样式: 在html元素中增加`style`属性
    - 内部样式表: 在html文档头部`<head>`中增加`<style>`元素来包含CSS
    - 外部引用: 在html文档头部`<head>`中增加`<link>`, 加载外部CSS文件

```html
// 内联样式
<p style="color:blue;margin-left:20px;">This is a paragraph.</p>

// 内部样式表
<head>
  <style type="text/css">
    body {
      color:#000;
    }
  </style>
</head>

// 外部样式表
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
```
