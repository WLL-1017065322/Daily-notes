   routes: [ // 路由匹配规则 

​        // 每个路由规则，都是一个对象，这个规则对象，身上，有两个必须的属性：

​        //  属性1 是 path， 表示监听 哪个路由链接地址；

​        //  属性2 是 component， 表示，如果 路由是前面匹配到的 path ，则展示 component 属性对应的那个组件

​        // 注意： component 的属性值，必须是一个 组件的模板对象， 不能是 组件的引用名称；

​        // { path: '/', component: login },

​        **{ path: '/', redirect: '/login' }, // 这里的 redirect 和 Node 中的 redirect 完全是两码事**

​        { path: '/login', component: login },

​        { path: '/register', component: register }

​      ],