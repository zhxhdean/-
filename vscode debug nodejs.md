```
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "debug nodejs",
      "program": "${workspaceFolder}/app.js",
      "env": {
        "NODE_ENV": "dev"
      }
    }
  ]
}
```

type: 指定类型

program: 程序主入口文件

env: 环境变量
