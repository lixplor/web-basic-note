# HTML 5 Web Worker

* web worker是运行在后台的JS, 不影响页面性能
* 由于web worker位于外部文件中, 所以无法访问DOM中的`window`, `document`. `parent`对象


## Web Worker

* 检查浏览器是否支持: `if(typeof(Worker) !== "undefined")`
* `new Worker(脚本文件)`: 创建Web worker对象
* `worker.terminate()`: 终止web worker
* `worker.onmessage=回调`: 添加消息监听器


```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
 
<p>计数： <output id="result"></output></p>
<button onclick="startWorker()">开始工作</button> 
<button onclick="stopWorker()">停止工作</button>
 
<p><strong>注意：</strong> Internet Explorer 9 及更早 IE 版本浏览器不支持 Web Workers.</p>
 
<script>
var w;
 
function startWorker() {
    if(typeof(Worker) !== "undefined") {
        if(typeof(w) == "undefined") {
            w = new Worker("demo_workers.js");
        }
        w.onmessage = function(event) {
            document.getElementById("result").innerHTML = event.data;
        };
    } else {
        document.getElementById("result").innerHTML = "抱歉，你的浏览器不支持 Web Workers...";
    }
}
 
function stopWorker() 
{ 
    w.terminate();
    w = undefined;
}
</script>
 
</body>
</html>
```
