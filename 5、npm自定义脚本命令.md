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