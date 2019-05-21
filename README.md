
## CDN (Content Delivery Network)
  - Source: https://unpkg.com/
    > unpkg is a fast, global content delivery network for everything on npm. Use it to quickly and easily load any file from any package using a URL like:
  - Format: ```unpkg.com/:package@:version/:file```
  - Vue CDN: https://unpkg.com/vue
  - Vuex CDN: https://unpkg.com/vuex
  - Vue-i18n CDN: https://unpkg.com/vue-i18n (locale/language/internationalization)


## 基礎學習資源
- [[tutorialspoint] VueJS - Introduction](https://www.tutorialspoint.com/vuejs/vuejs_introduction.htm)
- [[iT 邦幫忙][2018] Vue.js 30天隨身包 系列](https://ithelp.ithome.com.tw/users/20107673/ironman/1470)
- [[iT 邦幫忙][2017] Vue.js 30天 系列](https://ithelp.ithome.com.tw/users/20103424/ironman/1049) (day 18 後可以不用看，不知道再寫什麽)
- [[vuejs.org][chs] vue.js](https://cn.vuejs.org/v2/guide/index.html)
- [[vuejs.org][en] vue.js](https://vuejs.org/v2/guide/)
- [[vuejs.org/][en] vuex](https://vuex.vuejs.org/)
- [vue & vuex 10 - 什麼是 vuex?](https://ithelp.ithome.com.tw/articles/10185686)
- 當地語系化(localization)
  - [Vue I18n](https://kazupon.github.io/vue-i18n/started.html#html)
- [[中] Vue Router](https://router.vuejs.org/zh/)


## 基礎學習資源：Summer。桑莫。夏天
- [Todo List: Vue.js Example](https://cythilya.github.io/2017/03/07/todolist-vue-example/)
- [Vue.js: data、v-model 與雙向綁定](https://cythilya.github.io/2017/04/14/vue-data-v-model/)
- [Vue.js: 計算屬性 Computed](https://cythilya.github.io/2017/04/15/vue-computed/)
- [透過 :is & &lt;keep-alive&gt; 來達成動態元件佈署](https://cythilya.github.io/2017/10/22/vue-component-dynamic-components/)
- [Slot：單個插槽（Single Slot） / 具名插槽（Named Slots）/ 作用域插槽（Scoped Slots）](https://cythilya.github.io/2017/10/11/vue-component-slot/)
- [[props] camelCase vs kebab-case](https://cythilya.github.io/2017/05/16/vue-component-prop/)


## 其他主題討論
- [可帶的 Event Modifiers](https://vuejs.org/v2/guide/events.html#Event-Modifiers)
- [Key Modifiers](https://vuejs.org/v2/guide/events.html#Key-Modifiers)
- 透過 &lt;v-icon&gt; 使用 material icon
  - [How to use the new Material Design Icon themes: Outlined, Rounded, Two-Tone and Sharp?
](https://stackoverflow.com/questions/50303454/how-to-use-the-new-material-design-icon-themes-outlined-rounded-two-tone-and?noredirect=1&lq=1)
- 跨站請求問題
  - [Vue.js + Node.js + OpenAPI 帶你一次了解 CORS 跨域請求](https://medium.com/@moojing/vue-js-node-js-openapi-%E5%B8%B6%E4%BD%A0%E4%B8%80%E6%AC%A1%E4%BA%86%E8%A7%A3cors%E8%B7%A8%E5%9F%9F%E8%AB%8B%E6%B1%82-b37cd926551f)
  - [使用跨域代理伺服器(CORS PROXY)，解決讀取第三方網站資料問題﹍實作範例](https://www.wfublog.com/2018/11/js-cors-proxy.html)
    - [這是一個簡單、免費的跨域代理伺服器<br>https://cors-anywhere.herokuapp.com/](https://cors-anywhere.herokuapp.com/)
  - 驗證工具：
    - [curl.md](https://gist.github.com/subfuzion/08c5d85437d5d4f00e58)
  
## 高階功能實作
- [[Vue] uploader](https://lian-yue.github.io/vue-upload-component/#/en/examples/full)
- [A Vue.js upload component powered by simple-uploader.js](https://vuejsexamples.com/a-vue-js-upload-component-powered-by-simple-uploader-js/)


## Tips
- html 的屬性定義：```:iconName``` 應定義為 ```:icon-name```
  > [Vue tip]: Prop "iconname" is passed to component <Anonymous>, but the declared prop name is "iconName". Note that HTML attributes are case-insensitive and camelCased props need to use their kebab-case equivalents when using in-DOM templates. You should probably use "icon-name" instead of "iconName".
