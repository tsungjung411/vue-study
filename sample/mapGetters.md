
## mapGetters 程式碼範例
- mapGetters
- watch mapGetters

```html
<html>
<body>

    <div id="root">
        <button @click="onClick">[1] change the language</button>
        <br>
        <div>Result: 
            <br>language1: {{language1}}
            <br>language2: {{language2}}
        </div>
    </div>

    <script src="https://unpkg.com/vue" ></script>
    <script src="https://unpkg.com/vuex" ></script>

    <script>
        'use strict'

        const store = new Vuex.Store({
            state: {
                lang: 'en',
            },
            getters: {
                getLanguage1: (state) => {
                    const lang = state.lang;
                    console.log("called getLanguage1(): ", lang);
                    return lang;
                },
                getLanguage2: (state) => {
                    // not refer to the state.lang
                    // so this method won't be triggered when changing state.lang
                    const lang = 'state.lang';
                    console.log("called getLanguage2(): ", lang);
                    return lang;
                },
            }
        });

        new Vue({
            el: "#root",
            store: store,
            methods: {
                onClick: function() {
                    console.log('>> onClick:state:', this.$store.state);
                    let state = this.$store.state;
                    if (state.lang === 'en') {
                        state.lang = 'tw';
                    } else {
                        state.lang = 'en';
                    }
                    console.log('<< onClick:state:', this.$store.state);
                },
            },
            computed: {
                ...Vuex.mapGetters({
                    language1: 'getLanguage1',
                    language2: 'getLanguage2',
                }),
            },
            watch: {
                // The following definitions are all legal.
                // language1(newValue, oldValue) {
                // language1: (newValue, oldValue) => {
                // language1: function(newValue, oldValue) {
                
                language1(newValue, oldValue) {
                    console.log('watch: language1:');
                    console.log(' - newValue:', newValue);
                    console.log(' - oldValue:', oldValue);
                },
                language2(newValue, oldValue) {
                    console.log('watch: language2:');
                    console.log(' - newValue:', newValue);
                    console.log(' - oldValue:', oldValue);
                }
            }
        })
    </script>
</body>
</html>
```

## 個人對 mapGetters 的看法
> mapGetters 表面上看起來就像 API 
> <br>但實質上只是 computed state，就當作是一種屬性
> <br>所以能 watch 屬性變動，也就不足為奇

> mapGetters 的 API
> <br>parser 會去解析出：有哪些 state 變數依賴於那些 API
> <br>當 state 變數有變動，就會觸發相依的 API
