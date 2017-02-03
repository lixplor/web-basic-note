# HTML 5 MathML

* `MathML`是数学标记语言, 基于XML标准, 用于书写数学符号和公式
* `<math></math>`标签用于嵌入MathML

```html
<!DOCTYPE html>
<html>
   <head>
      <meta charset="UTF-8">
      <title>菜鸟教程(runoob.com)</title>
   </head>
   <body>
      <math xmlns="http://www.w3.org/1998/Math/MathML">
         <mrow>
            <msup><mi>a</mi><mn>2</mn></msup>
            <mo>+</mo>
            <msup><mi>b</mi><mn>2</mn></msup>
            <mo>=</mo>
            <msup><mi>c</mi><mn>2</mn></msup>
         </mrow>
      </math>
   </body>
</html> 
```
