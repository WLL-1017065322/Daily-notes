### vue-cli项目打包出现空白页和路径错误问题

vue-cli项目打包：

\1. 命令行输入：npm  run  build

​    打包出来后项目中就会多了一个文件夹dist，这就是我们打包过后的项目。

![img](../../../../../%E6%89%93%E5%8C%85/web%E9%A1%B9%E7%9B%AE/github/noteBlog/%E5%8D%9A%E5%AE%A2/assets/1202246-20171121094253805-1852331364.png)



#### 第一个问题，文件引用路径。

我们直接运行打包后的文件夹中的index.html文件，会看到网页一片空白，f12调试，全是css，js路径引用错误的问题。

解决：到config文件夹中打开index.js文件。

文件里面有两个assetsPublicPath属性，更改第一个，也就是更改build里面的assetsPublicPath属性：

![img](../../../../../%E6%89%93%E5%8C%85/web%E9%A1%B9%E7%9B%AE/github/noteBlog/%E5%8D%9A%E5%AE%A2/assets/1202246-20171121094900196-325897431.png)

assetsPublicPath属性作用是指定编译发布的根目录，**‘/’指的是项目的根目录 ，’./’指的是当前目录。**

**改好之后重新打包项目，运行index.html文件，我们可以看到没有报错了。但是router-view里面的内容却出不来了。**

 

#### **第二个问题：router-view中的内容显示不出来。**路由history模式。

这个坑是当你使用了路由之后，**在没有后端配合的情况下就手贱打开路由history模式的时候**，打包出来的文件也会是一片空白的情况，

很多人踩这个坑的时候花了很多时间，网上的教程基本上都是说的第一个坑，这个坑很少有人提起。

**![img](../../../../../%E6%89%93%E5%8C%85/web%E9%A1%B9%E7%9B%AE/github/noteBlog/%E5%8D%9A%E5%AE%A2/assets/1202246-20171121095445961-1591205997.png)**

解决：`// mode: 'history',//将这个模式关闭就好`

这里并不是说不能打开这个模式，这个模式需要后端设置的配合，详情可以看：[路由文档](https://router.vuejs.org/zh-cn/essentials/history-mode.html)