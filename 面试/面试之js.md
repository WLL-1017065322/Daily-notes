11JavaScript：
    数据类型、运算、对象、Function、继承、闭包、作用域、原型链、事件、RegExp、JSON、Ajax、
    DOM、BOM、内存泄漏、跨域、异步装载、模板引擎、前端MVC、路由、模块化、Canvas、ECMAScript 6、Nodejs



1.DOM 和 BOM 的区别是什么？

2.JavaScript 中的事件处理如何运行

3.如何在 JavaScript 中检测触摸事件？

 4 JavaScript的数据类型

5 JavaScript的闭包

6 new 操作符到底做了什么

7 改变函数内部this指针的指向函数

8 JavaScript的作用域和作用域链

9 sJavaScript的继承

10 JavaScript变量提升

11 JavaScript事件模型

12 内存泄漏

13 浏览器的垃圾回收机制

14 同源策略

15 跨域的几种方式

16 异步和同步

17 JavaScript的值类型和引用类型

18 浏览器js解析引擎的两个队列

19 封装cookie的添加，删除，查询方法

20 事件委托机制

21 JavaScript 基础问题

22 .解释 JavaScript 并发模型

23 new 关键字在 JavaScript 中有什么作用？

24 JavaScript 中有哪些不同的函数调用模式？ 详细解释。

25 .解释任一即将发布新的 ECMAScript 提案。

26 .JavaScript 中的迭代器（iterators）和迭代（iterables）是什么？ 你知道什么是内置迭代器吗？

27 .为什么 JavaScript classes(类)被认为是坏的或反模式？

28 如何在 JSON 中序列化以下对象

29 .你熟悉 Typed Arrays 吗？ 如果熟悉，请解释他们与 JavaScript 中的传统数组相比的异同？

30. 默认参数是如何工作？

31 JavaScript 前端应用设计问题

======



1 介绍js的数据类型。

2 介绍js有哪些内置对象？

3 说几条写JavaScript的基本规范

4 JavaScript原型，原型链 ? 有什么特点？

5 JavaScript有几种类型的值？，你能画一下他们的内存图吗？

6 Javascript如何实现继承？

7 JavaScript继承的几种实现方式？

8 javascript创建对象的几种方式？

9 Javascript作用链域?

10 谈谈This对象的理解。

11 eval是做什么的？

12 什么是window对象? 什么是document对象?

13 null，undefined 的区别？

14 写一个通用的事件侦听器函数。

15 ["1", "2", "3"].map(parseInt) 答案是多少？

16 事件是？IE与火狐的事件机制有什么区别？ 如何阻止冒泡？捕获

 17 什么是闭包（closure），为什么要用它？

18 javascript 代码中的"use strict";是什么意思 ? 使用它区别是什么？

19 如何判断一个对象是否属于某个类？

20 new操作符具体干了什么呢?

21用原生JavaScript的实现过什么功能吗？

22 Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？

23 json

24 [].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})` 能解释一下这段代码的意思吗？

25 js延迟加载的方式有哪些？

26 Ajax 是什么? 如何创建一个Ajax？

27 同步和异步的区别?

28 如何解决跨域问题?

29 页面编码和被请求的资源编码如果不一致如何处理？

30 模块化开发怎么做？

31 AMD（Modules/Asynchronous-Definition）、CMD（Common Module Definition）规范区别？

32 requireJS的核心原理是什么？（如何动态加载的？如何避免多次加载的？如何 缓存的？）

33 谈一谈你对ECMAScript6的了解？

34 ECMAScript6 怎么写class么，为什么会出现class这种东西? 

35 异步加载JS的方式有哪些？

36 documen.write和 innerHTML的区别

37 DOM操作——怎样添加、移除、移动、复制、创建和查找节点?

38 .call() 和 .apply() 的区别？

39 数组和对象有哪些原生方法，列举一下？

40 JS 怎么实现一个类。怎么实例化这个类

41 JavaScript中的作用域与变量声明提升？

42 如何编写高性能的Javascript？

43 那些操作会造成内存泄漏？

44 把 Script 标签 放在页面的最底部的body封闭之前 和封闭之后有什么区别？浏览器会如何解析它们？

45 移动端的点击事件的有延迟，时间是多久，为什么会有？ 怎么解决这个延时？（click 有 300ms 延迟,为了实现safari的双击事件的设计，浏览器要知道你是不是要双击操作。）

46 知道各种JS框架(Angular, Backbone, Ember, React, Meteor, Knockout...)么? 能讲出他们各自的优点和缺点么?

47 Underscore 对哪些 JS 原生对象进行了扩展以及提供了哪些好用的函数方法？

48 解释JavaScript中的作用域与变量声明提升？

49 那些操作会造成内存泄漏？

50 Node.js的适用场景？

51 (如果会用node)知道route, middleware, cluster, nodemon, pm2, server-side rendering么?

52 解释一下 Backbone 的 MVC 实现方式？

53 什么是"前端路由"?什么时候适合使用"前端路由"? "前端路由"有哪些优点和缺点?

54 知道什么是webkit么? 知道怎么用浏览器的各种工具来调试和debug代码么?

55 如何测试前端代码么? 知道BDD, TDD, Unit Test么? 知道怎么测试你的前端工程么(mocha, sinon, jasmin, qUnit..)?

56 前端templating(Mustache, underscore, handlebars)是干嘛的, 怎么用?

57 简述一下 Handlebars 的基本用法？

58 简述一下 Handlerbars 的对模板的基本处理流程， 如何编译的？如何缓存的？

59 用js实现千位分隔符?(来源：[前端农民工](http://div.io/topic/744)，提示：正则+replace)

60 检测浏览器版本版本有哪些方式？

61 What is a Polyfill? 

62 做的项目中，有没有用过或自己实现一些 polyfill 方案（兼容性处理方案）？

63 我们给一个dom同时绑定两个点击事件，一个用捕获，一个用冒泡。会执行几次事件，会先执行冒泡还是捕获？

64 事件的各个阶段



es6

1 Object.is() 与原来的比较操作符" ==="、" =="的区别？ 

2 let var const

3箭头函数



**1. DOM 和 BOM 的区别是什么？**

提示：BOM，DOM，ECMAScript 和 JavaScript 都是不同的东西。

**2.JavaScript 中的事件处理如何运行？**

如下图所示，我们有三个 div 元素。每个 div 都有一个与之关联的点击处理程序。处理程序执行以下任务：

- Outer div click 处理程序将 `hello outer` 打印到控制台。
- Inner div click 处理程序将 `hello inner` 打印到控制台。
- Innermost div click 处理程序将 hello innermost 打印到控制台。

编写一段代码来分配这些任务，以便在单击 innermost div 时始终打印以下序列？

```
hello inner` → `hello innermost` → `hello outer
```

![1.png](../../../../../%E6%89%93%E5%8C%85/web%E9%A1%B9%E7%9B%AE/github/%E7%AC%94%E8%AE%B0/%E9%9D%A2%E8%AF%95/assets/1548055553459132.png)

提示：事件捕获和事件冒泡



**3.如何在 JavaScript 中检测触摸事件？**

1. 你是否不看好检测设备对触摸事件的支持？如果是，为什么？
2. 比较触摸事件和点击事件。
3. 当设备同时支持触摸和鼠标事件时，你认为这些事件的正确事件顺序是什么或应该是什么？



 4 JavaScript的数据类型

基本数据类型：Number，String，Boolean，Undefined，Null

复杂数据类型：Object，Array，Function，RegExp，Date，Error

全局数据类型：Math

5 JavaScript的闭包

闭包简单的说就是一个函数能访问外部函数的变量，这就是闭包，比如说：

```js
function a(x){
       var tem=3;
      function b(y){
          console.log(x+y+(++tem));
     }
}
```

a函数中的b函数就是闭包了，b函数可以使用a函数的局部变量，参数，最典型的闭包应该是下面这样，将定义在函数中的函数作为返回值

```js
function a(x){
       var tem=3;
      function b(y){
          console.log(x+y+(++tem));
     }
return b;
}
```

闭包的缺点是，因为内部闭包函数可以访问外部函数的变量，所以外部函数的变量不能被释放，如果闭包嵌套过多，会导致内存占用大，要合理使用闭包。

6 new 操作符到底做了什么

  首先，new操作符为我们创建一个新的空对象，然后this变量指向该对象，

  其次，空对象的原型执行函数的原型，

  最后，改变构造函数内部的this的指向

代码如下：

```js
var obj={};
obj.__proto__=fn.prototype;
fn.call(obj);
```

7 改变函数内部this指针的指向函数

call和apply，假设要改变fn函数内部的this的指向，指向obj，那么可以fn.call(obj);或者fn.apply(obj);那么问题来了，call和apply的区别是什么，其是call和apply的区别在于参数，他们两个的第一个参数都是一样的，表示调用该函数的对象，apply的第二个参数是数组，是[arg1,arg2,arg3]这种形式，而call是arg1,arg2,arg3这样的形式。还有一个bind函数，

var bar=fn.bind(obj);那么fn中的this就指向obj对象了，bind函数返回新的函数，这个函数内的this指针指向obj对象。

8 JavaScript的作用域和作用域链

JavaScript的作用域指的是变量的作用范围，内部作用域由函数的形参，实参，局部变量，函数构成，内部作用域和外部的作用域一层层的链接起来形成作用域链，当在函数内部要访问一个变量的时候，首先查找自己的内部作用域有没有这个变量，如果没有就到外部的作用域中去查找，还是没有的话，就到在外面一层作用域中找，直到到window所在的作用域，每个函数在声明的时候就默认有一个外部作用域链存在了，比如：

```js
var t=4;
function foo(){
       var tem=12;
      funciton bar(){
       var temo=34;
       console.log(t+" "+tem+" "+temo);
      }
}
```

在bar函数中找t变量的过程就是，先到自己的内部作用域中找，发现没有找到，然后到bar所在的最近的外部环境中找，也就是foo的内部作用域，还是没有找到，再到window的作用域中找，结果找到了

9 sJavaScript的继承

```js
function A(name){  this.name=name; }
A.prototype.sayName=function(){ console.log(this.name); }
function B(age){ this.age=age; }
```

**原型继承**

```js
B.prototype=new A("mbj");  //被B的实例共享
var foo=new B(18);
foo.age;    //18,age是本身携带的属性
foo.name;   //mbj，等价于foo.__proto__.name
foo.sayName(); //mbj,等价于foo.__proto__.proto__.sayName()
foo.toString();  //"[object Object]",等价于foo.__proto__.__proto__.__proto__.toString();
```

这样B通过原型继承了A，在new B的时候，foo中有个隐藏的属性__proto__指向构造函数的prototype对象，在这里是A对象实例，A对象里面也有一个隐藏的属性__proto__,指向A构造函数的prototype对象，这个对象里面又有一个__proto__指向Object的prototype

这种方式的缺第一个缺点是所有子类共享父类实例，如果某一个子类修改了父类，其他的子类在继承的时候，会造成意想不到的后果。第二个缺点是在构造子类实例的时候，不能给父类传递参数。

构造函数继承

```js
function B(age,name){  this.age=age;A.call(this,name); }
var foo=new B(18,"wmy");
foo.name;     //wmy
foo.age;      //18
foo.sayName();   //undefined
```

采用这种方式继承是把A中的属性加到this上面，这样name相当于就是B的属性，sayName不在A的构造函数中，所以访问不到sayName。这种方法的缺点是父类的prototype中的函数不能复用。

**原型继承+构造函数继承**

```js
function B(age,name){  this.age=age;A.call(this,name); }
B.prototype=new A("mbj");
var foo=new B(18,"wmy");
foo.name;     //wmy
foo.age;      //18
foo.sayName();   //wmy
```

这样就可以成功访问sayName函数了，结合了上述两种方式的优点，但是这种方式也有缺点，那就是占用的空间更大了。



10 JavaScript变量提升

请看下面代码

```js
var bar=1;
function test(){
  console.log(bar);     //undeifned
  var bar=2; 
  console.log(bar);  //2
}
test();
```

为什么在test函数中会出现上述结果呢，这就是JavaScript的变量提升了，虽然变量bar的定义在后面，不过浏览器在解析的时候，会把变量的定义放到最前面，上面的test函数相当于

```js
function test(){
  var bar;
  console.log(bar);   //undefined
  bar=2; 
  console.log(bar);   //2
}
```

再看

```js
var foo=function(){  console.log(1); }
function foo(){  console.log(2); }
foo();  //结果为1
同样的，函数的定义也会到提升到最前面，上面的代码相当于
function foo(){  console.log(2); }
var foo;
foo=funciton(){ console.log(1); }
foo();   //1
```

11 JavaScript事件模型

原始事件模型，捕获型事件模型，冒泡事件模型，

原始事件模型就是ele.onclick=function(){}这种类型的事件模型

冒泡事件模型是指事件从事件的发生地（目标元素），一直向上传递，直到document，

捕获型则恰好相反，事件是从document向下传递，直到事件的发生地（目标元素）

IE是只支持冒泡事件模型的，下面是兼容各个浏览器的事件监听代码

```js
EventUtil={
  addListener:function(target,type,handler){
    if(target.addEventListener){
        target.addEventListener(type,handler);
    }else if(target.attachEvent){
        target.attach("on"+type,function(){
              handler.call(target);  //让handler中的this指向目标元素
        });
    }else{
        target["on"+type]=handler;
    }
  },
 removeListener:function(target,type,handler){   
      if(target.removeEventListener){    
        target.removeEventListener(type,handler);          
     }else if(target.detachEvent){
        target.detachEvent("on"+type,handler);
     }else{
        target["on"+type]=null;
     }
  },
 getEvent:function(e){      //获取事件对象
     var evt=window.event||e;
     return evt;
 },
 getTarget:function(e){      //获得目标对象
     var evt=EventUtil.getEvent(e);
     var target;
     if(evt.target){ target=evt.target;}
     else {target=evt.srcElement;}
     return target;
 },
 stopPropagation:function(e){  //停止冒泡
     var evt=EventUtil.getEvent(e);
     if(evt.stopPropagation) {evt.stopPropagation();}
     else {evt.cancelBubble=true;}
 },
 preventDefault:function(e){   //阻值默认行为的发生
     var evt=EventUtil.getEvent(e);
     if(evt.preventDefault){ evt.preventDefault(); }
     else {e.returnValue=false;}
 }
}
```

12 内存泄漏

内存泄漏指的是浏览器不能正常的回收内存的现象

13 浏览器的垃圾回收机制

垃圾收集器必须跟踪哪个变量有用哪个变量没用，对于不再有用的变量打上标记，以备将来收回其占用的内存，内存泄露和浏览器实现的垃圾回收机制息息相关， 而浏览器实现标识无用变量的策略主要有下两个方法：

**第一，引用计数法**

跟踪记录每个值被引用的次数。当声明一个变量并将引用类型的值赋给该变量时，则这个值的引用次数就是1。如果同一个值又被赋给另一个变量，则该值的引用次 数加1.相反，如果包含对这个值引用的变量又取得另外一个值，则这个值的引用次数减1.当这个值的引用次数变成0时，则说明没有办法访问这个值了，因此就 可以将其占用的内存空间回收回来。

```js
如： var a = {};     //对象{}的引用计数为1
     b = a;          //对象{}的引用计数为 1+1 
     a = null;       //对象{}的引用计数为2-1
```

所以这时对象{}不会被回收;

IE 6, 7 对DOM对象进行引用计数回收， 这样简单的垃圾回收机制，非常容易出现循环引用问题导致内存不能被回收， 进行导致内存泄露等问题，一般不用引用计数法。

**第二，标记清除法**

到2008年为止，IE,Firefox,Opera,Chrome和Safari的javascript实现使用的都是标记清除式的垃圾收集策略（或类似的策略），只不过垃圾收集的时间间隔互有不同。

标记清除的算法分为两个阶段，标记(mark)和清除(sweep). 第一阶段从引用根节点开始标记所有被引用的对象，第二阶段遍历整个堆，把未标记的对象清除。

14 同源策略

同源策略是浏览器有一个很重要的概念。所谓同源是指，域名，协议，端口相同。不同源的客户端脚本(javascript、ActionScript)在没明确授权的情况下，不能读写对方的资源。简单的来说，浏览器允许包含在页面A的脚本访问第二个页面B的数据资源，这一切是建立在A和B页面是同源的基础上。

15 跨域的几种方式

jsonp（利用script标签的跨域能力）跨域、websocket（html5的新特性，是一种新协议）跨域、设置代理服务器（由服务器替我们向不同源的服务器请求数据）、CORS（跨源资源共享，cross origin resource sharing）、iframe跨域、postMessage(包含iframe的页面向iframe传递消息)，document.domain跨域（比如：在一个文件中设置了document.domain="[http://qq.com](https://link.zhihu.com/?target=http%3A//qq.com)",那么另一个设置了document.domain="[http://qq.com](https://link.zhihu.com/?target=http%3A//qq.com)"的，他们两个就是同源）

16 异步和同步

同步指下一个程序的执行需要等到上一个程序执行完毕，也就是得出结果后下一个才能执行，

异步指的是上一个程序指向后，下一个程序不用等到上一个程序出结果就能执行，等上一个出结果了调用回调函数处理结果就好。

17 JavaScript的值类型和引用类型

JavaScript有两种类型的数据，值类型和引用类型，一般的数字，字符串，布尔值都是值类型，存放在栈中，而对象，函数，数组等是引用类型，存放在堆中，对引用类型的复制其实是引用复制，相当于复制着地址，对象并没有真正的复制。

```js
var a=5;var b=a;a=null;    //那么b是5
var a={},var b=a;b.name="mbj";
console.log(a.name);   //mbj，因为a，b指向同一个对象
a=null;console.log(typeof b);  //object，a=null，只是a不再指向该对象，但是这个对象还是在堆中确确实实的存在，b依然指向它。
```

18 浏览器js解析引擎的两个队列

请看下面代码

```js
console.log(1);                //(1)
setTimeout(function(){
      console.log(2);          //(2)
},0)
console.log(3);                //(3)
//输出的结果是1,3,2
```

可能会有人疑问，为什么不是输出1,2,3，这是因为上面代码在执行的时候被放到js解析引擎的同步队列中，然后先执行语句(1),在把setTimeout的回调函数放到异步队列，然后再执行语句(3),这样同步队列里面就没有代码需要执行了，然后在执行异步队列中的回调函数。

浏览器的js解析引擎在解析js代码的时候，把代码放入到两个队列，放入到同步队列中的代码会优先被执行，放入异步队列中的代码等同步队列中的代码被执行完了之后才会执行。需要异步等待回调的代码一般都是放到异步队列中的。

如果能明白下面代码，说明你对setTimeout，异步和同步队列掌握的比较好了

```js
for(var i=1;i<=4;i++){
	var time=setTimeout(function(i){
		clearTimeout(time);
                console.log(i);
	},1000,i);
}
//输出结果1,2,3
//PS:setTimeout的第三个以及第三个后面的参数都是分别传给setTimeout的回调函数的
```

19 封装cookie的添加，删除，查询方法

cookie是存储在浏览器端的，可以用于存储sessionID，也可以用于自动登陆，记住密码等，但是在浏览器端并没有官方的操作cookie的方法，下面我们来封装一下：

```js
CookieUtil=｛
    addCookie:function(key,value,options){
        var str=key+"="+escape(value);
        if(options.expires){
           var curr=new Date();   //options.expires的单位是小时
           curr.setTime(curr.getTime()+options.expires*3600*1000);
           options.expires=curr.toGMTString();
        }
        for(var k in options){   //有可能指定了cookie的path，cookie的domain
           str+=";"+k+"="+options[k];
        }
        document.cookie=str;
    },
    queryCookie:function(key){
      var cookies=document.cookie;
     //获得浏览器端存储的cookie,格式是key=value;key=value;key=value
      cookies+=";";
      var start=cookies.indexOf(key);
      if(start<=-1){ return null; }  //说明不存在该cookie
      var end=cookies.indexOf(";",start);
      var value=cookies.slice(start+key.length+1,end);
      return unescape(value);
    },
    deleteCookie:function(key){
      var value=CookieUtil.queryCookie(key);
      if(value===null){return false;}
      CookieUtil.addCookie(key,value,{expires:0});//把过期时间设置为0，浏览器会马上自动帮我们删除cookie
    }
｝
```

20 事件委托机制

事件委托指的是，不再事件的发生地设立监听函数，而是在事件发生地的父元素或者祖先元素设置监听器函数，这样可以大大提高性能，因为可以减少绑定事件的元素，比如：

```html
<ul>
 <li></li>
 <li></li>
 <li></li>
</ul>
```

要给li元素绑定click事件，使用事件委托机制的话，就只需要给ul绑定click事件就行了，这样就不需要给每个li'绑定click事件，减小内存占用，提高效率，有兴趣的童鞋可以去看看jQuery的live，bind，on，delegate函数的区别，这几个函数就采用了事件委托机制。







**21 JavaScript 基础问题**

**1.使以下代码正常运行：**

JavaScript 代码:

```JavaScript
const a = [1, 2, 3, 4, 5];
 
// Implement this
a.multiply();
 
console.log(a); // [1, 2, 3, 4, 5, 1, 4, 9, 16, 25]
```

**2.以下代码在 JavaScript 中返回 false 。 解释一下为什么会这样：**

JavaScript 代码:

```JavaScript
// false
0.2 + 0.1 === 0.3
```

3.JavaScript 中有哪些不同的数据类型？

提示：只有两种类型 – 主要数据类型和引用类型（对象）。 有 6 种主要类型。

**4.解决以下异步代码问题。**

检索并计算属于同一教室中每个学生的平均分数，其中一些ID为75。每个学生可以在一年内参加一门或多门课程。 以下 API 可用于检索所需数据。

JavaScript 代码:

```
`// GET LIST OF ALL THE STUDENTS``GET /api/students``Response:``[{``    ``"id"``: 1,``    ``"name"``: ``"John"``,``    ``"classroomId"``: 75``}]``// GET COURSES FOR GIVEN A STUDENT``GET /api/courses?filter=studentId eq 1``Response:``[{``   ``"id"``: ``"history"``,``   ``"studentId"``: 1``}, {``   ``"id"``: ``"algebra"``,``   ``"studentId"``: 1``},]``// GET EVALUATION FOR EACH COURSE``GET /api/evaluation/history?filter=studentId eq 1``Response:``{``    ``"id"``: 200,``    ``"score"``: 50,``    ``"totalScore"``: 100``}`
```

编写一个接受教室 ID 的函数，您将根据该函数计算该教室中每个学生的平均值。该函数的最终输出应该是具有平均分数的学生列表：

JavaScript 代码:

```JavaScript
[
  { "id": 1, "name": "John", "average": 70.5 },
  { "id": 3, "name": "Lois", "average": 67 },
]
```

使用普通的 **callbacks** ，**promises** ，**observables**，**generator** 或 **async-wait** 编写所需的函数。尝试使用至少 3 种不同的技术解决这个问题。

**5.使用 JavaScript Proxy 实现简单的数据绑定**

提示：ES Proxy 允许您拦截对任何对象属性或方法的调用。首先，每当更改底层绑定对象时，都应更新 DOM 。

**22 .解释 JavaScript 并发模型**

您是否熟悉 Elixir，Clojure，Java 等其他编程语言中使用的任何其他并发模型？

提示：查找事件循环，任务队列，调用栈，堆等。

**23 new 关键字在 JavaScript 中有什么作用？**

提示：在 JavaScript 中，`new` 是用于实例化对象的运算符。 这里的目的是了解知识广度和记忆情况。

另外，请注意 `[[Construct]]` 和 `[[Call]]`。

**24 JavaScript 中有哪些不同的函数调用模式？ 详细解释。**

提示：有四种模式，函数调用，方法调用，`.call()` 和 `.apply()`。

**25 .解释任一即将发布新的 ECMAScript 提案。**

提示：比如 2018 的 BigInt，partial 函数，pipeline 操作符 等。

**26 .JavaScript 中的迭代器（iterators）和迭代（iterables）是什么？ 你知道什么是内置迭代器吗？**

**27 .为什么 JavaScript classes(类)被认为是坏的或反模式？**

这是一个神话吗？它是否遭受了误传？是否有一些有用的用例？

**28 如何在 JSON 中序列化以下对象？**

如果我们将以下对象转换为 JSON 字符串，会发生什么？

JavaScript 代码:

```JavaScript
const a = {
    key1: Symbol(),
    key2: 10
}
// What will happen?
console.log(JSON.stringify(a));
```

**29 .你熟悉 Typed Arrays 吗？ 如果熟悉，请解释他们与 JavaScript 中的传统数组相比的异同？**

**30. 默认参数是如何工作？**

如果我们在调用 `makeAPIRequest` 函数时必须使用 `timeout` 的默认值，那么正确的语法是什么？

JavaScript 代码:

```JavaScript
function makeAPIRequest(url, timeout = 2000, headers) {   
    // Some code to fetch data
}
```

**15.解释 TCO – 尾调用优化（Tail Call Optimization）。 有没有支持尾调用优化的 JavaScript 引擎？**

提示：截至 2018 年，没有。

------

**31 JavaScript 前端应用设计问题**

**1.解释单向数据流和双向数据绑定。**

Angular 1.x 基于双向数据绑定，而 React，Vue，Elm 等基于单向数据流架构。

**2.单向数据流架构在哪些方面适合 MVC？**

MVC 拥有大约 50 年的悠久历史，并已演变为 MVP，MVVM 和 MV *。两者之间的相互关系是什么？如果 MVC 是架构模式，那么单向数据流是什么？这些竞争模式是否能解决同样的问题？

**3.客户端 MVC 与服务器端或经典 MVC 有何不同？**

提示：经典 MVC 是适用于桌面应用程序的 Smalltalk MVC。在 Web 应用中，至少有两个不同的数据 MVC 周期。

**4.使函数式编程与面向对象或命令式编程不同的关键因素是什么？**

提示：Currying（柯里化），point-free 函数，partial 函数应用，高阶函数，纯函数，独立副作用，record 类型（联合，代数数据类型）等。

**5.在 JavaScript 和前端的上下文中，函数式编程与响应式编程有什么关系？**

提示：没有正确答案。但粗略地说，函数式编程是关于小型编码，编写纯函数和响应式编程是大型编码，即模块之间的数据流，连接以 FP 风格编写的组件。 FRP – 功能响应式编程（ Functional Reactive Programming）是另一个不同但相关的概念。

**6.不可变数据结构（immutable data structures）解决了哪些问题？**

不可变结构是否有任何性能影响？ JS 生态系统中哪些库提供了不可变的数据结构？这些库的优点和缺点是什么？

提示：线程安全（我们真的需要在浏览器 JavaScript 中担心吗？），无副作用的函数，更好的状态管理等。

**7.大型应用程序是否应使用静态类型？**

1. 如何比较 TypeScript/Flow 与 Elm/ReasonML/PureScript 等 JS 转换语言？这些方法的优缺点是什么？
2. 选择特定类型系统的主要标准应该是什么？
3. 什么是类型推断（type inference）？
4. 静态类型语言和强类型语言有什么区别？在这方面 JavaScript 的本质是什么？
5. 有你知道的弱类型但静态类型的语言吗？有你知道的动态类型但强类型的语言吗？举例一二。

提示：Structural 与 Nominal 类型系统，类型稳健性，工具/生态系统支持，正确性超过方便。

**8.JavaScript 中有哪些杰出的模块系统（module systems ）？如何评价 ES 模块系统。**

列出在实现不同模块系统之间互操作所涉及的一些复杂性问题（主要对 ES 模块和 CommonJS 互操作感兴趣）

**9.HTTP/2 将如何影响 JavaScript 应用程序打包？**

列出 HTTP/2 与其上一个版本的基本区别。

**10.Fetch API 相对于传统的 Ajax 有哪些改进？**

1. 使用 Fetch API 有那些缺点/难点吗？
2. 哪些是Ajax 可以做的，而 fetch 不能做的？

**11.如何评论 pull-based 和 push-based 的反应系统。**

讨论概念，含义，用途等。

1. 在这个讨论中加入惰性和及早求值。
2. 然后在讨论中添加单数和复数值维度。
3. 最后，讨论值解析的同步和异步性质。
4. 为JavaScript中可用的每个组合提供示例。

提示：Observable 是惰性的，基于推送的复数值构造，同时具有 async/sync 调度程序。

**12.讨论与 Promise 相关的问题。**

提示：及早求值（eager evaluation），尴尬的取消机制，用 `then()` 方法伪装 `map()` 和 `flatMap()` 等。













## JavaScript

- 1 介绍js的数据类型。

  ```
  基本 Undefined、Null、Boolean、Number、String 复杂Object
  ```

  es6新增数据类型：Symbol：表示独一无二

  **null的typeof返回的是object**

-  值类型：

  ```
  字符串（String）、数值（Number）、布尔值（Boolean）、Undefined、Null 
  ```

  

- 三大引用类型：

  ```
  Object Array Function
  ```

  区别：

  ```
  2.值类型和引用类型的区别
  （1）值类型：1、占用空间固定，保存在栈中（当一个方法执行时，每个方法都会建立自己的内存栈，在这个方法内定义的变量将会逐个放入这块栈内存里，随着方法的执行结束，这个方法的内存栈也将自然销毁了。因此，所有在方法中定义的变量都是放在栈内存中的；栈中存储的是基础变量以及一些对象的引用变量，基础变量的值是存储在栈中，而引用变量存储在栈中的是指向堆中的数组或者对象的地址，这就是为何修改引用类型总会影响到其他指向这个地址的引用变量。）
  2、保存与复制的是值本身
  3、使用typeof检测数据的类型
  4、基本类型数据是值类型
  （2）引用类型：1、占用空间不固定，保存在堆中（当我们在程序中创建一个对象时，这个对象将被保存到运行时数据区中，以便反复利用（因为对象的创建成本通常较大），这个运行时数据区就是堆内存。堆内存中的对象不会随方法的结束而销毁，即使方法结束后，这个对象还可能被另一个引用变量所引用（方法的参数传递时很常见），则这个对象依然不会被销毁，只有当一个对象没有任何引用变量引用它时，系统的垃圾回收机制才会在核实的时候回收它。）
  2、保存与复制的是指向对象的一个指针
  3、使用instanceof检测数据类型
  4、使用new()方法构造出的对象是引用型
  ```

  

  

  #### 2 介绍js有哪些内置对象？

  ```
  Object 是 JavaScript 中所有对象的父对象
  
  数据封装类对象：Object、Array、Boolean、Number 和 String
  其他对象：Function、Arguments、Math、Date、RegExp、Error
  ```

  常用属性方法：Array：

  Array 对象方法:every,filter,findIndex,forEach，from，include。。

  Object

  Boolean

  Number 

   String

  。。

  

- 3 说几条写JavaScript的基本规范？

  ```
  1.不要在同一行声明多个变量。
  2.请使用 ===/!==来比较true/false或者数值
  3.使用对象字面量替代new Array这种形式
  4.不要使用全局函数。
  5.Switch语句必须带有default分支
  6.函数不应该有时候有返回值，有时候没有返回值。
  7.For循环必须使用大括号
  8.If语句必须使用大括号
  9.for-in循环中的变量 应该使用var关键字明确限定作用域，从而避免作用域污染。
  ```

- 4 JavaScript原型，原型链 ? 有什么特点？

  ```
  每个对象都会在其内部初始化一个属性，就是prototype(原型)，当我们访问一个对象的属性时，
  如果这个对象内部不存在这个属性，那么他就会去prototype里找这个属性，这个prototype又会有自己的prototype，
  于是就这样一直找下去，也就是我们平时所说的原型链的概念。
  关系：instance.constructor.prototype = instance.__proto__
  
  特点：
  JavaScript对象是通过引用来传递的，我们创建的每个新对象实体中并没有一份属于自己的原型副本。当我们修改原型时，与之相关的对象也会继承这一改变。
  
  
   当我们需要一个属性的时，Javascript引擎会先看当前对象中是否有这个属性， 如果没有的话，
   就会查找他的Prototype对象是否有这个属性，如此递推下去，一直检索到 Object 内建对象。
      function Func(){}
      Func.prototype.name = "Sean";
      Func.prototype.getInfo = function() {
        return this.name;
      }
      var person = new Func();//现在可以参考var person = Object.create(oldObject);
      console.log(person.getInfo());//它拥有了Func的属性和方法
      //"Sean"
      console.log(Func.prototype);
      // Func { name="Sean", getInfo=function()}
  ```

- 5 JavaScript有几种类型的值？，你能画一下他们的内存图吗？

  ```
  栈：原始数据类型（Undefined，Null，Boolean，Number、String） 
  堆：引用数据类型（对象、数组和函数）
  
  两种类型的区别是：存储位置不同；
  原始数据类型直接存储在栈(stack)中的简单数据段，占据空间小、大小固定，属于被频繁使用数据，所以放入栈中存储；
  引用数据类型存储在堆(heap)中的对象,占据空间大、大小不固定,如果存储在栈中，将会影响程序运行的性能；引用数据类型在栈中存储了指针，该指针指向堆中该实体的起始地址。当解释器寻找引用值时，会首先检索其
  在栈中的地址，取得地址后从堆中获得实体
  ```

  ![img](https:////www.runoob.com/wp-content/uploads/2016/06/687474703a2f2f7777772e77337363686f6f6c2e636f6d2e636e2f692f63745f6a735f76616c75652e676966.gif)

- ##### 6 Javascript如何实现继承？

  ```
  1、构造继承
  2、原型继承
  3、实例继承
  4、拷贝继承
  
  原型prototype机制或apply和call方法去实现较简单，建议使用构造函数与原型混合方式。
  
   function Parent(){
          this.name = 'wang';
      }
  
      function Child(){
          this.age = 28;
      }
      Child.prototype = new Parent();//继承了Parent，通过原型
  
      var demo = new Child();
      alert(demo.age);
      alert(demo.name);//得到被继承的属性
    }
  ```

- 7 JavaScript继承的几种实现方式？

  - 参考：[构造函数的继承](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_inheritance.html)，[非构造函数的继承](http://www.ruanyifeng.com/blog/2010/05/object-oriented_javascript_inheritance_continued.html)；

-  8 javascript创建对象的几种方式？

  ```
  javascript创建对象简单的说,无非就是使用内置对象或各种自定义对象，当然还可以用JSON；但写法有很多种，也能混合使用。
  
  
  1、对象字面量的方式   
  
      person={firstname:"Mark",lastname:"Yun",age:25,eyecolor:"black"};
  
  2、用function来模拟无参的构造函数
  
      function Person(){}
      var person=new Person();//定义一个function，如果使用new"实例化",该function可以看作是一个Class
      person.name="Mark";
      person.age="25";
      person.work=function(){
      alert(person.name+" hello...");
      }
      person.work();
  
  3、用function来模拟参构造函数来实现（用this关键字定义构造的上下文属性）
  
      function Pet(name,age,hobby){
         this.name=name;//this作用域：当前对象
         this.age=age;
         this.hobby=hobby;
         this.eat=function(){
            alert("我叫"+this.name+",我喜欢"+this.hobby+",是个程序员");
         }
      }
      var maidou =new Pet("麦兜",25,"coding");//实例化、创建对象
      maidou.eat();//调用eat方法
  
  
  4、用工厂方式来创建（内置对象）
  
       var wcDog =new Object();
       wcDog.name="旺财";
       wcDog.age=3;
       wcDog.work=function(){
         alert("我是"+wcDog.name+",汪汪汪......");
       }
       wcDog.work();
  
  
  5、用原型方式来创建
  
      function Dog(){
  
       }
       Dog.prototype.name="旺财";
       Dog.prototype.eat=function(){
       alert(this.name+"是个吃货");
       }
       var wangcai =new Dog();
       wangcai.eat();
  
  
  5、用混合方式来创建
  
      function Car(name,price){
        this.name=name;
        this.price=price; 
      }
       Car.prototype.sell=function(){
         alert("我是"+this.name+"，我现在卖"+this.price+"万元");
        }
      var camry =new Car("凯美瑞",27);
      camry.sell(); 
  ```

- ##### 9 Javascript作用链域?

  ```
  全局函数无法查看局部函数的内部细节，但局部函数可以查看其上层的函数细节，直至全局细节。
  当需要从局部函数查找某一属性或方法时，如果当前作用域没有找到，就会上溯到上层作用域查找，
  直至全局函数，这种组织形式就是作用域链。
  ```

- 10 谈谈This对象的理解。

  - this总是指向函数的直接调用者（而非间接调用者）；
  - 如果有new关键字，this指向new出来的那个对象；
  - 在事件中，this指向触发这个事件的对象，特殊的是，IE中的attachEvent中的this总是指向全局对象Window；

- 11 eval是做什么的？

  ```
  它的功能是把对应的字符串解析成JS代码并运行；
  应该避免使用eval，不安全，非常耗性能（2次，一次解析成js语句，一次执行）。
  由JSON字符串转换为JSON对象的时候可以用eval，var obj =eval('('+ str +')');
  ```

- 12 什么是window对象? 什么是document对象?

- 13 null，undefined 的区别？

  ```
  null        表示一个对象被定义了，值为“空值”；
  undefined   表示不存在这个值。
  
  
  typeof undefined
      //"undefined"
      undefined :是一个表示"无"的原始值或者说表示"缺少值"，就是此处应该有一个值，但是还没有定义。当尝试读取时会返回 undefined； 
      例如变量被声明了，但没有赋值时，就等于undefined
  
  typeof null
      //"object"
      null : 是一个对象(空对象, 没有任何属性和方法)；
      例如作为函数的参数，表示该函数的参数不是对象；
  
  注意：
      在验证null时，一定要使用　=== ，因为 == 无法分别 null 和　undefined
  
  
  再来一个例子：
  
      null
      Q：有张三这个人么？
      A：有！
      Q：张三有房子么？
      A：没有！
  
      undefined
      Q：有张三这个人么？
      A：没有！
  ```

  参考阅读：[undefined与null的区别](http://www.ruanyifeng.com/blog/2014/03/undefined-vs-null.html)

- 14 写一个通用的事件侦听器函数。

  ```
      // event(事件)工具集，来源：github.com/markyun
      markyun.Event = {
          // 页面加载完成后
          readyEvent : function(fn) {
              if (fn==null) {
                  fn=document;
              }
              var oldonload = window.onload;
              if (typeof window.onload != 'function') {
                  window.onload = fn;
              } else {
                  window.onload = function() {
                      oldonload();
                      fn();
                  };
              }
          },
          // 视能力分别使用dom0||dom2||IE方式 来绑定事件
          // 参数： 操作的元素,事件名称 ,事件处理程序
          addEvent : function(element, type, handler) {
              if (element.addEventListener) {
                  //事件类型、需要执行的函数、是否捕捉
                  element.addEventListener(type, handler, false);
              } else if (element.attachEvent) {
                  element.attachEvent('on' + type, function() {
                      handler.call(element);
                  });
              } else {
                  element['on' + type] = handler;
              }
          },
          // 移除事件
          removeEvent : function(element, type, handler) {
              if (element.removeEventListener) {
                  element.removeEventListener(type, handler, false);
              } else if (element.datachEvent) {
                  element.detachEvent('on' + type, handler);
              } else {
                  element['on' + type] = null;
              }
          },
          // 阻止事件 (主要是事件冒泡，因为IE不支持事件捕获)
          stopPropagation : function(ev) {
              if (ev.stopPropagation) {
                  ev.stopPropagation();
              } else {
                  ev.cancelBubble = true;
              }
          },
          // 取消事件的默认行为
          preventDefault : function(event) {
              if (event.preventDefault) {
                  event.preventDefault();
              } else {
                  event.returnValue = false;
              }
          },
          // 获取事件目标
          getTarget : function(event) {
              return event.target || event.srcElement;
          },
          // 获取event对象的引用，取到事件的所有信息，确保随时能使用event；
          getEvent : function(e) {
              var ev = e || window.event;
              if (!ev) {
                  var c = this.getEvent.caller;
                  while (c) {
                      ev = c.arguments[0];
                      if (ev && Event == ev.constructor) {
                          break;
                      }
                      c = c.caller;
                  }
              }
              return ev;
          }
      };
  ```

- 15 ["1", "2", "3"].map(parseInt) 答案是多少？

  ```
   [1, NaN, NaN] 因为 parseInt 需要两个参数 (val, radix)，
   其中 radix 表示解析时用的基数。
   map 传了 3 个 (element, index, array)，对应的 radix 不合法导致解析失败。
  
  ```

- ##### 16 事件是？IE与火狐的事件机制有什么区别？ 如何阻止冒泡？捕获

  ```
   1. 我们在网页中的某个操作（有的操作对应多个事件）。例如：当我们点击一个按钮就会产生一个事件。是可以被 JavaScript 侦测到的行为。
   2. 事件处理机制：IE是事件冒泡、Firefox同时支持两种事件模型，也就是：捕获型事件和冒泡型事件；
   3. ev.stopPropagation();（旧ie的方法 ev.cancelBubble = true;）
  ```

  ##### 17 什么是闭包（closure），为什么要用它？

  ```
  闭包是指有权访问另一个函数作用域中变量的函数，创建闭包的最常见的方式就是在一个函数内创建另一个函数，通过另一个函数访问这个函数的局部变量,利用闭包可以突破作用链域，将函数内部的变量和方法传递到外部。
  
  闭包的特性：
  
  1.函数内再嵌套函数
  2.内部函数可以引用外层的参数和变量
  3.参数和变量不会被垃圾回收机制回收
  
  //li节点的onclick事件都能正确的弹出当前被点击的li索引
   <ul id="testUL">
      <li> index = 0</li>
      <li> index = 1</li>
      <li> index = 2</li>
      <li> index = 3</li>
  </ul>
  <script type="text/javascript">
      var nodes = document.getElementsByTagName("li");
      for(i = 0;i<nodes.length;i+= 1){
          nodes[i].onclick = function(){
              console.log(i+1);//不用闭包的话，值每次都是4
          }(i);
      }
  </script>
  
  
  
  执行say667()后,say667()闭包内部变量会存在,而闭包内部函数的内部变量不会存在
  使得Javascript的垃圾回收机制GC不会收回say667()所占用的资源
  因为say667()的内部函数的执行需要依赖say667()中的变量
  这是对闭包作用的非常直白的描述
  
    function say667() {
      // Local variable that ends up within closure
      var num = 666;
      var sayAlert = function() {
          alert(num);
      }
      num++;
      return sayAlert;
  }
  
   var sayAlert = say667();
   sayAlert()//执行结果应该弹出的667
  ```

- 18 javascript 代码中的"use strict";是什么意思 ? 使用它区别是什么？

  ```
  use strict是一种ECMAscript 5 添加的（严格）运行模式,这种模式使得 Javascript 在更严格的条件下运行,
  
  使JS编码更加规范化的模式,消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为。
  默认支持的糟糕特性都会被禁用，比如不能用with，也不能在意外的情况下给全局变量赋值;
  全局变量的显示声明,函数必须声明在顶层，不允许在非函数代码块内声明函数,arguments.callee也不允许使用；
  消除代码运行的一些不安全之处，保证代码运行的安全,限制函数中的arguments修改，严格模式下的eval函数的行为和非严格模式的也不相同;
  
  提高编译器效率，增加运行速度；
  为未来新版本的Javascript标准化做铺垫。
  ```

- 19 如何判断一个对象是否属于某个类？

  ```
    使用instanceof （待完善）
     if(a instanceof Person){
         alert('yes');
     }
  ```

- 20 new操作符具体干了什么呢?

  ```
       1、创建一个空对象，并且 this 变量引用该对象，同时还继承了该函数的原型。
       2、属性和方法被加入到 this 引用的对象中。
       3、新创建的对象由 this 所引用，并且最后隐式的返回 this 。
  
  var obj  = {};
  obj.__proto__ = Base.prototype;
  Base.call(obj);
  ```

- 21用原生JavaScript的实现过什么功能吗？

-  22 Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？

  ```
  hasOwnProperty
  
  javaScript中hasOwnProperty函数方法是返回一个布尔值，指出一个对象是否具有指定名称的属性。此方法无法检查该对象的原型链中是否具有该属性；该属性必须是对象本身的一个成员。
  使用方法：
  object.hasOwnProperty(proName)
  其中参数object是必选项。一个对象的实例。
  proName是必选项。一个属性名称的字符串值。
  
  如果 object 具有指定名称的属性，那么JavaScript中hasOwnProperty函数方法返回 true，反之则返回 false。
  ```

  ### 

### 23 json

  

```
  JSON(JavaScript Object Notation) 是一种轻量级的数据交换格式。
  它是基于JavaScript的一个子集。数据格式简单, 易于读写, 占用带宽小
  如：{"age":"12", "name":"back"}
  
  JSON字符串转换为JSON对象:
  var obj =eval('('+ str +')');
  var obj = str.parseJSON();
  var obj = JSON.parse(str);
  
  JSON对象转换为JSON字符串：
  var last=obj.toJSONString();
  var last=JSON.stringify(obj);
```

- `24 [].forEach.call($$("*"),function(a){a.style.outline="1px solid #"+(~~(Math.random()*(1<<24))).toString(16)})` 能解释一下这段代码的意思吗？

- 25 js延迟加载的方式有哪些？

  ```
  defer和async、动态创建DOM方式（用得最多）、按需异步载入js
  ```

- 26 Ajax 是什么? 如何创建一个Ajax？

  ```
  ajax的全称：Asynchronous Javascript And XML。
  异步传输+js+xml。
  所谓异步，在这里简单地解释就是：向服务器发送请求的时候，我们不必等待结果，而是可以同时做其他的事情，等到有了结果它自己会根据设定进行后续操作，与此同时，页面是不会发生整页刷新的，提高了用户体验。
  
  (1)创建XMLHttpRequest对象,也就是创建一个异步调用对象
  (2)创建一个新的HTTP请求,并指定该HTTP请求的方法、URL及验证信息
  (3)设置响应HTTP请求状态变化的函数
  (4)发送HTTP请求
  (5)获取异步调用返回的数据
  (6)使用JavaScript和DOM实现局部刷新
  ```

- 27 同步和异步的区别?

  同步的概念应该是来自于OS中关于同步的概念:不同进程为协同完成某项工作而在先后次序上调整(通过阻塞,唤醒等方式).同步强调的是顺序性.谁先谁后.异步则不存在这种顺序性.

  同步：浏览器访问服务器请求，用户看得到页面刷新，重新发请求,等请求完，页面刷新，新内容出现，用户看到新内容,进行下一步操作。

  异步：浏览器访问服务器请求，用户正常操作，浏览器后端进行请求。等请求完，页面不刷新，新内容也会出现，用户看到新内容。

  （待完善）

- 28 如何解决跨域问题?

  ```
  jsonp、 iframe、window.name、window.postMessage、服务器上设置代理页面
  ```

- 29 页面编码和被请求的资源编码如果不一致如何处理？

- 30 模块化开发怎么做？

  [ 立即执行函数](http://benalman.com/news/2010/11/immediately-invoked-function-expression/),不暴露私有成员

  ```
      var module1 = (function(){
      　　　　var _count = 0;
      　　　　var m1 = function(){
      　　　　　　//...
      　　　　};
      　　　　var m2 = function(){
      　　　　　　//...
      　　　　};
      　　　　return {
      　　　　　　m1 : m1,
      　　　　　　m2 : m2
      　　　　};
      　　})();
  ```

  （待完善）

- 31 AMD（Modules/Asynchronous-Definition）、CMD（Common Module Definition）规范区别？

  > AMD 规范在这里：<https://github.com/amdjs/amdjs-api/wiki/AMD>
  >
  > CMD 规范在这里：<https://github.com/seajs/seajs/issues/242>

  ```
  Asynchronous Module Definition，异步模块定义，所有的模块将被异步加载，模块加载不影响后面语句运行。所有依赖某些模块的语句均放置在回调函数中。
  
   区别：
  
      1. 对于依赖的模块，AMD 是提前执行，CMD 是延迟执行。不过 RequireJS 从 2.0 开始，也改成可以延迟执行（根据写法不同，处理方式不同）。CMD 推崇 as lazy as possible.
      2. CMD 推崇依赖就近，AMD 推崇依赖前置。看代码：
  
  // CMD
  define(function(require, exports, module) {
      var a = require('./a')
      a.doSomething()
      // 此处略去 100 行
      var b = require('./b') // 依赖可以就近书写
      b.doSomething()
      // ...
  })
  
  // AMD 默认推荐
  define(['./a', './b'], function(a, b) { // 依赖必须一开始就写好
      a.doSomething()
      // 此处略去 100 行
      b.doSomething()
      // ...
  })
  ```

- 32 requireJS的核心原理是什么？（如何动态加载的？如何避免多次加载的？如何 缓存的？）

- 33 谈一谈你对ECMAScript6的了解？

- 34 ECMAScript6 怎么写class么，为什么会出现class这种东西? 

- 35 异步加载JS的方式有哪些？

  ```
    (1) defer，只支持IE
  
    (2) async：
  
    (3) 创建script，插入到DOM中，加载完毕后callBack
  ```

- 36 documen.write和 innerHTML的区别

  ```
  document.write只能重绘整个页面
  
  innerHTML可以重绘页面的一部分
  ```

- 37 DOM操作——怎样添加、移除、移动、复制、创建和查找节点?

  ```
  （1）创建新节点
    createDocumentFragment()    //创建一个DOM片段
    createElement()   //创建一个具体的元素
    createTextNode()   //创建一个文本节点
  （2）添加、移除、替换、插入
    appendChild()
    removeChild()
    replaceChild()
    insertBefore() //在已有的子节点前插入一个新的子节点
  （3）查找
    getElementsByTagName()    //通过标签名称
    getElementsByName()    //通过元素的Name属性的值(IE容错能力较强，会得到一个数组，其中包括id等于name值的)
    getElementById()    //通过元素Id，唯一性
  ```

- 38 .call() 和 .apply() 的区别？

  ```
    例子中用 add 来替换 sub，add.call(sub,3,1) == add(3,1) ，所以运行结果为：alert(4);
  
    注意：js 中的函数其实是对象，函数名是对 Function 对象的引用。
  
      function add(a,b)
      {
          alert(a+b);
      }
  
      function sub(a,b)
      {
          alert(a-b);
      }
  
      add.call(sub,3,1);
  ```

- 39 数组和对象有哪些原生方法，列举一下？

- 40 JS 怎么实现一个类。怎么实例化这个类

- 41 JavaScript中的作用域与变量声明提升？

- 42 如何编写高性能的Javascript？

- 43 那些操作会造成内存泄漏？


- 44 把 Script 标签 放在页面的最底部的body封闭之前 和封闭之后有什么区别？浏览器会如何解析它们？

- 45 移动端的点击事件的有延迟，时间是多久，为什么会有？ 怎么解决这个延时？（click 有 300ms 延迟,为了实现safari的双击事件的设计，浏览器要知道你是不是要双击操作。）

- 46 知道各种JS框架(Angular, Backbone, Ember, React, Meteor, Knockout...)么? 能讲出他们各自的优点和缺点么?

- 47 Underscore 对哪些 JS 原生对象进行了扩展以及提供了哪些好用的函数方法？

- 48 解释JavaScript中的作用域与变量声明提升？

- 49 那些操作会造成内存泄漏？

  ```
  内存泄漏指任何对象在您不再拥有或需要它之后仍然存在。
  垃圾回收器定期扫描对象，并计算引用了每个对象的其他对象的数量。如果一个对象的引用数量为 0（没有其他对象引用过该对象），或对该对象的惟一引用是循环的，那么该对象的内存即可回收。
  
  setTimeout 的第一个参数使用字符串而非函数的话，会引发内存泄漏。
  闭包、控制台日志、循环（在两个对象彼此引用且彼此保留时，就会产生一个循环）
  ```

- 50 Node.js的适用场景？

- 51 (如果会用node)知道route, middleware, cluster, nodemon, pm2, server-side rendering么?

- 52 解释一下 Backbone 的 MVC 实现方式？

- 53 什么是"前端路由"?什么时候适合使用"前端路由"? "前端路由"有哪些优点和缺点?

- 54 知道什么是webkit么? 知道怎么用浏览器的各种工具来调试和debug代码么?

- 55 如何测试前端代码么? 知道BDD, TDD, Unit Test么? 知道怎么测试你的前端工程么(mocha, sinon, jasmin, qUnit..)?

- 56 前端templating(Mustache, underscore, handlebars)是干嘛的, 怎么用?

- 57 简述一下 Handlebars 的基本用法？

- 58 简述一下 Handlerbars 的对模板的基本处理流程， 如何编译的？如何缓存的？

- 59 用js实现千位分隔符?(来源：[前端农民工](http://div.io/topic/744)，提示：正则+replace)

  ```
  function commafy(num) {
       num = num + '';
       var reg = /(-?d+)(d{3})/;
  
      if(reg.test(num)){
       num = num.replace(reg, '$1,$2');
      }
      return num;
  }
  ```

- 60 检测浏览器版本版本有哪些方式？

  ```
  功能检测、userAgent特征检测
  
  比如：navigator.userAgent
  //"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_2) AppleWebKit/537.36
    (KHTML, like Gecko) Chrome/41.0.2272.101 Safari/537.36"
  ```

- 61 What is a Polyfill? 

  ```
  polyfill 是“在旧版浏览器上复制标准 API 的 JavaScript 补充”,可以动态地加载 JavaScript 代码或库，在不支持这些标准 API 的浏览器中模拟它们。
  例如，geolocation（地理位置）polyfill 可以在 navigator 对象上添加全局的 geolocation 对象，还能添加 getCurrentPosition 函数以及“坐标”回调对象，
  所有这些都是 W3C 地理位置 API 定义的对象和函数。因为 polyfill 模拟标准 API，所以能够以一种面向所有浏览器未来的方式针对这些 API 进行开发，
  一旦对这些 API 的支持变成绝对大多数，则可以方便地去掉 polyfill，无需做任何额外工作。
  ```

- 62 做的项目中，有没有用过或自己实现一些 polyfill 方案（兼容性处理方案）？

  ```
  比如： html5shiv、Geolocation、Placeholder 
  ```

- 63 我们给一个dom同时绑定两个点击事件，一个用捕获，一个用冒泡。会执行几次事件，会先执行冒泡还是捕获？





##### 64 事件的各个阶段

```
1：捕获阶段 ---> 2：目标阶段 ---> 3：冒泡阶段
document   ---> target目标 ----> document
```

由此，addEventListener 的第三个参数设置为 true 和 false 的区别已经非常清晰了：

- true 表示该元素在事件的"捕获阶段"（由外往内传递时）响应事件； 
- false 表示该元素在事件的"冒泡阶段"（由内向外传递时）响应事件。









## es6





- 1 Object.is() 与原来的比较操作符" ==="、" =="的区别？ 

  ```
  两等号判等，会在比较时进行类型转换；
  三等号判等(判断严格)，比较时不进行隐式类型转换,（类型不同则会返回false）； 
  
  Object.is 在三等号判等的基础上特别处理了 NaN 、-0 和 +0 ，保证 -0 和 +0 不再相同，
  但 Object.is(NaN, NaN) 会返回 true.
  
  Object.is 应被认为有其特殊的用途，而不能用它认为它比其它的相等对比更宽松或严格。
  ```

## 





##### 2 let var const

- **let**: 允许你声明一个作用域被限制在块级中的变量、语句或者表达式 let 绑定不受变量提升的约束，这意味着let声明不会被提升到当前，该变量处于从块开始到初始化处理的"暂存死区"。
- **var**: 声明变量的作用域限制在其声明位置的上下文中，而非声明变量总是全局的, 由于变量声明（以及其他声明）总是在任意代码执行之前处理的，所以在代码中的任意位置声明变量总是等效于在代码开头声明。
- const 声明创建一个值的只读引用 (即指针)，这里就要介绍下 JS 常用类型: String、Number、Boolean、Array、Object、Null、Undefined。其中基本类型有 Undefined、Null、Boolean、Number、String，保存在栈中；复合类型 有 Array、Object ，保存在堆中； 基本数据当值发生改变时，那么其对应的指针也将发生改变，故造成 const申明基本数据类型时，再将其值改变时，将会造成报错， 例如 const a = 3 ; a = 5 时 将会报错；但是如果是复合类型时，如果只改变复合类型的其中某个Value项时， 将还是正常使用；

------

##### 3、箭头函数

语法比函数表达式更短，并且不绑定自己的 this，arguments，super 或 new.target。这些函数表达式最适合用于非方法函数，并且它们不能用作构造函数。







