# HTML基础


## 语义化

## 元素分类

* 块级元素
默认独占一行
* 内联元素(行内元素)
可以在同一行中显示多个内联元素

## 注释

```html
<!--注释内容-->

<!--注释
    可以
    换行-->
```

## html元素

* 标题
`<h1>`~`<h6>`分别代表6个级别的标题
* 段落
`<p></p>`定义段落
* 超链接
`<a id="ID" href="链接地址" target="定义链接的文档在何处显示"></a>`
    - `href`: 链接地址
        - `#id`则可以跳转到本页中指定id位置. 如果没有该属性, 则该链接不可以点击
        - `mailto:name@email.com?cc=抄送地址&bcc=暗送地址&subject=邮件标题&body=邮件正文`: 电子邮箱超链接, 点击会打开系统邮件客户端. 空格用`%20`代替以保证链接不会被空格断开
    - `target`: 定义文档在何处显示. 
        - `_blank`:在新窗口打开. 
        - `_top`: 跳出frame
* 图像
`<img />`
* 水平线
`<hr/>`
* 换行
`<br/>`
* 文本格式化
    - 加粗文本
    `<b></b>`
    `<strong></strong>`
    - 斜体文本
    `<i></i>`
    `<em></em>`
    - 放大文本
    `<big></big>`
    - 缩小文本
    `<small></small>`
    - 预格式文本, 不会将多个空格或换行转换为一个空格
    `<pre></pre>`
    - 代码文本(计算机输出)
    `<code></code>`
    - 计算机代码样本
    `<samp></samp>`
    - 计算机变量
    `<var></var>`
    - 键盘输入
    `<kbd></kbd>`
    - 打字机文本
    `<tt></tt>`
    - 下标文本
    `<sub></sub>`
    - 上标文本
    `<sup></sup>`
    - 地址文本
    `<address></address>`
    - 缩略词文本, 某些浏览器中, 鼠标放在缩略词上可以显示完整单词
    `<abbr title="完整文本">缩略文本</abbr>`
    - 首字母缩写, 同上
    `<acroym title="完整文本">缩略文本</acronym>`
    - 文字方向, 方向值为`rtl`(从右到左), `ltr`(从左到右)
    `<bdo dir="方向值"></bdo>`
    - 短引用
    `<q></q>`
    - 长引用
    `<blockquote></blockquote>
    - 引证
    `<cite></cite>`
    - 定义文本
    `<dfn></dfn>`
    - 删除文本
    `<del></del>`
    - 插入文本
    `<ins></ins>`



```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>

<p>段落</p>

<a id="tips" target="_blank" href="https://www.baidu.com">超链接</a>

<a id="title1">不可点击的超链接, 没有href属性, 但可以使用锚点跳过来</a>

<a href="#title1">跳转到title1的超链接</a>

<a href="mailto:someone@email.com?cc=personA@email.com&bcc=personB@email.com&subject=Hello%20There&body=Hi%20all,%20You're%20good!">发送邮件</a>

图像<img src="demo.png" width="100" height="100"/>

水平线<hr/>

换行<br/>


<!-- 文本格式化 -->

<b>加粗文本, 格式化方式</b>
<strong>加粗文本, 语义化方式</strong>

<i>斜体文本, 格式化方式</i>
<em>斜体文本, 语义化方式</em>

<big>放大文本</big>

<small>缩小文本</small>

<pre>预格式文本, 不会转换     多余的        空格</pre>

<code>代码文本: var result = sum(1, 2);</code>

<samp>计算机代码样本</samp>

<var>计算机变量</var>

<kbd>键盘输入文本</kbd>

<tt>打字机文本</tt>

<sub>上标文本</sub>

<sup>下标文本</sup>

<address>地址信息文本</address>

<abbr title="etcerera">etc.</abbr>

<acronym title="World Wide Web">WWW</acronym>

<bdo dir="rtl">从右往左念</bdo>

<q>短引用文本</q>

<blockquote>长引用文本</blockquote>

<cite>引证文本</cite>

<dfn>定义</dfn>

<del>删除文本</del>

<ins>插入文本</ins>

```

## head标签

* `<head></head>`: 包含所有的头部标签元素, 可以在其中插入script, css, meta
* `<title></title>`: 必须有. 定义不同文档的标题
    - 浏览器工具栏标题
    - 收藏夹标题
    - 搜索引擎结果页面的标题
* `<base>`: HTML文档中所有超链接标签的默认链接
* `<link>`: 定义文档与外部资源之间的联系
* `<style></style>`: 定义HTML文档的样式文件引用地址
* `<meta>`: 定义基本元数据
    - `charset`: 页面字符集
    - `name': 属性名
        - `keywords`: 搜索引擎关键字
        - `description`: 页面描述
        - `author`: 页面作者
* `<script></script>`: 定义脚本文件
    


```html
// title标签
<!DOCTYPE html>
<html>
<head> 
  <meta charset="utf-8"> 
  <title>文档标题</title>
</head>
<body>
  文档内容......
</body>
</html>


// base标签
<head>
  <base href="http://www.runoob.com/images/" target="_blank">
</head>
<body>
  <img src="logo.png" />  // 自动使用base标签中的地址
</body>


// link标签
<head>
  <link rel="stylesheet" type="text/css" href="mystyle.css">
</head>


// style标签
<head>
  <style type="text/css">
    body {
      background-color:yellow;
    }
  </style>
</head>


// meta标签
<meta name="keywords" content="搜索引擎关键字, 用逗号分隔">
<meta name="description" content="页面内容描述">
<meta name="author" content="网页作者信息">
<meta http-equiv="refresh" content="30">每30秒刷新页面


// script标签
<script type="text/javascript">
  var js = runJs();
</script> 
