
## Vuetify grid layout v-layout v-flex 參數設定
- [margin/padding values](https://v4-alpha.getbootstrap.com/utilities/spacing/)
  - m: margin (外邊界)
    - ma / mt / mb / ml / mr / mx / my
  - p: padding (內邊界/內距)
    - pa / pt / pb / pl / pr / px / py
  - 補充說明
    - 他們的關係：外邊界|邊框|內邊界
      <br>![](https://developer.mozilla.org/files/4045/margin-bottom.svg)
    - a(all-sides), t(top), b(bottom), l(left), r(right), x(x-axis), y(y-axis)
      <br><br>
      
- [Meaning of numbers in “col-md-4”,“ col-xs-1”, “col-lg-2” in Bootstrap](https://stackoverflow.com/questions/24175998/meaning-of-numbers-in-col-md-4-col-xs-1-col-lg-2-in-bootstrap)
  - xs = extra small screens (mobile phones)
  - sm = small screens (tablets)
  - md = medium screens (some desktops)
  - lg = large screens (remaining desktops)
  - the # of columns always add up to 12. It can be less than twelve,
  
- grid 為何要分 12 格? 可能的解釋如下：
  > ![](../../images/grid-mode.png)
  > 12 剛好是 1, 2, 3, 4, 6 的最小公倍數
  > <br>有 5 種模式，可以方便配置適當的排版
  > <br>模式1：1 1 1 1 1 1 1 1 1 1 1 1
  > <br>模式2：2 2 2 2 2 2
  > <br>模式3：3 3 3 3
  > <br>模式4：4 4 4 (三欄位均分)
  > <br>模式5：6 6 (兩欄位均分)
  > <br>其他不等寬配置

- [Bootstrap: Grid system](https://getbootstrap.com/docs/4.1/layout/grid/)
- [Vuetify: Grid system](https://vuetifyjs.com/en/framework/grid)

