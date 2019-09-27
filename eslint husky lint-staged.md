- 1.安装eslint

  ``` 
  npm i eslint --D 
  ```
  
- 2.配置eslint

  ``` 
  eslint --init
  ```
  
  生成eslintrc.js
  ```
    module.exports = {
    env: {
      browser: true,
      commonjs: true,
      es6: true,
    },
    extends: 'eslint:recommended',
    rules: {
      indent: ['error', 2],
      'linebreak-style': ['error', 'unix'],
      quotes: ['error', 'single'],
      semi: ['error', 'always'],
    }
  };
  ```

- 3.新建文件.eslitignore，忽略eslint校验目录或文件
  ```
    node_modules/
    *.json
    *.md
  ```
  
- 4.git commit提交eslint钩子

  - 4.1 安装 husky、lint-staged、prettier

    ```
    npm i husky lint-staged prettier --D
    ```

  - 4.2 配置package.json

    ```
        "husky": {
          "hooks": {
            "pre-commit": "lint-staged"
          }
        },
        "lint-staged": {
          "*.js": [
            "prettier --single-quote --tab-width 2 --trailing-comma all --write",
            "eslint *.js --fix",
            "git add"
          ]
        }
    ```

- 5.async/await 特性校验

  - 5.1 安装 babel-eslint

  ```
  npm i babel-eslint --D
  ```

  - 5.2 配置 eslintrc.js

  ```
  parser: 'babel-eslint'
  ```
