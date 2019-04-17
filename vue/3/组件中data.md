组件可以有data

但是必须是一个方法，且内部返回一个对象？？？？？？为什么

\1. 在组件中，`data`需要被定义为一个方法，例如：

\```

Vue.component('account', {

​      template: '#tmpl',

​      data() {

​        return {

​          msg: '大家好！'

​        }

​      },

​      methods:{

​        login(){

​          alert('点击了登录按钮');

​        }

​      }

​    });