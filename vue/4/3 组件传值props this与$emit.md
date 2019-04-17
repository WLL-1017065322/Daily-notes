###组件传值-父组件向子组件传值和data与props的区别

<body>

  <div id="app">

​    <!-- 父组件，可以在引用子组件的时候， 通过 属性绑定（v-bind:） 的形式, 把 需要传递给 子组件的数据，以属性绑定的形式，传递到子组件内部，供子组件使用 -->

​    <com1 v-bind:parentmsg="msg"></com1>

  </div>

  <script>

​    // 创建 Vue 实例，得到 ViewModel

​    var vm = new Vue({

​      el: '#app',

​      data: {

​        msg: '123 啊-父组件中的数据'

​      },

​      components: {

​        // 结论：经过演示，发现，子组件中，默认无法访问到 父组件中的 data 上的数据 和 methods 中的方法

​        com1: {

​          data() { // 注意： 子组件中的 data 数据，并不是通过 父组件传递过来的，而是子组件自身私有的，比如： 子组件通过 Ajax ，请求回来的数据，都可以放到 data 身上；

​            // data 上的数据，都是可读可写的；

​            return {

​              title: '123',

​              content: 'qqq'

​            }

​          },

​          **template: '<h1 @click="change">这是子组件 --- {{ parentmsg }}</h1>',**

​          **// 注意： 组件中的 所有 props 中的数据，都是通过 父组件传递给子组件的**

​          **// props 中的数据，都是只读的，无法重新赋值**

​          **props: ['parentmsg'], // 把父组件传递过来的 parentmsg 属性，先在 props 数组中，定义一下，这样，才能使用这个数据**

​          directives: {},

​          filters: {},

​          components: {},

​          methods: {

​            change() {

​              this.parentmsg = '被修改了'

​            }

​          }

​        }

​      }

​    });

  </script>



###组件传值-子组件通过事件调用向父组件传值



<body>

  <div id="app">

​    <!-- 父组件向子组件 传递 方法，使用的是 事件绑定机制； v-on, 当我们自定义了 一个 事件属性之后，那么，子组件就能够，通过某些方式，来调用 传递进去的 这个 方法了 -->

​    **<com2 @func="show"></com2>**

  </div>

  <template id="tmpl">

    <div>

​      <h1>这是 子组件</h1>

​      <input type="button" value="这是子组件中的按钮 - 点击它，触发 父组件传递过来的 func 方法" @click="myclick">

​    </div>

  </template>

  <script>

​    // 定义了一个字面量类型的 组件模板对象

​    var com2 = {

​      template: '#tmpl', // 通过指定了一个 Id, 表示 说，要去加载 这个指定Id的 template 元素中的内容，当作 组件的HTML结构

​      data() {

​        return {

​          sonmsg: { name: '小头儿子', age: 6 }

​        }

​      },

​      methods: {

​        myclick() {

​          // 当点击子组件的按钮的时候，如何 拿到 父组件传递过来的 func 方法，并调用这个方法？？？

​          //  emit 英文原意： 是触发，调用、发射的意思

​          // this.$emit('func123', 123, 456)

​          **this.$emit('func', this.sonmsg)**

​        }

​      }

​    }

​    // 创建 Vue 实例，得到 ViewModel

​    var vm = new Vue({

​      el: '#app',

​      data: {

​        datamsgFormSon: null

​      },

​      methods: {

​        show(data) {

​          // console.log('调用了父组件身上的 show 方法: --- ' + data)

​          // console.log(data);

​          this.datamsgFormSon = data

​        }

​      },

​      components: {

​        com2

​        // com2: com2

​      }

​    });