

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