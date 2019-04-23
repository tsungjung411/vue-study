
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
					// so this method won't be called when changing state.lang
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

