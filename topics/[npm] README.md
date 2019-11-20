## 相關術語
- cli
  - en: command-line interface
  - cht: 命令列介面
  - chs: 腳手架（用途：脚手架是帮你减少「为减少重复性工作而做的重复性工作」）

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
  > for local packages (但跟 -g 好像沒有差別)
- ```npm list -g```
  > for globally installed packages

<br>

## npm install (同 npm i)
- ```npm help install``` (同 ```npm help i```)
  > 印出指令說明
  
<br>
  
## 下載並建立一個 todo 範本
```bash
# 安裝 vue-cli 套件到 global, 因此就可以在任意的 terminal 中，直接使用 vue 指令
# 若已經安裝過 vue-cli 套件，就可以略過此指令
npm install vue-cli -g   # npm i vue-cli -g

# 從 webpack-simple 範本中，下載 vue-todos 專案
vue init webpack-simple vue-todos

# 在 vue-todos 專案中，安裝 package.json 所定義的相關套件
cd vue-todos
npm install

# 在 vue-todos 專案中，執行 package.json 所定義的 scripts 檔
npm run dev
```
