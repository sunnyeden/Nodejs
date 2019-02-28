### node内置模块

> ### os系统模块
```js
var os = require("os");

换行：os.EOL
主机名：os.hostname();
操作系统：os.type();
操作平台：os.platform();
内存总量(字节)：os.totalmem();
空闲内存(字节)：os.freemem();
```


> ### path路径模块
```js
var path = require("path");

var filepath ="https://www.jiangliang738.cn/wechat/wechatpay.php";

文件名：path.basename(filepath);
目录名：path.dirname(filepath);
```

> ### URL模块
```js
var url = require("url");

var data ="https://www.jiangliang738.cn?name=eden&age=24";

url.parse(data);

变为对象：$info = url.parse(data,true);
获取参数：$info.query
```

> ### fs文件模块
```js
var fs = require("fs");

fs.writeFile(路径及文件名,"utf8",function(err,data){
		if(!err){
			console.log(data);
		}
	});
```

> ### http模块
```js
var http = require("http");

#创建web服务器
var server = http.createServer();

#监听请求
server.on('request',function(req,res){
		console.log("收到请求"+req.url);
		res.setHeader("Content-Type","text/html;charset=utf-8");
		res.write("你好 nodejs");
		res.end();
	})

#启动服务
server.listen(8080,function(){
		console.log("服务启动成功");
	})
```

> ### http模块请求头

* request.headers  获取请求头

* request.rawHeaders  获取请求头信息

* request.httpVersion  获取http版本

* request.method  获取请求方式

* request.url  获取请求地址


> ### http模块响应头
```js
res.writeHeader(404,"Not Found",{
	"Content-Type" : "text/html;charset=utf7"
})
```







