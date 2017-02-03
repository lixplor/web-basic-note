# HTML 5 Web存储

* HTML5提供了web存储, 比cookie更好
* 使用key-value方式存储
* web网页的数据只允许该网页访问使用


## localStorage和sessionStorage

获取浏览器支持的存储类型:
* `if(typeof(Storage) !== "undefined")`

客户端存储数据的2个对象:
* `localStorage`: 没有时间限制的数据存储
    - `localStorage.key = value`: 保存数据
    - `localStorage.key`: 获取数据
    - `localStorage.setItem(key, value)`: 保存数据
    - `localStorage.getItem(key)`: 读取数据
    - `localStorage.removeItem(key)`: 删除指定数据
    - `localStorage.clear()`: 删除所有数据
    - `localStorage.key(index)`: 获取每个索引的key
* `sessionStorage`: 针对一个session的数据存储
    - api同localStorage

