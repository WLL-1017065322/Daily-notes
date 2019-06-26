二、JavaScript部分

（1）JavaScript的数据类型

基本数据类型：Number，String，Boolean，Undefined，Null

复杂数据类型：Object，Array，Function，RegExp，Date，Error

全局数据类型：Math

（2）JavaScript的闭包

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

（3）new 操作符到底做了什么

  首先，new操作符为我们创建一个新的空对象，然后this变量指向该对象，

  其次，空对象的原型执行函数的原型，

  最后，改变构造函数内部的this的指向

代码如下：

```js
var obj={};
obj.__proto__=fn.prototype;
fn.call(obj);
```

（4）改变函数内部this指针的指向函数

call和apply，假设要改变fn函数内部的this的指向，指向obj，那么可以fn.call(obj);或者fn.apply(obj);那么问题来了，call和apply的区别是什么，其是call和apply的区别在于参数，他们两个的第一个参数都是一样的，表示调用该函数的对象，apply的第二个参数是数组，是[arg1,arg2,arg3]这种形式，而call是arg1,arg2,arg3这样的形式。还有一个bind函数，

var bar=fn.bind(obj);那么fn中的this就指向obj对象了，bind函数返回新的函数，这个函数内的this指针指向obj对象。

（5）JavaScript的作用域和作用域链

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

（6）JavaScript的继承

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

（7）JavaScript变量提升

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

（8）JavaScript事件模型

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

（9）内存泄漏

内存泄漏指的是浏览器不能正常的回收内存的现象

（10）浏览器的垃圾回收机制

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

（11）同源策略

同源策略是浏览器有一个很重要的概念。所谓同源是指，域名，协议，端口相同。不同源的客户端脚本(javascript、ActionScript)在没明确授权的情况下，不能读写对方的资源。简单的来说，浏览器允许包含在页面A的脚本访问第二个页面B的数据资源，这一切是建立在A和B页面是同源的基础上。

（12）跨域的几种方式

jsonp（利用script标签的跨域能力）跨域、websocket（html5的新特性，是一种新协议）跨域、设置代理服务器（由服务器替我们向不同源的服务器请求数据）、CORS（跨源资源共享，cross origin resource sharing）、iframe跨域、postMessage(包含iframe的页面向iframe传递消息)，document.domain跨域（比如：在一个文件中设置了document.domain="[http://qq.com](https://link.zhihu.com/?target=http%3A//qq.com)",那么另一个设置了document.domain="[http://qq.com](https://link.zhihu.com/?target=http%3A//qq.com)"的，他们两个就是同源）

（13）异步和同步

同步指下一个程序的执行需要等到上一个程序执行完毕，也就是得出结果后下一个才能执行，

异步指的是上一个程序指向后，下一个程序不用等到上一个程序出结果就能执行，等上一个出结果了调用回调函数处理结果就好。

（14）JavaScript的值类型和引用类型

JavaScript有两种类型的数据，值类型和引用类型，一般的数字，字符串，布尔值都是值类型，存放在栈中，而对象，函数，数组等是引用类型，存放在堆中，对引用类型的复制其实是引用复制，相当于复制着地址，对象并没有真正的复制。

```js
var a=5;var b=a;a=null;    //那么b是5
var a={},var b=a;b.name="mbj";
console.log(a.name);   //mbj，因为a，b指向同一个对象
a=null;console.log(typeof b);  //object，a=null，只是a不再指向该对象，但是这个对象还是在堆中确确实实的存在，b依然指向它。
```

（15）浏览器js解析引擎的两个队列

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

（16）封装cookie的添加，删除，查询方法

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

（17）事件委托机制

事件委托指的是，不再事件的发生地设立监听函数，而是在事件发生地的父元素或者祖先元素设置监听器函数，这样可以大大提高性能，因为可以减少绑定事件的元素，比如：

```html
<ul>
 <li></li>
 <li></li>
 <li></li>
</ul>
```

要给li元素绑定click事件，使用事件委托机制的话，就只需要给ul绑定click事件就行了，这样就不需要给每个li'绑定click事件，减小内存占用，提高效率，有兴趣的童鞋可以去看看jQuery的live，bind，on，delegate函数的区别，这几个函数就采用了事件委托机制。







**JavaScript 基础问题**

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

**6.解释 JavaScript 并发模型**

您是否熟悉 Elixir，Clojure，Java 等其他编程语言中使用的任何其他并发模型？

提示：查找事件循环，任务队列，调用栈，堆等。

**7.new 关键字在 JavaScript 中有什么作用？**

提示：在 JavaScript 中，`new` 是用于实例化对象的运算符。 这里的目的是了解知识广度和记忆情况。

另外，请注意 `[[Construct]]` 和 `[[Call]]`。

**8.JavaScript 中有哪些不同的函数调用模式？ 详细解释。**

提示：有四种模式，函数调用，方法调用，`.call()` 和 `.apply()`。

**9.解释任一即将发布新的 ECMAScript 提案。**

提示：比如 2018 的 BigInt，partial 函数，pipeline 操作符 等。

**10.JavaScript 中的迭代器（iterators）和迭代（iterables）是什么？ 你知道什么是内置迭代器吗？**

**11.为什么 JavaScript classes(类)被认为是坏的或反模式？**

这是一个神话吗？它是否遭受了误传？是否有一些有用的用例？

**12.如何在 JSON 中序列化以下对象？**

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

**13.你熟悉 Typed Arrays 吗？ 如果熟悉，请解释他们与 JavaScript 中的传统数组相比的异同？**

**14. 默认参数是如何工作？**

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

**JavaScript 前端应用设计问题**

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

















