### npm是一个命令行工具,下载第三方所需要的模块

**下载nodejs会自动安装npm工具**
```
npm -v
```

> ### nmp语法

**查看**
```
npm list
```

**初始化**
```
npm init -y
```

**安装模块**
```
npm install [模块]
```

**卸载模块**
```
npm uninstall [模块]
```

**安装参数**

* --save 记录生产环境所需要的模块

* --save-dev 记录开发环境所需要的模块

* -g 该模块可在命令行运行

**模块网址**
```
https://www.npmjs.com
```

**例如安装mime模块**

* 搜索mime，有安装命令提示
```
npm -i mime [-g]
```
```js
 //引入模块
 var mime = require("mime");
 //判断文件类型
 var img = "xxxx.png";

 console.log(mime.getType(img));
 console.log(mime.getExtension("image/png"));
```
