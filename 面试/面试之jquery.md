1 jQuery是什么？

2 jquery与JavaScript的关系，jQuery会取代JavaScript吗？

##### 3 如何使用jQuery库？

4 CDN（内容分发网络）是什么？

5 如何使用jQuery CDN？

6 如何在CDN网络不可访问情况下，能自动访问网站的jQuery文件？

7 同版本的jQuery.js文件和jQuery.min.js有何不同？

8 何时使用jquery.js，何时使用jquery.min.js？

9  jQuery.vsdoc.js文件是什么?

10 jQuery的基本语法如何解释？

11 在jQuery中，"$"符号代表什么？

12 为何要使用jQuery.noConflict（）？

13 同一个页面中，能否加载多个个document.ready事件？





##### 1 jQuery是什么？

jQuery是javascript编写一个可重用的JavaScript库。 

不使用jQuery设置UI文本的JavaScript代码如下： 

```
document.getElementById("txt1").value = "hello"; 
```

用jQuery类库后的的JavaScript代码如下： 

```
$("#txt1").val("Hello"); 
```

可见，在使用jQuery类库后的JavaScript代码明显简洁了很多，也更符合IT行业特点：短、平、快。 

##### 2 jquery与JavaScript的关系，jQuery会取代JavaScript吗？

- JavaScript：是一门Web最流行的脚本语言。
- jQuery: 是一个优秀的Javascript框架。它是轻量级的js库 ，它兼容CSS3，还兼容各种浏览器（IE 6.0+, FF 1.5+, Safari  2.0+, Opera 9.0+）。

jQuery是并不是要取代的JavaScript。使用jQuery使Web开发变得简单。 

##### 3 如何使用jQuery库？

从jquery.com下载的jquery.js文件（最新的jQuery版本V1.11.1或V2.1.1）。 jQuery的文件规则，如"jquery-1.4.1.j s"，其中1.4.1是JS文件的版本的版本号。 

在开发Web程序前，需要包含的JavaScript，如图下面的代码：

```
<script src="http://code.jquery.com/jquery-1.9.1.min.js" type="text/javascript"></script>
```

##### 



##### 4 CDN（内容分发网络）是什么？

在开发Web页面，考虑最多的问题之一是页面在客户端电脑的响应：时间越短，用户体验越好。

而制约用户体验的关键因素之一是浏览器下载Web文件大小，包括*.html、图片、*.js、*.css等文件。

为了最大化复用和节约带宽，故CDN应运而生：其基本思路是尽可能避开互联网上有可能影响数据传输速度和稳定性的瓶颈和环节，使内容传输的更快、更稳定。其目的是使用户可就近取得所需内容，解决 Internet网络拥挤的状况，提高用户访问网站的响应速度。 

##### 5 如何使用jQuery CDN？

- （1）推荐使用官方的CDN节点，使用代码如下：

  ```
  <script src="//code.jquery.com/jquery-1.11.0.min.js"></script> 
  <script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script> 
  ```

- 2）还有Google提供的jQuery CDN：

  ```
  <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script> 
  ```

- （3）同时微软也提供了jQuery CDN的节点：

  ```
  <script type="text/javascript" src="http://ajax.microsoft.com/ajax/jquery/jquery-1.9.1.min.js"> </script>
  ```

##### 6 如何在CDN网络不可访问情况下，能自动访问网站的jQuery文件？

一般情况下，CDN网络节点是可靠的。但是偶尔也有失灵的时候，故为了提供双保险，可进行判断网络加载CDN失败，则自动加载网站上的jQuery, 示例代码如下：

```
<script type="text/javascript" src="http:/ajax.microsoft.com/ajax/jquery/jquery-1.9.1.min.js"></script> 
<script type="text/javascript">
if (typeof jQuery == 'undefined')  
{  
    document.write(unescape("%3Cscript src='Scripts/jquery.1.9.1.min.js' type='text/javascript'%3E%3C/script%3E"));  
}
</script> 
```

##### 7 同版本的jQuery.js文件和jQuery.min.js有何不同？

- 相同：这两个文件提供相同的jQuery的功能，即在函数调用上没有区别。 
- 不同：jQuery.js文件，适合让程序员阅读。jQuery.min.js文件，通过压缩和删除所有的空格，以节省带宽和空间，使得文件更小，用于网络传输，不适合程序员阅读。 

##### 8 何时使用jquery.js，何时使用jquery.min.js？

- 开发调试场景下：用jQuery.js文件，因为你想调试，能够看到javascript代码。
- 生产部署环境下：用jQuery.min.js文件，可减少网络宽度，加快网页加载速度。

##### 9 jQuery.vsdoc.js文件是什么?

*.vsdoc.js文件是用来在微软的开发环境Visual Studio下使用的，方便得获得jQuery的智能感知，当你输入jQuery函授后，会自动提示函数的类型、函数使用说明、函数参数等等。如果在VS下用jQuery开发Web程序，则vsdoc.js文件会大大的提高开发效率。 

##### 10 jQuery的基本语法如何解释？

jQuery的语法结构可以分为四部分：

- 1、默认情况下，所有Jquery的命令开始以一个"$"符号。
- 2、其次是HTML元素的选择。例如下面是我们通过ID"txt1"选择一个HTML文本框。
- 3、接着由点（.）分隔。这个操作者将分离的元素和该元素的动作(函数)。
- 4、最后什么样的函数(动作)。

##### 11 在jQuery中，"$"符号代表什么？

在jQuery中，"$"符号是一个jQuery的别名，默认的jQuery类库以$开头。 

##### 12 为何要使用jQuery.noConflict（）？

有很多类似jQuery一样的类库，如MooTools, Backbone, Sammy, Cappuccino, Knockout 。这些类库中，有的也使用了$符号，如果同时使用，则会导致命名冲突。 

为了解决这个冲突，需要用到jQuery.noConflict()，这样就不依赖$这个默认符号了。例如：

```
jQuery.noConflict();  
(function($){

})(jQuery);
```

##### 13 同一个页面中，能否加载多个个document.ready事件？

可以。 











- 44 JQuery的源码看过吗？能不能简单概况一下它的实现原理？

- 45 jQuery.fn的init方法返回的this指的是什么对象？为什么要返回this？

- 46 jquery中如何将数组转化为json字符串，然后再转化回来？

- 47 jQuery 的属性拷贝(extend)的实现原理是什么，如何实现深拷贝？ 

- 48 jquery.extend 与 jquery.fn.extend的区别？

- 49 jQuery 的队列是如何实现的？队列可以用在哪些地方？

- 50 谈一下Jquery中的bind(),live(),delegate(),on()的区别？

- 51 JQuery一个对象可以同时绑定多个事件，这是如何实现的？

- 52  是否知道自定义事件。jQuery里的fire函数是什么意思，什么时候用？

- 53 jQuery 是通过哪个方法和 Sizzle 选择器结合的？（jQuery.fn.find()进入Sizzle）

- 针对 jQuery性能的优化方法？

- Jquery与jQuery UI 有啥区别？

  ```
  *jQuery是一个js库，主要提供的功能是选择器，属性修改和事件绑定等等。
  
  *jQuery UI则是在jQuery的基础上，利用jQuery的扩展性，设计的插件。
   提供了一些常用的界面元素，诸如对话框、拖动行为、改变大小行为等等
  ```

- JQuery的源码看过吗？能不能简单说一下它的实现原理？

- jquery 中如何将数组转化为json字符串，然后再转化回来？

jQuery中没有提供这个功能，所以你需要先编写两个jQuery的扩展：

```
    $.fn.stringifyArray = function(array) {
        return JSON.stringify(array)
    }

    $.fn.parseArray = function(array) {
        return JSON.parse(array)
    }

    然后调用：
    $("").stringifyArray(array)
```

- jQuery和Zepto的区别？各自的使用场景？

- 针对 jQuery 的优化方法？

  ```
  *基于Class的选择性的性能相对于Id选择器开销很大，因为需遍历所有DOM元素。
  
  *频繁操作的DOM，先缓存起来再操作。用Jquery的链式调用更好。
   比如：var str=$("a").attr("href");
  
  *for (var i = size; i < arr.length; i++) {}
   for 循环每一次循环都查找了数组 (arr) 的.length 属性，在开始循环的时候设置一个变量来存储这个数字，可以让循环跑得更快：
   for (var i = size, length = arr.length; i < length; i++) {}
  ```

- Zepto的点透问题如何解决？

- jQueryUI如何自定义组件?

- 需求：实现一个页面操作不会整页刷新的网站，并且能在浏览器前进、后退时正确响应。给出你的技术实现方案？

- 如何判断当前脚本运行在浏览器还是node环境中？（阿里）

  ```
  通过判断Global对象是否为window，如果不为window，当前脚本没有运行在浏览器中
  ```

- 移动端最小触控区域是多大？

- jQuery 的 slideUp动画 ，如果目标元素是被外部事件驱动, 当鼠标快速地连续触发外部元素事件, 动画会滞后的反复执行，该如何处理呢?

JQuery一个对象可以同时绑定多个事件，这是如何实现的？







**12. jQuery获取的dom对象和原生的dom对象有何区别？**

js原生获取的dom是一个对象，jQuery对象就是一个数组对象，其实就是选择出来的元素的数组集合，所以说他们两者是不同的对象类型不等价。

原生DOM对象转jQuery对象：

```
`var` `box = document.getElementById(``'box'``);``var` `$box` `= $(box);`
```

jQuery对象转原生DOM对象：

```
`var` `$box` `= $(``'#box'``);``var` `box = ``$box``[0];`
```

**13. jQuery如何扩展自定义方法**

```
`(jQuery.fn.myMethod=``function` `() {``       ``alert(``'myMethod'``);``})``// 或者：``(``function` `($) {``        ``$.fn.extend({``             ``myMethod : ``function` `() {``                  ``alert(``'myMethod'``);``             ``}``        ``})``})(jQuery)`
```

目前来看公司面试的问题还是比较基础的，但是对于某些只追求会用并不研究其原理的同学来说可能就没那么容易了。所以大家不仅要追求学习的广度，更要追求深度。

OK，希望自己能早日拿到心仪的offer.

