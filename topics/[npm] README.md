## 相關術語
- cli
  - 翻譯
    - en: command-line interface
    - cht: 命令列介面
    - chs: 腳手架
  - 用途
    - [脚手架是帮你减少「为减少重复性工作而做的重复性工作」](https://www.zhihu.com/question/47731497)
  - 相關工具
    - vue-cli
    - webpack-cli

<br>

## npm
- ```npm -v```
  > 印出 npm 版本
  ```
  6.13.1
  ```
- ```npm -version```
  > 印出 npm 詳細版本
  ```
  {
    'vue-todos': '1.0.0',
    npm: '6.13.1',
    ares: '1.15.0',
    brotli: '1.0.7',
    cldr: '35.1',
    http_parser: '2.8.0',
    icu: '64.2',
    llhttp: '1.1.4',
    modules: '72',
    napi: '4',
    nghttp2: '1.39.2',
    node: '12.10.0',
    openssl: '1.1.1c',
    tz: '2019a',
    unicode: '12.1',
    uv: '1.31.0',
    v8: '7.6.303.29-node.16',
    zlib: '1.2.11'
  }
  ```
  
- ```npm list```
  > 列出當前專案(local)已安裝的所有套件(包含子套件)，及其版本
  
- ```npm list -g```
  > 列出系統(global)已安裝的所有套件(包含子套件)，及其版本
  
- ```npm list --depth=0```
  > 列出當前專案(local)已安裝的所有套件(不含子套件)，及其版本
  ```
  vue-todos@1.0.0 /home/tj/Downloads/vue1120/vue-todos
  ├── babel-core@6.26.3
  ├── babel-loader@7.1.5
  ├── babel-preset-env@1.7.0
  ├── babel-preset-stage-3@6.24.1
  ├── cross-env@5.2.1
  ├── css-loader@3.2.0
  ├── file-loader@1.1.11
  ├── vue@2.6.10
  ├── vue-loader@13.7.3
  ├── vue-template-compiler@2.6.10
  ├── UNMET PEER DEPENDENCY webpack@4.41.2
  └── webpack-dev-server@2.11.5
  ```

- ```npm list --depth=0 -g```
  > 列出系統(global)已安裝的所有套件(不含子套件)，及其版本
  ```
  /usr/lib
  ├── npm@6.13.1
  ├── vue-cli@2.9.6
  ├── webpack@4.41.2
  ├── webpack-cli@3.3.10
  └── webpack-dev-server@3.9.0
  ```

- ```npm list webpack-dev-server```
  > 列出當前專案(local)已安裝的 webpack-dev-server 套件，及其版本
  ```
  vue-todos@1.0.0 /home/tj/Downloads/vue1120/vue-todos
  └── webpack-dev-server@2.11.5 
  ```
  
- ```npm list webpack-dev-server -g```
  > 列出系統(global)已安裝的 webpack-dev-server 套件，及其版本
  ```
  /usr/lib
  └── webpack-dev-server@3.9.0
  ```

<br>

## npm install (同 npm i)
> 安裝 npm 指令或套件
- ```npm help install``` (同 ```npm help i```)
  > 印出 npm install 指令說明

### npm install 套件
- ```npm install``` (同 ```npm i```)
  > 安裝 package.json 所定義的相關套件
  
- ```npm install moment``` (同 ```npm i moment```)
  > 安裝：日期時間格式化的專用套件 moment.js，並更新到 package.json
  
- ```npm install vuetify``` (同 ```npm i vuetify```)
  > 安裝：vue 的美化(beautify) UI，並更新到 package.json

### npm install 指令
- 參數
  - ```-g``` (置放該參數，沒有位置順序問題)
    > 通常用在安裝指令 npm install -g 指令 (或 npm install 指令 -g)
    > <br>表示將此指令，安裝到 node.js 的全域執行目錄下
    > <br>於是，它能在本機的任意目錄下執行該指令
    ```
    tj@tj-M52AD-M12AD-A-F-K31AD:~$ vue
    Usage: vue <command> [options]

    Options:
      -V, --version  output the version number
      -h, --help     output usage information

    Commands:
      init           generate a new project from a template
      list           list available official templates
      build          prototype a new project
      create         (for v3 warning only)
      help [cmd]     display help for [cmd]
    ```
  
- ```npm install vue-cli -g``` (同 ```npm i vue-cli -g```)
  > 安裝 vue-cli 指令

<br>
  
## 下載並建立一個 todo 範本 (相當於 Hello World 的空專案)
```bash
# 安裝 vue-cli 套件到 global, 因此就可以在任意的 terminal 中，直接使用 vue 指令
# 若已經安裝過 vue-cli 套件，就可以略過此指令
npm install vue-cli -g   # npm i vue-cli -g

# 使用 webpack-simple 官方範本來建立一個小專案，並將專案命名成 vue-todos 
vue init webpack-simple vue-todos

# 在 vue-todos 專案中，安裝 package.json 所定義的相關套件
cd vue-todos
npm install

# 在 vue-todos 專案中，執行 package.json 所定義的 scripts 檔
npm run dev
```

<br>

## 故障排除
### [webpack/bin/config-yargs](https://github.com/mzgoddard/jest-webpack/issues/27)
- 問題
  ```
  Error: Cannot find module 'webpack/bin/config-yargs'
  Require stack:
  - /home/tj/Downloads/vue1120/vue-todos/node_modules/webpack-dev-server/bin/webpack-dev-server.js
  ```
- 原因
  > webpack/bin/config-yargs has been moved to webpack-cli/bin/config-yargs.
- 解法
  - 安裝 webpack-cli
    ```
    npm install webpack-cli
    ```
  - 修改 package.json
    - Before: ```"webpack-dev-server": "^2.9.1"```
    - After: ```"webpack-dev-server": "^3.9.0"```
  - 更新 package.json
    ```
    $ npm install
    ```
    <br>
### vue-loader: build failed
- 問題
  ```
  ERROR in ./src/App.vue
  Module build failed (from ./node_modules/vue-loader/index.js):
  TypeError: Cannot read property 'vue' of undefined
      at Object.module.exports (/home/tj/Downloads/vue1120/vue-todos/node_modules/vue-loader/lib/loader.js:61:18)
   @ ./src/main.js 2:0-28 7:13-16
  ```
- 解法
  - 修改 package.json
    - Before: ```"vue-loader": "^13.0.5",```
    - After: ```"vue-loader": "14.2.4",```
  - 更新 package.json
    ```
    $ npm install
    ```
    <br>
