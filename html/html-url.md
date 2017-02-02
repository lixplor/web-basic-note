# HTML URL

* URL: 统一资源定位器, 是一个网页地址, 可以由域名或IP地址构成


## URL

* 浏览器通过URL从web服务器请求页面
* URL格式: `scheme://host.domain:port/path/filename`
    - `scheme`: 定义Internet服务类型, 常见的是http
    - `host`: 定义域主机(http的默认主机是www)
    - `domain`: 定义Internet域名, 如baidu.com
    - `:port`: 定义主机端口(默认端口为80)
    - `path`: 定义服务器上的路径
    - `filename`: 定义文档/资源的名称


## 常见URL scheme

* `http`: 超文本传输协议   
以http://开头, 不加密
* `https`: 安全超文本传输协议   
安全网页, 加密所有信息交换
* `ftp`: 文件传输协议    
用于将文件下载或上传至网站
* `file`    
计算机上的文件



## URL字符编码

* URL只能使用ASCII字符串
* 如果包含ASCII之外的字符串, 则需要转换为有效的ASCII字符, URL编码使用`%`跟随两位十六进制数来替换非ASCII字符
* URL不能包含空格, 通常使用`+`来替换空格


