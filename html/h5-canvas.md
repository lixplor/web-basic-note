# HTML 5 Canvas

* `<canvas>`标签定义图形, 如图表和其他图像
* `<canvas>`标签只是图形的容器, 必须使用脚本来绘制图形


## 创建画布

* 画布在网页中是一个矩形框, 默认没有边框和内容
* 通常需要制定一个id属性, 以便脚本引用, width和height属性定义画布的大小
* 一个html页面中可以定义多个`<canvas>`元素
* 可以使用css来定义画布样式

```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas>
```

## 使用JS绘制图像

* canvas没有绘图能力, 绘图必须在JS中完成
* 绘图步骤
    - 找到`<canvas>`元素
    - 通过canvas对象获取context对象
    - 使用context对象进行绘制
* canvas以左上角为(0, 0)坐标


```javascript
var canvas = document.getElementById("myCanvas");
var context = canvas.getContext("2d");
context.fillStyle"#FF0000";
context.fillRect(0, 0, 150, 75);  // 从坐标0,0开始绘制宽150高75的矩形
```


## Canvas绘制

* 获取Context对象
    - `canvas.getContext(type);`: 使用canvas对象获取context
        - `type`: 画布类型
            - `"2d"`: 2d平面画布
* 属性设置
    - `context.fillStyle`: 设置用于填充会话的颜色, 渐变, 或模式
    - `context.strokeStyle`: 设置画笔的颜色, 渐变, 或模式
    - `context.shadowColor`: 设置阴影的颜色
    - `context.shadowBlur`: 设置阴影的模糊级别
    - `context.shadowOffsetX`: 设置阴影的水平偏移
    - `context.shadowOffsetY`: 设置阴影的垂直偏移
    - `context.lineCap`: 设置线条的结束端点样式
    - `context.lineJoin`: 设置两条线相交时, 拐角的类型
    - `context.lineWidth`: 设置线条宽度
    - `context.meterLimit`: 设置最大斜接长度, 即超过该值的miter会变为bevel
* 绘制图形
    - `context.moveTo(x, y)`: 移动到(x, y)点
    - `context.lineTo(x, y)`: 使用线段连接当前点到(x, y)点
    - `context.beginPath()`: 开始Path
    - `context.closePath()`: 结束Path
    - `context.arc(x, y, r, start, stop)`: 绘制弧形
    - `context.arcTo(x1, y1, x2, y2, r)`: 绘制弧线
    - `context.quadraticCurveTo(cpx, cpy, x, y)`: 绘制二阶贝塞尔曲线
    - `context.bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)`: 绘制三阶贝塞尔曲线
    - `context.stroke()`: 绘制线条
    - `context.fill()`: 填充当前绘图或路径
    - `context.rect()`: 创建矩形
    - `context.strokeRect(x, y, x1, y1)`: 创建空心矩形
    - `context.fillRect(x, y, x1, y1)`: 创建实心矩形
    - `context.clearRect(x, y x1, y1)`: 清除指定矩形区域的像素
    - `context.clip()`: 从画布剪切任意形状和尺寸的区域
    - `context.isPintInPath(x, y)`: 指定点是否位于路径中
* 绘制文字
    - `context.font`属性: 定义字体
    - `context.textAlign`: 设置文本对齐方式
    - `context.textBaseline`: 设置绘制文本时使用的文本基线
    - `context.fillText(text, x, y)`: 绘制实心文本
    - `context.strokeText(text, x, y)`: 绘制空心文本
    - `context.measureText(text)`: 获取指定文本宽度的对象
* 绘制图像
    - `context.drawImage(image, x, y)`: 将图像绘制到画布上, 以(x, y)为左上角, image为image元素
* 渐变
    - `context.createLinearGradient(x, y, x1, y1)`: 创建线条渐变
    - `context.createRadialGradient(x, y, r, x1, y1, r1)`: 创建圆渐变
    - `gradient.addColorStop(f, colorStr)`: 设置起始或结束的颜色
    - `context.fillStyle = gradient;`: 设置渐变到context
* 转换
    - `context.scale(scalewidth, scaleheight)`: 缩放
    - `context.rotate(angle)`: 旋转, 以弧度计算
    - `context.translate(x, y)`: 平移指定像素
    - `context.transform(a, b, c, d, e, f)`: 变换当前画布的矩阵
    - `context.setTransform(a, b, c, d, e, f)`: 将当前转换重置为单位矩阵, 然后执行transform()
* 像素操作
    - `context.width`: 返回ImageData对象的宽度
    - `context.height`: 返回ImageData对象高度
    - `context.data`: 返回一个对象, 包含指定的ImageData对象的图像数据
    - `context.createImageData()`: 创建新的ImageData对象
    - `context.getImageData()`: 获取ImageData对象, 该独享为画布上指定的矩形复制像素数据
    - `context.putImageData(imgData, x, y, dirtyX, dirtyY, dirtyWidth, dirtyHeight)`: 将图像数据从指定的ImageData对象放回画布上
* 合成
    - `context.globalAlpha`: 设置画布当前透明度
    - `context.globalCompositionOperation`: 设置新图像如何绘制到已有图像上
* 其他
    - `save()`: 保存当前画布环境
    - `restore()`: 恢复保存过的路径状态和属性
    - `createEvent()`
    - `getContext()`
    - `toDataURL()`


## 示例

```html
<!-- 创建canvas -->
<canvas id="c" width="200" height="200"></canvas>
```

```javascript
// 获取canvas和context对象
var canvas = document.getElementById("c");
var context = canvas.getContext("2d");

// 绘制线段
context.moveTo(0, 0,);
context.lineTo(80, 80);
context.stroke();

// 绘制实心矩形
context.fillStyle("#000000");
context.fillRect(0, 0, 50, 90);

// 绘制空心矩形
context.fillStyle("#000000");
context.strokeRect(0, 0, 50, 50);

// 绘制实心圆
context.beginPath();
context.arc(95, 50, 40, 2*Math.PI);
context.fill();

// 绘制空心圆
context.beginPath();
context.arc(95, 50, 40, 0, 2*Math.PI);
context.stroke();

// 绘制实心文本
context.font = "30px Arial";
context.fillText("hello", 4, 10);

// 绘制空心文本
context.font = "20px Arial";
context.strokeText("world", 5, 40);

// 绘制线性渐变
var gradient = context.createLinearGradient(0, 0, 200, 0);
gradient.addColorStop(0, "red");
gradient.addColorStop(1, "white");
context.fillStyle = gradient;
context.fillRect(10, 10, 50, 50);

// 绘制圆渐变
var gradient = context.createRadialGradient(75, 50, 5, 90, 60, 100);
gradient.addColorStop(0, "red");
gradient.addColorStop(1, "white");
context.fillStyle = gradient;
context.fillRect(10, 10, 150, 80);

// 绘制图像
var img = document.getElementById("photo");
context.drawImage(img, 10, 10);
```
