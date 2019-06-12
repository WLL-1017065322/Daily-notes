```js
new Vue({
  router,
  store,
  render: h => h(App),
}).$mount('#app');
```





这是Vue 2.0新增的函数，可以直接给绑定节点渲染一个vue组件，如果在Vue 1.x下，就应该使用

```js
new Vue({
    el: '#app',
    components: { App }
});
```

然后在页面中写入标记：

```vue
<div id="app">
    <app></app>
</div>
```