### nodejs操作数据库

> ### 手册地址
```
https://www.npmjs.com/package/mysql
```

> ### 安装mysql
```
npm i mysql
```

```js
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'me',
  password : 'secret',
  database : 'my_db'
});

connection.connect();

connection.query('mysql语句', function (error, results, fields) {
  if (error) throw error;
  console.log('The solution is: ', results[0].solution);
});


connection.end();
```


