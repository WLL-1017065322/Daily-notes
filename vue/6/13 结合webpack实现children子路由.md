main.js

import Vue from 'vue'

 

import VueRouter from 'vue-router'

Vue.use(VueRouter)

// import Vue from '../node_modules/vue/dist/vue'

import app from './app.vue'

import account from './main/Account.vue'

import goodslist from './main/GoodsList.vue'

import login from './subcom/login.vue'

import register from './subcom/register.vue'



var router=new VueRouter({

​    routes:[

​        {path:'/account',component:account,children:[

​            {path:'login',component:login},

​            {path:'register',component:register}

​        ]},

​        {path:'/goodslist',component:goodslist}

​    ]

})

var vm = new Vue({

​    el: '#app',

​    data: {

​        msg: "123"

​    },

​    // components: {

​    //     login

​    // }

​    render: function (createElements) {

​        return createElements(app)

​    },

​    router

})



app.vue

<template>

  <div>

​    <h1>这是 App 组件</h1>

  

​    <router-link to="/account">Account</router-link>

​    <router-link to="/goodslist">Goodslist</router-link>

​    <router-view></router-view>

  </div>



account.vue

<template>

  <div>

​    <h1>这是 Account 组件</h1>

​    <router-link to="/account/login">登录</router-link>

​    <router-link to="/account/register">注册</router-link>

​    <router-view></router-view>

  </div>

</template>





