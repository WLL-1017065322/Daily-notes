**## 在网页中会引用哪些常见的静态资源？**

\+ JS

 \- .js  .jsx  .coffee  .ts（TypeScript  类 C# 语言）

\+ CSS

 \- .css  .less   .sass  .scss

\+ Images

 \- .jpg   .png   .gif   .bmp   .svg

\+ 字体文件（Fonts）

 \- .svg   .ttf   .eot   .woff   .woff2

\+ 模板文件

 \- .ejs   .jade  .vue【这是在webpack中定义组件的方式，推荐这么用】





**## 网页中引入的静态资源多了以后有什么问题？？？**

\1. 网页加载速度慢， 因为 我们要发起很多的二次请求；

\2. 要处理错综复杂的依赖关系

**## 如何解决上述两个问题**

\1. 合并、压缩、精灵图、图片的Base64编码

\2. 可以使用之前学过的requireJS、也可以使用webpack可以解决各个包之间的复杂依赖关系；

**## 什么是webpack?**

webpack 是前端的一个项目构建工具，它是基于 Node.js 开发出来的一个前端工具；

**## 如何完美实现上述的2种解决方案**

\1. 使用Gulp， 是基于 task 任务的；

\2. 使用Webpack， 是基于整个项目进行构建的；

\+ 借助于webpack这个前端自动化构建工具，可以完美实现资源的合并、打包、压缩、混淆等诸多功能。

\+ 根据官网的图片介绍webpack打包的过程

\+ [webpack官网](http://webpack.github.io/)

**## webpack安装的两种方式**

**\1. 运行`npm i webpack -g`全局安装webpack，这样就能在全局使用webpack的命令**

**\2. 在项目根目录中运行`npm i webpack --save-dev`安装到项目依赖中**

**## 初步使用webpack打包构建列表隔行变色案例**

\1. 运行`npm init`初始化项目，使用npm管理项目中的依赖包

\2. 创建项目基本的目录结构

\3. 使用`cnpm i jquery --save`安装jquery类库

\4. 创建`main.js`并书写各行变色的代码逻辑：

\```

​    // 导入jquery类库

​    import $ from 'jquery'

​    // 设置偶数行背景色，索引从0开始，0是偶数

​    $('#list li:even').css('backgroundColor','lightblue');

​    // 设置奇数行背景色

​    $('#list li:odd').css('backgroundColor','pink');

\```

\5. 直接在页面上引用`main.js`会报错，因为浏览器不认识`import`这种高级的JS语法，需要使用webpack进行处理，webpack默认会把这种高级的语法转换为低级的浏览器能识别的语法；

\6. 运行`webpack 入口文件路径 输出文件路径`对`main.js`进行处理：

\```

webpack src/js/main.js dist/bundle.js







```
npm uninstall -g webpack-cli
# 注释给我这种小白提供参考
# 卸载 uninstall  可以简写成 un  
# 全局 -g 的完整写法是 --global
# 现在问题来了这样真的卸载了webpack-cli吗？
# 答案是没有。到现在为止我还没有发现那个webpack-cli是全局安装的，至少官方文档没看到。
# 那就看下面怎么删除局部webpack-cli
```





<https://www.jianshu.com/p/a55fb5bf75e1>





当输入命令：webpack .\src\main.js .\dist\bundle.js

报错如下：



![img](https:////upload-images.jianshu.io/upload_images/3675862-2718b7df4c33577d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/638/format/webp)

来自本地

这是为什么呢？原因是我的webpack版本过高，原来的命令已经不适用了

如下查询版本号：



![img](https:////upload-images.jianshu.io/upload_images/3675862-87646b47da819fc6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/245/format/webp)

来自本地

那应该如何解决?

更换打包命令为: webpack ./src/main.js -o ./dist/bundle.js

其中 bundle.js是打包后生成的文件的文件名

![img](https:////upload-images.jianshu.io/upload_images/3675862-66aa44e2b81609cf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

来自本地

可以看到main.js已经被打包为了bundle.js文件，但是，这个并没有打包成功！

 因为打包的时候没有出现红色的error了，但是还有黄色的警告，如下图.



![img](https:////upload-images.jianshu.io/upload_images/3675862-e065ddf6151d3e74.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

来自本地

黄色警告:是因为webpack4引入了模式,有开发模式,生产模式,无这三个状态

可以看到末尾并没有生成我们所打包的main.js的信息

黄色部分的警告的意思是，没有设置模式,有开发模式和生产模式两种，

接下来，找到package.json.添加上”dev”和”build”这两个信息以及他们的值：

  “scripts”: {

​    “test”: “echo \”Error: no test specified\” && exit 1”,

   "dev":"webpack --mode development",

​    "bulid":"webapck --mode production"

  },

再全局安装 webpack-cli：

npm i --save-dev webpack-cli -g

安装完成后, 输入命令  npm run dev



![img](https:////upload-images.jianshu.io/upload_images/3675862-8c02fd8ff0c54bff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/698/format/webp)

来自本地

但是结果还是有很多报错，

原因是，你输入命令 npm run dev 的时候，会默认打包src文件夹下的index.js文件，打包完成后是main.js文件(放在dist)，你有没有发现我们一开始安装webpack的时候并没有这个文件生成，所以更别提什么index.js文件了，所以这些我们需要手动创建

我们先创建src文件，还有一个dist文件，存放默认的打包生成的文件, 然后在src里再创建index.js文件

重新输入命令：npm run dev ，如下图，dist文件夹里会自动生成一个mian.js文件，并且无任何警告或报错出现，说明我们的问题已经解决了



![img](https:////upload-images.jianshu.io/upload_images/3675862-fd17decf5be9d792.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/329/format/webp)

npm run dev后无报错



![img](https:////upload-images.jianshu.io/upload_images/3675862-b6d349958b29fa22.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/264/format/webp)

看项目

在看main.js尾部，也把index.js的代码放进去了



![img](https:////upload-images.jianshu.io/upload_images/3675862-57d81177cfd46be5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

main.js尾部代码

到了这一步，打包main.js(不是默认的文件的时候),，黄色警告还是出现!那么应该怎么解决呢？那就是webpack的版本问题，命令不同了

应该使用如下命令进行打包：

webpack ./src/main.js -o ./dist/bundle.js --mode development



![img](https:////upload-images.jianshu.io/upload_images/3675862-3ecc4eec6b3cff64.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/705/format/webp)

来自本地

很神奇吧? 黄色警告没有了

查看打包后的bundle.js文件，末尾也出现了main.js代码了



![img](https:////upload-images.jianshu.io/upload_images/3675862-d849986ba30fb761.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)

来自本地



注意：运行npm run dev后，index.js打包正常，但是自己手动创建的main.js打包后虽然出现bundle.js，但还是会报黄色警告：The 'mode' option has not been set, webpack will fallback to 'production' for this value.....，解决此问题，只需新建一个webpack.config.js，在module.exports配置对象里加上mode: 'development'，再打包就显示正常了

作者：尹莫一

链接：https://www.jianshu.com/p/a55fb5bf75e1

来源：简书

简书著作权归作者所有，任何形式的转载都请联系作者获得授权并注明出处。