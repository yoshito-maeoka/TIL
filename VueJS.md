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



