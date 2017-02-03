# HTML 5 Websocket

* websocket是在单个TCP链接上进行全双工通讯的协议
* 浏览器通过JS向服务器发出建立websocket链接的请求
* 创建WebSocket连接的HTTP请求与通常的请求不同, 包含附加头信息

## websocket

* 判断浏览器是否支持: `if("WebSocket" in window)`
* `new WebSocket(url, [protocol])`: 创建websocket对象
* 属性
    - `socket.readyState`: 只读, 连接状态
        - `0`: 连接尚未建立
        - `1`: 连接已经建立, 可以通信
        - `2`: 连接正在进行关闭
        - `3`: 连接已经关闭, 或连接不能打开
    - `socket.bufferedAmount`: 只读, 已被send()方法加入队列中等待传输但还没有发出的UTF-8文本字节数
* 事件
    - `socket.onopen`: 连接建立时触发
    - `socket.onmessage`: 客户端接收服务端数据时触发
    - `socket.onerror`: 通信发生错误时触发
    - `socket.onclose`: 连接关闭时触发
* 方法
    - `socket.send()`: 发送数据
    - `socket.close()`: 关闭连接 

```html
<!DOCTYPE HTML>
<html>
   <head>
   <meta charset="utf-8">
   <title>菜鸟教程(runoob.com)</title>
	
      <script type="text/javascript">
         function WebSocketTest()
         {
            if ("WebSocket" in window)
            {
               alert("您的浏览器支持 WebSocket!");
               
               // 打开一个 web socket
               var ws = new WebSocket("ws://localhost:9998/echo");
				
               ws.onopen = function()
               {
                  // Web Socket 已连接上，使用 send() 方法发送数据
                  ws.send("发送数据");
                  alert("数据发送中...");
               };
				
               ws.onmessage = function (evt) 
               { 
                  var received_msg = evt.data;
                  alert("数据已接收...");
               };
				
               ws.onclose = function()
               { 
                  // 关闭 websocket
                  alert("连接已关闭..."); 
               };
            }
            
            else
            {
               // 浏览器不支持 WebSocket
               alert("您的浏览器不支持 WebSocket!");
            }
         }
      </script>
		
   </head>
   <body>
   
      <div id="sse">
         <a href="javascript:WebSocketTest()">运行 WebSocket</a>
      </div>
      
   </body>
</html>
```
