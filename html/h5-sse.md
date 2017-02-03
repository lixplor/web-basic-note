# HTML 5 Server-Sent Event

* `Server-Sent Event`: h5服务器发送事件, 允许网页获取来自服务器的更新
* sse是网页自动获取来自服务器的更新, 它是单向的


## 相关方法

* 检测浏览器是否支持: `if(typeof(EventSource) !== "undefined")`
* `new EventSource(页面)`: 创建事件源对象
* `eventSource.onopen=回调`: 当通往服务器的链接被打开时回调
* `eventSource.onmessage=回调`: 当接收到消息时回调
* `eventSource.onerror=回调`: 当发生错误的回调


```html
var source=new EventSource("demo_sse.php");
source.onmessage=function(event) {
    document.getElementById("result").innerHTML+=event.data + "<br>";
};
```
