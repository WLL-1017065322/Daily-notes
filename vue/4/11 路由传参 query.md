 <!-- 如果在路由中，使用 查询字符串，给路由传递参数，则 不需要修改 路由规则的 path 属性 -->

 <router-link to="/login?id=10&name=zs">登录</router-link>

​    <router-link to="/register">注册</router-link>

var login = {

​      **template: '<h1>登录 --- {{ $ route. query.id}} --- {{ ​$route.query.name }}</h1>',**

​      data(){

​        return {

​          msg: '123'

​        }

​      },

​      created(){ // 组件的生命周期钩子函数

​        // console.log(this.$route)

​        // console.log(this.$route.query.id)

​      }

​    }

​    var register = {

​      template: '<h1>注册</h1>'

​    }

​    var router = new VueRouter({

​      routes: [

​        { path: '/login', component: login },

​        { path: '/register', component: register }

​      ]

​    })

​    // 创建 Vue 实例，得到 ViewModel

​    var vm = new Vue({

​      el: '#app',

​      data: {},

​      methods: {},

​      // router: router

​      router

​    });

  </script>