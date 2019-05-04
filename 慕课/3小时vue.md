

# 1

### 开发环境&工具：

nvm：切换node版本

nvm: nvm ls  ;num use



vue-cli

npm run serve

### 知识点解释：





![1556848275342](assets/1556848275342.png)



# 2Vue框架常用知识点



### 第一个vue项目

优先绑定第一个{{msg}}

vueCDN使用： https://www.bootcdn.cn/



<script src="https://cdn.bootcss.com/vue/2.6.10/vue.min.js"></script>



### 模板语法：

vue文件结构：

插值语法

v-bind  ：

v-on @

v-html





### 计算属性和侦听器

computed：

模板内的表达式非常便利，但是设计它们的初衷是用于简单运算的。在模板中放入太多的逻辑会让模板过重且难以维护。例如：

```
<div id="example">
  {{ message.split('').reverse().join('') }}
</div>
```

在这个地方，模板不再是简单的声明式逻辑。你必须看一段时间才能意识到，这里是想要显示变量 `message` 的翻转字符串。当你想要在模板中多次引用此处的翻转字符串时，就会更加难以处理。

所以，对于任何复杂逻辑，你都应当使用**计算属性**。

watch:

​	虽然计算属性在大多数情况下更合适，但有时也需要一个自定义的侦听器。这就是为什么 Vue 通过 `watch` 选项提供了一个更通用的方法，来响应数据的变化。当需要在数据变化时执行异步或开销较大的操作时，这个方式是最有用的。

​	在这个示例中，使用 `watch` 选项允许我们执行异步操作 (访问一个 API)，限制我们执行该操作的频率，并在我们得到最终结果前，设置中间状态。这些都是计算属性无法做到的。



![1556850510779](assets/1556850510779.png)





### 条件渲染，列表渲染，class与style绑定



条件渲染，v-if  v-else v-elseif  v-show

![1556850971347](assets/1556850971347.png)

当count 执行 v-if的div，其他失效

![1556851077097](assets/1556851077097.png)



两者区别：



列表渲染，v-for；

![1556851384899](assets/1556851384899.png)

条件渲染和列表渲染同时使用：

![1556851408167](assets/1556851408167.png)



class与style绑定



v-bind：

![1556851454978](assets/1556851454978.png)



![1556851492718](assets/1556851492718.png)

![1556851501764](assets/1556851501764.png)

单横线，单引号，驼峰

![1556851579979](assets/1556851579979.png)

![1556851602965](assets/1556851602965.png)





![1556851657513](assets/1556851657513.png)

# 3vue核心技术：



认识vue-cli

![1556861051124](assets/1556861051124.png)

安装：npm install -g @vue/cli



![1556861397551](assets/1556861397551.png)

#### vue create hello



![1556861510792](assets/1556861510792.png)

默认

手动





![1556861943670](assets/1556861943670.png)



npm run serve







#### vue ui







## 组件化思想：

![1556862351500](assets/1556862351500.png)





![1556862376244](assets/1556862376244.png)



![1556862411696](assets/1556862411696.png)



## 风格指南

![1556862463387](assets/1556862463387.png)



<https://cn.vuejs.org/v2/style-guide/>





## vue-router

#### 定义组件



![1556864138048](assets/1556864138048.png)



#### 添加

![1556864054977](assets/1556864054977.png)



![1556864108253](assets/1556864108253.png)







#### app.vue

![1556864087025](assets/1556864087025.png)





## 单项数据流



![1556864681937](assets/1556864681937.png)



vuex介绍 



![1556864765977](assets/1556864765977.png)



![1556864774855](assets/1556864774855.png)





![1556864803843](assets/1556864803843.png)

state：





mutations：



info：添加事件

![1556864890199](assets/1556864890199.png)



info：引入store

 ![1556864932210](assets/1556864932210.png) 



store

![1556864988844](assets/1556864988844.png)



 info

![1556865015819](assets/1556865015819.png)



传递到about组件

![1556865098581](assets/1556865098581.png)





## 如何进行调试：

1，console.log()/error（）

2，alert（）点击确定执行后面 阻塞的行为

3，添加关键词debugger

![1556868367089](assets/1556868367089.png)

![1556868650897](assets/1556868650897.png)

![1556868666108](assets/1556868666108.png)

4



![1556868698405](assets/1556868698405.png)





![1556868758792](assets/1556868758792.png)





![1556868900474](assets/1556868900474.png)





# 4集成vue



![1556868985118](assets/1556868985118.png)







![1556869055448](assets/1556869055448.png)





![1556869080824](assets/1556869080824.png)





git --version

git clone http~~~

ls

git status

![1556869517807](assets/1556869517807.png)



git branch -a

git branch

touch test.txt

git status

![1556869567911](assets/1556869567911.png)



git add .

git commit -m "..."

git remote -v





![1556869585184](assets/1556869585184.png)



git push origin master



git branch -a

git checkout -b dev 创建新的分支

![1556869684534](assets/1556869684534.png)

ni test1.txt

git status

git add name

git commit -m "dev"

git push origin dev

  ![1556869746459](assets/1556869746459.png)



git branch -a

![1556869799520](assets/1556869799520.png)



git checkout master

git merge dev 合并分支





![1556869842566](assets/1556869842566.png)





删除分支 git branch -D dev

删除远程dev分支 git push origin :dev

退回之前的版本 git reset --hard head^





![1556869980356](assets/1556869980356.png)



 日志git log   git reflog

git reset --hard head^

git log

git reflog

git reset --hard HEAD@{1}

![1556870056755](assets/1556870056755.png) 





## 单页面demo1



创建demo.vue

vue serve demo.vue 



上列表； 

v-for     v-for="(item,index) in lists"   :key="index"

choose（）  @click="choose(index)"   

active 切换     :class="{active:index==current}"

按钮；add（）

   <button @click="add()"></button>

下列表；

v-for \<li v-for="(item,index) in targets" :key="index">{{item}}\</li>



bug:

1默认未选择，添加后，删除样式

push后 this.current=‘’ ‘’

![1556960388195](assets/1556960388195.png)

2，连续点击添加空，

![1556960462187](assets/1556960462187.png)

完整代码：



![1556960497180](assets/1556960497180.png)





![1556960470972](assets/1556960470972.png)



## 如何高仿别人的app？

观察结构

head 用了那些库

js用了哪些库

根据class，找到库

source:



移动端

头部尾部，看到加载了那些库

###### chrome 样式 格式化 format {}

总结：



![1556964476538](assets/1556964476538.png)





## demo2





vue ui 

不保存预设

![1556965366929](assets/1556965366929.png)



添加div



配置 router

app.js





### vuex



![1556971514238](assets/1556971514238.png)



### add.js



add，传递数据到list，跨组件用vuex（引入，state，mutations）

![1556971575022](assets/1556971575022.png)





引入store

改变store store.commit

![  1556971666658](assets/1556971666658.png)

![1556971740860](assets/1556971740860.png)





list

 引入 store

### list



![1556993349093](assets/1556993349093.png)







### login

v-if:



![1556997579786](assets/1556997579786.png)

  



![1556997555080](assets/1556997555080.png)

![1556998628196](assets/1556998628196.png)

![1556997524615](assets/1556997524615.png)





![1556997603771](assets/1556997603771.png)

密码校验：

![1556997644413](assets/1556997644413.png)



密码 text==》password

![1556997729647](assets/1556997729647.png)



点击登录清空 回到登录

![1556997794641](assets/1556997794641.png)s





验证：

![1556997847299](assets/1556997847299.png)

![1556997862484](assets/1556997862484.png)





![1556997898206](assets/1556997898206.png)





### 样式：

home

![1556997959994](assets/1556997959994.png)



![1556998055563](assets/1556998055563.png)



![1556998076431](assets/1556998076431.png)

![1556998183479](assets/1556998183479.png)



app.js

![1556998026123](assets/1556998026123.png)





router

![1556998232055](assets/1556998232055.png)









## 回顾：

![1557000907943](assets/1557000907943.png)



![1557000932590](assets/1557000932590.png)

![1557000946515](assets/1557000946515.png)

npm run build

dist

创建vue.config.js



vue-cli的webpack

环境变量

https://cli.vuejs.org/zh/guide/webpack.html#简单的配置方式





![1557002740749](assets/1557002740749.png)