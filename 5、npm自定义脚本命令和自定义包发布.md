### npm自定义命令

> ### 在package.json包中配置scripts
```
"scripts": {
    "test" : "echo \"Error: no test specified\" && exit 1",
    "a"    : "echo 666",
    "mime" : "node ./mime.js"
  },
```

> ### 运行相应的命令
```
npm run [别名]
```

### npm自定义包的发布

**1、新建文件夹,并且初始化**
```
npm init -y
```

**2、配置package.json参数**
```
{
  "name": "mydemo",
  "version": "2.0.0",
  "description": "php,nodejs",
  "main": "index.js",
  "scripts": {
    "test" : "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": ["nodejs","php"],
  "author": "eden",
  "license": "ISC"
}
```

**3、在index.js封装包代码**
```
function say(){
	console.log("hello npm");
}

exports.say = say;
```

**4、注册npmjs账号(一定要有账号才可以发布)**
```
https://www.npmjs.com
```

**5、nrm切换到国外服务器才可以发布**
```
nrm ls
```
```
nrm use npm
```

**6、登陆自己的账号，输入账号，密码，邮箱**
```
npm login
```

**7、上传自己的包到仓库**
```
npm publish
```