# CSS 3

* 边框
    - `border-radius`: 边框圆角
        - 长度, 顺序左上, 右上, 右下, 左下
    - `border-top-left-radius`: 边框左上圆角
    - `border-top-right-radius`: 边框右上圆角
    - `border-bottom-right-radius`: 边框右下圆角
    - `border-bottom-left-radius`: 边框左下圆角
    - `box-shadow`: 盒子阴影
        - h-shadow: 必须, 水平阴影位置, 允许负值
        - v-shadow: 必须, 垂直阴影位置, 允许负值
        - blur: 可选, 模糊距离
        - spread: 可选, 阴影大小
        - color: 可选, 阴影颜色
        - inset: 可选, 内侧阴影 
    - `border-image`: 边框图像
        - src: 图像路径
        - slice: 图像边界向内偏移
        - width: 图像边界宽度
        - outset: 指定在边框外部绘制border-image-area的量
        - repeat: 图像边界是否有相应属性
            - `stretch`: 默认, 拉伸图像来填充区域
            - `repeat`: 平铺填充
            - `round`: 类似repeat, 如无法完整平铺所有图像, 则对图像缩放以适应区域
            - `space`: 类似repeat, 如无法完整平铺所有图像, 则扩展空间会分布在图像周围
* 背景
    - `background-image`: 背景图
        - url, 可以有多个url, 用`,`逗号分隔
    - `background-size`: 背景图的大小
        - 宽
        - 高
    - `background-origin`: 背景图的位置区域
        - `border-box`: 边界框
        - `padding-box`: 填充框
        - `content-box`: 内容框
    - `background-clip`: 指定背景绘制区域
        - `border-box`: 默认, 绘制在边界框内
        - `padding-box`: 绘制在填充框内
        - `content-box`: 绘制在内容框内 
* 渐变
    - `linear-gradient`: 线性渐变
        - direction
            - `to left`
            - `to right`
            - `to top left`
            - `to bottom right`
        - angle
            - xxdeg
        - color-stop1
        - color-stop2
        - ...
    - `radial-gradient`: 径向渐变
        - shape
            - `circlr`: 圆形
            - `ellipse`: 椭圆形
        - shape-size
            - `closest-side`
            - `farthest-side`
            - `closest-corner`
            - `farthest-corner`
        - start-color
        - ...
        - last-color
    - `repeating-linear-gradient`: 重复线性渐变
    - `repeating-radial-gradient`: 重负径向渐变


