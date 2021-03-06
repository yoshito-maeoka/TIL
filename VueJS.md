# vue component
## replace: false

```js
new Vue([{
  el:'#app',
  template:'<div>something to add </div>',
  replace: false
});
```

then will be added into #app like that:

```html
<div id="app">
  <div>something to add </div>
</div>
```


## how to inject values from child component to parent component

```javascript
this.$parent['name_of_variable'] = 'value of child';
```


## give own parameter with calleing emit
```html
    <child :item='item' @emitting='emitted($event, index)'/>
```
then in handler:

```javascript
  methods: {
    emitted(eventArgs, index) {
      console.log(index, eventArgs)
    }
  },
```


## v-model = (v-bind:value, v-on:input)

```html
<vue-input label="Input" name="input" v-model="form.input"></vue-input>
```

in component:
```html
<input ...
       :value="value"
       @input="updateValue"
       ...
/>
```
# vue cli as framework
## Using Env Variables in Client-side Code
https://cli.vuejs.org/guide/mode-and-env.html#using-env-variables-in-client-side-code

we can define in .env file like that:
```.env
VUE_APP_XXX=YYY
```
Keys with PREFIX "VUE_APP_" will be added automatically into your ENVIRONMENT Variable in client process. We can refer them like that:
```js
console.log(process.env.VUE_APP_XXX)
```
it will return:
```
YYY
```


## debug test:unit
in package.json:
```JSON
"test:debug": "node --inspect-brk node_modules/.bin/vue-cli-service test:unit --no-cache --watch --runInBand"
```
