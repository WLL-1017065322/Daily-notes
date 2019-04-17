<body>

    <div id="app">

​        **第一种，用keyup监听**

<input type="text" v-model="firstname" @keyup="func"> +

​        <input type="text" v-model="lastname" @keyup="func"> =

​        <input type="text" v-model="fullname">

​    </div>

    <div id="app1">

​        <input type="text" v-model="firstname"> +

​        <input type="text" v-model="lastname"> =

​        <input type="text" v-model="fullname">

​    </div>

​    

    <div id="app2">

​            <input type="text" v-model="firstname"> +

​            <input type="text" v-model="middlename"> +

​            <input type="text" v-model="lastname"> =

​            <input type="text" v-model="fullname">

​        </div>

    <script>

​        var vm = new Vue({

​            el: '#app',

​            data: {

​                firstname: '',

​                lastname: '',

​                fullname: ''

​            },

​            methods: {

​                func() {

​                    this.fullname = this.firstname + "-" + this.lastname

​                }

​            }

​        });

​        var vm = new Vue({

​            el: '#app1',

​            data: {

​                firstname: '',

​                lastname: '',

​                fullname: ''

​            },

​            methods: {

​            },

**第二种，用watch监听**

​            watch: {

​                'firstname': function (newVal, oldVal) {

​                    this.fullname = newVal + "-" + this.lastname

​                },

​                'lastname': function (newVal, oldVal) {

​                    this.fullname = this.firstname + "-" + newVal

​                }

​            }

​        });

​        var vm = new Vue({

​            el: '#app2',

​            data: {

​                firstname: '',

​                lastname: '',

​                fullname: ''

​            },

​            methods: {

​            },

**第三种用，computed**   注意，返回值

 // 在 computed 中，可以定义一些 属性，这些属性，叫做 【计算属性】， 计算属性的，本质，就是 一个方法，只不过，我们在使用 这些计算属性的时候，是把 它们的 名称，直接当作 属性来使用的；并不会把 计算属性，当作方法去调用；

​        // 注意1： 计算属性，在引用的时候，一定不要加 () 去调用，直接把它 当作 普通 属性去使用就好了；

​        // 注意2： 只要 计算属性，这个 function 内部，所用到的 任何 data 中的数据发送了变化，就会 立即重新计算 这个 计算属性的值

​        // 注意3： 计算属性的求值结果，会被缓存起来，方便下次直接使用； 如果 计算属性方法中，所以来的任何数据，都没有发生过变化，则，不会重新对 计算属性求值；

​           computed:{

​               "fullname":function(){

​                **return this.firstname + '-' + this.middlename + '-' + this.lastname**

​               **}**

​           }

​        })

​    </script>

</body>

</html>