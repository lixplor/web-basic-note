# HTML 5 新input特性


## 新表单input类型

* 新input类型
    - `color`: 颜色选择器
    - `date`: 日期选择器
    - `datetime`: 日期时间选择器
    - `datetime-local`: 本地日期时间选择器
    - `email`: 可验证email的输入框
    - `month`: 选择月份
    - `number`: 仅能输入数字的输入框
        - `max`: 允许输入的最大值
        - `min`: 允许输入的最小值
        - `pattern`: 规定用于验证输入字段的模式
        - `required`: 规定输入字段是必须的
        - `step`: 规定输入字段的合法数字间隔
    - `range`: 滑块, 设置指定范围的数值
    - `search`: 搜索输入框
    - `tel`: 电话号码输入框
    - `time`: 时间输入框
    - `url`: 可验证url的值
    - `week`: 周和年选择框
* 新表单元素
    - `<datalist>`: 规定输入域的选项列表
    - `<keygen>`: 用于表单的密钥对生成器字段
    - `<output>`: 用于不同类型的输出
* 新表单属性
    - `<form>`新属性:
        - `autocomplete`: 自动完成
        - `novalidate`: 在提交表单时不验证form或input域
    - `<input>`新属性
        - `autocomplete`: 自动完成
        - `autofocus`: 自动获取焦点
        - `form`: 定义输入域所属的一个或多个表单
        - `formaction`: 描述表单提交的URL地址
        - `formenctype`: 描述了表单提交到服务器的数据编码
        - `formmethod`: 定义表单的提交方式
        - `formnovalidate`: 描述input元素在表单提交时不验证
        - `formtarget`: 指定一个名称或关键字指明表单提交数据接收后的显示
        - `height`和`width`: 指定input image类型的高度和宽度
        - `list`: 定义输入框的选项列表
        - `min`和`max`: 指定最小最大值
        - `multiple`: 定义input中可选择多个值
        - `pattern`: 使用正则表达式验证输入框
        - `placeholder`: 占位提示
        - `required`: 定义必须在提交之前填写输入域
        - `step`: 定义输入域的数字间隔
