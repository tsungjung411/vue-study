## slot 特性
- ### name 屬性
  - 用途
    - 給 ```<slot>``` 名稱，才能辨識使用哪個 ```<slot>``` 元件
  - 匿名 slot
    - ```<slot>``` 沒有指定 name
    - 又稱為 single slot (單一插槽)
  - 具名 slot
    - ```<slot name="xxx">``` 有指定 name
    - 又稱為 named slot (具名插槽)
- ### slot-scope 屬性
  - 此 ```<slot>``` 又稱為 Scoped Slots(作用域插槽)
  - 用途1：父類別元件，合併到子類別元件
  - 用途2：顯示客製化清單
    - 從 ```<slot>``` 端接收資料，再根據資料，客製化自己的 UI
    - 範例：    


## 參考資料
- [[Summer。桑莫。夏天] Vue.js: Slot](https://cythilya.github.io/2017/10/11/vue-component-slot/)
