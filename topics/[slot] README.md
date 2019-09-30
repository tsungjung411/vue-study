## slot 特性
- ### name 屬性
  - 用途
    - 給 ```<slot>``` 名稱，才能辨識使用哪個 ```<slot>``` 元件
  - 匿名插槽，又稱單一插槽(single slot)
    - ```<slot>``` 沒有指定 name
  - 具名插槽(named slot)
    - ```<slot name="xxx">``` 有指定 name
- ### slot-scope 屬性
  - 此 ```<slot>``` 又稱為 Scoped Slots(作用域插槽)
  - 用途1：父類別元件，合併到子類別元件
    - 範例：[[slot] merge layout.htm](../topics/%5Bslot%5D%20merge%20layout.htm)
  - 用途2：顯示客製化清單
    - 從 ```<slot>``` 端接收資料，再根據資料，客製化自己的 UI
    - 範例：[[slot][Scoped Slot] slot + slot-scope.htm](../topics/%5Bslot%5D%5BScoped%20Slot%5D%20slot%20+%20slot-scope.htm)


## 參考資料
- [[Summer。桑莫。夏天] Vue.js: Slot](https://cythilya.github.io/2017/10/11/vue-component-slot/)
