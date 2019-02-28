## 安装nodejs(以windows为例)

> ### 下载地址
```
http://nodejs.cn/download
```
* or
```
https://nodejs.org/zh-cn/download
```

> ### 安装完nodejs，在黑窗口中查看是否安装成功
```
node -v
```

> ### 进入nodejs
```
node
```

> ### 输出hello world
```
console.log("hello world");
```

### 自定义模块

* 定义:say.js
```js
function say(){
	console.log("hello world!");
}

#(另一种方式) module.exports.say = say;
exports.say = say;
```
```
var res = require("./say");

res.say();
```



