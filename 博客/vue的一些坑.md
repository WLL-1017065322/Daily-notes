# 记录vue 的一些坑

### 1.给link添加事件、给组件绑定原生事件

在vue-router1中使用v-link写入路由，但是在vue-router2中要使用router-link写入路由，在浏览器渲染的时候会把router-link渲染成a。

有时候需要为router-link注册事件，对于一般的html元素，直接使用@click="eventFun"即可，但是对于router-link，像普通html元素那样注册事件后并不管用，需要添加.native才会成功注册。

事实上给组件绑定原生事件就需要.native修饰v-on，否则无法注册成功。

```vue
<my-component v-on:click.native="doTheThing"></my-component>
```

错误事例：

```vue
<el-inputplaceholder="请输入特定消费金额 " @mouseover="test()"></el-input>

<router-link:to="item.menuUrl" @click="toggleName=''"></router-link>

<!--官方文档有-><!--https://cn.vuejs.org/v2/guide/components.html#给组件绑定原生事件-->
```



### 2.修改prop中的数据

每次父组件更新时，子组件的所有 prop 都会更新为最新值。这意味着你不应该在子组件内部改变 prop。如果你这么做了，Vue 会在控制台给出警告。

在两种情况下，我们很容易忍不住想去修改 prop 中数据：
Prop 作为初始值传入后，子组件想把它当作局部数据来用；
Prop 作为原始数据传入，由子组件处理成其它数据输出。

对这两种情况，正确的应对方式是：

定义一个局部变量，并用 prop 的值初始化它：

```vue
props: ['initialCounter'],
data: function () {
return { counter: this.initialCounter }
}
```

定义一个计算属性，处理 prop 的值并返回：

```
props: ['size'],
computed: {
normalizedSize: function () {
return this.size.trim().toLowerCase()
}
}
```



### 3.我需要遍历的数组值更新了,值也赋值了,为什么视图不更新？

因为有局限性啊,官方文档也说的很清楚，一般我们常用的手段是使用:this.$set(obj,item,value)

官方文档如下：

由于 JavaScript 的限制，Vue 不能检测以下变动的数组：

当你利用索引直接设置一个项时，例如：vm.items[indexOfItem] = newValue
当你修改数组的长度时，例如：vm.items.length = newLength
为了解决第一类问题，以下两种方式都可以实现和 vm.items[indexOfItem] = newValue 相同的效果，同时也将触发状态更新：

// Vue.set
Vue.set(example1.items, indexOfItem, newValue)
// Array.prototype.splice
example1.items.splice(indexOfItem, 1, newValue)
为了解决第二类问题，你可以使用 splice：
example1.items.splice(newLength)

还是由于 JavaScript 的限制，Vue 不能检测对象属性的添加或删除，对于已经创建的实例，Vue 不能动态添加根级别的响应式属性。

但是，可以使用 Vue.set(object, key, value) 方法向嵌套对象添加响应式属性。例如，对于：

```
var vm = new Vue({
data: {
userProfile: {
name: 'Anika'
}
}
})
```

你可以添加一个新的 age 属性到嵌套的 userProfile 对象：

Vue.set(vm.userProfile, 'age', 27)
有时你可能需要为已有对象赋予多个新属性，比如使用 Object.assign() 或 _.extend()。
在这种情况下，你应该用两个对象的属性创建一个新的对象。所以，如果你想添加新的响应式属性，不要像这样：

```vue
Object.assign(this.userProfile, {
age: 27,
favoriteColor: 'Vue Green'
})
你应该这样做：
this.userProfile = Object.assign({}, this.userProfile, {
age: 27,
favoriteColor: 'Vue Green'
})
```



### 4.建议尽可能在使用 v-for 时提供 key

```vue
<div v-for="item in items" :key="item.id">
<!-- 内容 -->
</div>
```

它是 Vue 识别节点的一个通用机制，key 并不与 v-for 特别关联，key 还具有其他用途，我们将在后面的指南中看到其他用途，后续补充
（2.2.0+ 的版本里，当在组件中使用 v-for 时，key 现在是必须的。）



### 5.路由模式改为history后,除了首次启动首页没报错,刷新访问路由都报错

必须给对应的服务端配置查询的主页面..也可以认为是主路由入口的引导。。。Vue-Router官方文档链接

（https://router.vuejs.org/zh-cn/essentials/history-mode.html）包括动态路由匹配、向路由组件传递props等基础知识



### 6.Uncaught ReferenceError: xxx is not define

实例内的 data 对应的变量没有声明
你导入模块报这个错误,那绝逼是导出没写好



### 7.Error in render function:"Type Error: Cannot read property 'xxx' of undefined"

这种问题大多都是初始化的姿势不对;
比如引入echart这些...仔细去了解下生命周期,再来具体初始化;
vue 组件有时候也会(嵌套组件或者 props传递初始化)..也是基本这个问题



### 8.Failed to mount component: template or render function not defined

组件挂载失败,问题只有这么几个
组件没有正确引入; 挂载点顺序错了了;
自行动手排查



### 9.[Vue warn]: Error in render function: "TypeError: Cannot read property '0' of undefined"



想将seller传递给子组件使用，但是我们ajax获取数据是异步过程，也就是说一开始在初始化seller时是空对象，所以把此时的seller传给header就是undefined

使用v-if可以解决报错问题，和created为空问题  

【详解vue2父组件传递props异步数据到子组件的问题】【http://www.jb51.net/article/117447.htm】



### 10.vue-cli 新建项目 缺少dev-server.js和dev-client.js , 怎么模拟数据

在使用vue开发过程中，难免需要去本地数据地址进行请求，而原版配置在dev-server.js中，新版vue-webpack-template已经删除dev-server.js，改用webpack.dev.conf.js代替，所以 配置本地访问在webpack.dev.conf.js里配置即可。

```vue
//首先
const express = require('express')
const app = express()
var appData = require('../data.json')
var seller = appData.seller
var goods = appData.goods
var ratings = appData.ratings
var apiRoutes = express.Router()
app.use('/api', apiRoutes)

//找到devServer,添加
before(app) {
  app.get('/api/seller', (req, res) => {
    res.json({
      // 这里是你的json内容
      errno: 0,
      data: seller
    })
  }),
  app.get('/api/goods', (req, res) => {
    res.json({
      // 这里是你的json内容
      errno: 0,
      data: goods
    })
  }),
  app.get('/api/ratings', (req, res) => {
    res.json({
      // 这里是你的json内容
      errno: 0,
      data: ratings
    })
  })
}
```



### 11.[WDS] Errors while compiling. Reload prevented.

有一种错误的原因是import的路径不对 

import header from '@views/header/header.vue'



### 12.应当避免在模板或计算属性中使用 $refs

$refs 只在组件渲染完成后才填充，并且它是非响应式的。它仅仅是一个直接操作子组件的应急方案——应当避免在模板或计算属性中使用 $refs

