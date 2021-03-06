### Express框架

**初始化文件夹**
```
npm init -y
```

**安装express框架**
```
npm install express
```

**基本使用**
```js
#引入模块
var express = require("express");

#创建服务器
var app = express();

#监听请求
app.get("/",function(req,res){
		//end() 响应字符串（乱码）
		//send() 响应字符串（自动识别）
		//render() 响应字符串（自动识别，指定文件中的字符串）
	});

#启动服务
app.listen(8080,function(){
		console.log("启动成功");
	})
```

**配置模板引擎(因为end和send无法解析模板)**

* art模板引擎文档地址：https://aui.github.io/art-template/zh-cn/docs/index.html

* 安装
```
npm install art-template
```
```
npm install express-art-template
```

**因为render方法默认调用文件夹下views文件夹下的试图，所以要手动创建该文件夹**

**初体验,配置引擎**
```js
#引入模块
var express = require("express");

#创建服务器
var app = express();

#配置引擎
app.engine("html",require('express-art-template'));

#监听请求
app.get("/",function(req,res){
		//end() 响应字符串（乱码）
		//send() 响应字符串（自动识别）
		//render() 响应字符串（自动识别，指定文件中的字符串）

		res.render("test.html"{
			[参数1]：[值1],
			[参数2]：[值2],
			[参数3]：[
				{id:1,title:"标题1"},
				{id:2,title:"标题2"},
				{id:3,title:"标题3"}
			],
			})
	});

#启动服务
app.listen(8080,function(){
		console.log("启动成功");
	})
```

**框架路由**
```js
#get 路由
app.get(请求路径，回调函数);

#post路由
app.post(请求路径，回调函数);

#任意请求
app.all(请求路径，回调函数);
app.use(请求路径，回调函数);
```
**静态资源托管**
```js
#允许指定目录下文件被外部访问
#语法：express.static("目录名")

app.use("/public",express.static("public"));
```

### 如何开始一个框架项目
```
npm init -y
npm install express
npm install art-template
npm install express-art-template
```

### 模板中循环
```
{{each orders as order index}}

{{/each}}
```


