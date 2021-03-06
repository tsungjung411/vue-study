
## VueI18n 程式碼範例
```html=
<html>
<body>

    <div id="root">
        <h1>{{$t('greeting')}}</h1>

        <p style="float: right">by {{$t('profile.first_name') + ' ' + $t('profile.last_name')}}</sub>
    </div>

    <script src="https://unpkg.com/vue" ></script>
    <script src="https://unpkg.com/vue-i18n" ></script>

    <script>
        'use strict'
        
        const tw = {
            greeting: '您好, Vue!',
            profile: {
                first_name: '宗容',
                last_name: '蔡',
            },
        }
        const en = {
            greeting: 'hello, Vue!',
            profile: {
                first_name: 'TsungJung',
                last_name: 'Tsai',
            },
        }
        const jp = {
            greeting: 'こんにちは, Vue!',
            profile: {
                first_name: 'しゅうよう',
                last_name: 'さい',
            },
        }
        const i18n = new VueI18n({
            locale: 'tw', // default language: tw / jp / en
            messages: {tw, en, jp}
        })

        new Vue({
            el: "#root",
            i18n
        })
    </script>
</body>
</html>
```

<br>

## 執行結果
### locale = 'tw'
![](../images/i18n-sample-tw.png)

### locale = 'en'
![](../images/i18n-sample-en.png)

### locale = 'jp'
![](../images/i18n-sample-jp.png)
