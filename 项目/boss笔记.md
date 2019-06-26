# vue 在哪个生命周期进行数据请求

看实际情况，一般在 created（或beforeRouter） 里面就可以，如果涉及到需要页面加载完成之后的话就用 mounted。


在created的时候，视图中的html并没有渲染出来，所以此时如果直接去操作html的dom节点，一定找不到相关的元素

而在mounted中，由于此时html已经渲染出来了，所以可以直接操作dom节点，（此时document.getelementById 即可生效了）

# vue 点击当前元素添加class 去掉兄弟的class

```vue
.blue {color: #2175bc;}
<ul><li v-for="(todo, index) in todos" v-on:click="addClass(index)" v-bind:class="{ blue:index==current}">
{{ todo.text }}
</li></ul>
data: {
current:0,
todos: [{ text: '选项一' },{ text: '选项二' },{ text: '选项三' }
]},
methods:{
addClass:function(index){this.current=index;}}})

```



或者



```vue

<ul class="inter_bar flex_parent">
                <li v-for="(item,index) in listBar"
                 :class="{ isHad:item.isHad }" class="flex_child"
                 @click="toggleTab(item,index)">{{ item.title }}</li>
</ul>


  toggleTab(item,index){
      //4.4
      this.lists=this.interactData[index];
      // console.log(index);
      if(!item.isHad){
        this.listBar.filter( value=>{
          value.isHad=false;
        });
        item.isHad=true;
      }
    }
            
            
```

## keep-alive 简介

`keep-alive` 是 Vue 内置的一个组件，可以使被包含的组件保留状态，或避免重新渲染。
 用法也很简单：

```vue
<keep-alive>
  <component>
    <!-- 该组件将被缓存！ -->
  </component>
</keep-alive>
```





## 动态组件

```vue
<component :is="currentTabComponent"></component>
```





### vue 登录，拦截

```vue
  methods: {
    getUserInfo() {
      // 提交mutation
      this.$store.commit("updateUserInfo", this.userInfo);
    },

    // 网页拦截
    checkLogin() {
      console.log(this.$route.path);
      //检测是否存在session
      if (!this.getCookie("session")) {
        if (this.$route.path == "/register") {
          this.$router.push("/register");
        } else {
          this.$router.push("/");
        }
      } else {
        this.$router.push(this.$route.path);
        // this.$router.push(this.$route.path)
      }
    }
  }
};
```





