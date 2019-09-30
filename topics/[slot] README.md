## slot 特性
- ### 特性1：可以合併父元件與子元件的layout
  - 此 ```<slot>``` 又稱為 作用域插槽(Scoped Slot)
  - 範例：[[slot] merge layout.htm](../topics/%5Bslot%5D%20merge%20layout.htm)
- ### name 屬性
  - 用途
    - 給 ```<slot>``` 名稱，才能辨識使用哪個 ```<slot>``` 元件
  - 匿名插槽
    - ```<slot>``` 沒有指定 name
    - 又稱 單一插槽 (single slot)
  - 具名插槽 (named slot)
    - ```<slot name="xxx">``` 有指定 name
- ### slot-scope 屬性
  - 用途：顯示客製化清單
    - 從 ```<slot>``` 端接收資料，再根據資料，客製化自己的 UI
  - 範例：[[slot][Scoped Slot] slot + slot-scope.htm](../topics/%5Bslot%5D%5BScoped%20Slot%5D%20slot%20+%20slot-scope.htm)


## 參考資料
- [深入理解vue中的slot与slot-scope](https://juejin.im/post/5a69ece0f265da3e5a5777ed)
- [[Summer。桑莫。夏天] Vue.js: Slot](https://cythilya.github.io/2017/10/11/vue-component-slot/)
