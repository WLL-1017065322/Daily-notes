    <style>
    .v-enter,
    .v-leave-to {
        opacity:0;
        transform:translateX(150px);
    }
​    .v-enter-active,
​    .v-leave-active {
​        transition: all 0.5s ease;
​    }
​    </style>
</head>

    <div id="app">
        <a href="" @click.prevent="comName='login'">登录</a>
        <a href="" @click.prevent="cName='register'">注册</a>
        <transition name="" mode="out-in">=============================过渡模式
            <component :is="comName"></component>   
        </transition>
    </div>
    <script>
        Vue.component('login',{
            template:'<h3>登录组件</h3>'
        })
        Vue.component('register',{
            template:'<h3>注册组件</h3>'
        })
         var vm = new Vue({
            el : '#app',
            data : { 
                comName:'login'
             },
            methods : { }    
        });