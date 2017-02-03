# HTML 5 Web SQL数据库

* Web SQL数据库并不是H5规范的一部分, 而是独立的规范


## 核心方法

* `openDatabase(数据库名称, 版本号, 描述文本, 数据库大小, 创建结果回调)`: 打开现有数据库, 如果数据库不存在, 则创建新数据库并打开
* `transaction(回调)`: 事务
* `executeSql(sql语句)`: 执行SQL查询
    - 增加: `executeSql('INSERT INTO LOGS (id, log) VALUES (1, "菜鸟教程")');`
    - 删除: `executeSql('DELETE FROM LOGS  WHERE id=1');`
    - 修改: `executeSql('UPDATE LOGS SET log=\'www.w3cschool.cc\' WHERE id=2');`
    - 查询: `executeSql('SELECT * FROM LOGS', [], 查询结果回调, null);`


```html
<!DOCTYPE HTML>
<html>
   <head>
      <meta charset="UTF-8">  
      <script type="text/javascript">
      
         var db = openDatabase('mydb', '1.0', 'Test DB', 2 * 1024 * 1024);
         var msg;
         
         db.transaction(function (tx) {
            tx.executeSql('CREATE TABLE IF NOT EXISTS LOGS (id unique, log)');
            tx.executeSql('INSERT INTO LOGS (id, log) VALUES (1, "菜鸟教程")');
            tx.executeSql('INSERT INTO LOGS (id, log) VALUES (2, "www.runoob.com")');
            msg = '<p>数据表已创建，且插入了两条数据。</p>';
            document.querySelector('#status').innerHTML =  msg;
         });

         db.transaction(function (tx) {
              tx.executeSql('DELETE FROM LOGS  WHERE id=1');
              msg = '<p>删除 id 为 1 的记录。</p>';
              document.querySelector('#status').innerHTML =  msg;
         });

         db.transaction(function (tx) {
             tx.executeSql('UPDATE LOGS SET log=\'www.w3cschool.cc\' WHERE id=2');
              msg = '<p>更新 id 为 2 的记录。</p>';
              document.querySelector('#status').innerHTML =  msg;
         });

         db.transaction(function (tx) {
            tx.executeSql('SELECT * FROM LOGS', [], function (tx, results) {
               var len = results.rows.length, i;
               msg = "<p>查询记录条数: " + len + "</p>";
               document.querySelector('#status').innerHTML +=  msg;
               
               for (i = 0; i < len; i++){
                  msg = "<p><b>" + results.rows.item(i).log + "</b></p>";
                  document.querySelector('#status').innerHTML +=  msg;
               }
            }, null);
         });
         
      </script>
      
   </head>
   
   <body>
      <div id="status" name="status">状态信息</div>
   </body>
   
</html>
```
