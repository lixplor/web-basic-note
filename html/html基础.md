# HTML基础


## 语义化



## 注释

```html
<!--注释内容-->

<!--注释
    可以
    换行-->
```


## html元素

* 标题
    - `<h1>`~`<h6>`分别代表6个级别的标题
* 段落
    - `<p></p>`定义段落
* 超链接
    - `<a id="ID" href="链接地址" target="定义链接的文档在何处显示"></a>`
        - `href`: 链接地址
            - `#id`则可以跳转到本页中指定id位置. 如果没有该属性, 则该链接不可以点击
            - `mailto:name@email.com?cc=抄送地址&bcc=暗送地址&subject=邮件标题&body=邮件正文`: 电子邮箱超链接, 点击会打开系统邮件客户端. 空格用`%20`代替以保证链接不会被空格断开
        - `target`: 定义文档在何处显示.
            - `_blank`:在新窗口打开.
            - `_top`: 跳出frame
* 图像
    - `<img src="图像地址" alt="替换文本"/>`
        - `src`: 图像路径
        - `alt`: 替换文本, 当图像无法显示时出现
        - `width`: 图像宽度
        - `height`: 图像高度    
    - `<map>`: 定义图像地图
    - `<area>`: 定义图像地图中的可点击区域
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
* 表格
表格可以嵌套
    - `<table></table>`
        - `colspan`属性: 跨列数量
        - `rowspan`属性: 跨行数量
        - `<caption></caption>`: 表格标题
        - `<colgroup></colgroup>`: 定义表格列的组
            - `<col>`: 定义表格列的属性
        - `<tr></tr>`: 表格行
            - `<th></th>`: 表格头
            - `<td></td>`: 表格数据
        - `<thead></thead>`: 表格页眉
        - `<tbody></tbody>`: 表格主体
        - `<tfoot></tfoot>`: 表格页脚
* 列表
列表可以嵌套
    - `<ul></ul>`: 无序列表
        - 通过css的`list-style-type`来定义序号类型
            - `disc`: 圆点
            - `circle`: 圆圈
            - `square`: 正方形
    - `<ol></ol>`: 有序列表
        - `type`属性: 定义有序列表的序号样式
            - `1`: 数字序号
            - `A`, `a`: 字母序号
            - `I`, `i`: 希腊字母序号
    - `<li></li>`: 列表项目
    - `<dl></dl>: 自定义列表
        - `<dt></dt>`: 列表中的上层条目
        - `<dd></dd>`: 列表中的底层条目
* 块
    - 块级元素: 显示时以新行开始
        - `<div></div>`: 作为容器, 没有特定含义
        - `<hN>`, `<p>`, `<ul>`, `<table>`也是块级元素
    - 内联元素(行内元素): 不会以新行开始显示
        - `<span></span>`: 作为容器, 没有特定含义
        - `<b>`, `<td>`, `<a>`, `<img>`也是内联元素
* 表单
表单是包含`表单元素`的区域, 表单元素是允许用户输入内容的元素
    - `<form></form>`: 表单
        - `action`属性: 提交动作
        - `method`属性: http方法
        - `<input>`: 输入元素, 输入类型由`type`属性定义
            - `type`属性: 定义输入类型
                - `text`: 文本域, 大多数浏览器中默认宽度是20个字符
                - `number`: 数字输入框
                - `password`: 密码字段, 文本不会明文显示
                - `radio`: 单选按钮, `name`属性值相同的归为一组
                - `checkbox`: 复选框, `name`属性值相同的归为一组
                - `submit`: 提交按钮, 将表单内容提交
                - `reset`: 重置按钮, 重置表单数据为默认值
                - `button`: 普通按钮
                - `range`: 滑块
                    - `min`: 最小值
                    - `max`: 最大值
                    - `value`: 默认值
                - `list`: 输入框提示列表数据, 与`<datalist>`元素结合
        - `<datalist></datalist>`: 可下拉的输入框, 选项使用`<option>`定义
        - `<button type="button"></button>`: 按钮, 与input不同之处在于, button内部可以防止内容, 如文本或图像
        - `<select></select>`: 下拉选择框
            - `<optgroup></optgroup>`: 下拉选项分组
                - `label`属性: 分组名
            - `<option></option>`: 选项
                - `value`: 选项值
        - `<output></output>`: 定义计算结果
            - `for`属性: 描述计算中使用的元素与计算结果之间的关系
        - `<textarea></textarea>`: 多行文本域
        - `<fieldset></fieldset>`: 使用边框包裹内部输入元素
            - `<legend></legend>`: fieldset的标题
* 框架
    - `<iframe></iframe>`: 嵌入其他页面
        - `src`属性: 其他页面的url
        - `width`: 框架宽度
        - `height`: 框架高度
        - `frameborder`: 框架边框, 值为0没有边框, 1显示边框


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


<!-- 图像 -->

<img src="demo.png" width="100" height="100"/>

<map name="planetmap">
  <area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
  <area shape="circle" coords="90,58,3" alt="Mercury" href="mercur.htm">
  <area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
</map>

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


<!-- 表格 -->

<table>
  <caption>
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$100</td>
  </tfoot>
</table>


<!-- 列表 -->

<ul>
  <li>无序列表项1</li>
  <li>无序列表项2</li>
<ul>

<ol>
  <li>有序列表项1</li>
  <li>有序列表项2</li>
<ol>

<dl>
  <dt>自定义列表的上层条目</dt>
  <dd>自定义列表的底层条目</dd>
</dl>


<!-- 表单 -->

<form>
  文本输入框<input type="text">
  数字输入框<input type="number">
  密码输入框<input type="password">
  <input type="range" min="-50" max="100" value="50">
  <input type="radio" name="sex" value="male">单选按钮选项Male
  <input type="radio" name="sex" value="female">单选按钮选项Female
  <input type="checkbox" name="car" value="ford">Ford
  <input type="checkbox" name="car" value="benz">Benz
  <select>
    <option value="1">1</option>
    <option value="2">2</option>
  </select>
  <select>
    <optgroup label="颜色">
      <option value="red">红</option>
      <option value="yellow">黄</option>
    </optgroup>
    <optgroup label="数字">
      <option value="1">1</option>
      <option value="2">2</option>
    </optgroup>
  </select>
  <input list="browsers">
  <datalist id="browsers">
    <option value="IE">
    <option value="FireFox">
  </datalist>
  <fieldset>
    <legend>按钮组</field>
    <input type="button" value="普通按钮">
    <input type="reset" value="重置按钮">
    <input type="submit" value="提交按钮">
  </fieldset>
</form>


<!-- 框架 -->

<iframe src="https:www.baidu.com" frameborder="0"></iframe>
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
    - `name`: 属性名
        - `keywords`: 搜索引擎关键字
        - `description`: 页面描述
        - `author`: 页面作者
    - `http-equiv`: 响应头的键
    - `content`: 响应头的值
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
