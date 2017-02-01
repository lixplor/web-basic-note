# HTML简介

* `HTML`是`HyperText Markup Language`的缩写, 超文本标记语言
* html文档后缀有以下两种, 没有区别
    - `.html`
    - `.htm`
* html不是编程语言, 而是一种`标记`语言

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

## html元素

* html元素和html标签通常表示相同的意思, 但严格来讲, 一个html元素包含了开始标签和结束标签


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
