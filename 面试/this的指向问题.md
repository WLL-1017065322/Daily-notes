# this

this是js中的一个关键字，函数运行时自动生成的一个内部对象，只能在函数内部使用。我们要讨论的是 this 的指向。

> this就是函数运行时自动生成的一个内部对象

**this的指向不是在创建时就决定了，而是由执行环境决定的。**

下面介绍一下几种情况下，this的指向

## 1、全局环境

全局环境下，this就代表window对象。（针对web 应用来讲）

```
var name = 'zhar';
function say(){
  console.log(this.name);//zhar
}
say();
```

同样，在 setTimeout 或 setInterval 这样的延时函数中调用也属于全局对象

```
var name = 'zhar';
setTimeout(function(){
  console.log(this.name);//zhar
},0);
```

## 2、对象环境

对象环境指向对象。

```
var obj = {
  name : "zhar",
  say : function(){
    console.log(this.name);//zhar
  }
}
obj.say();
```

下面举两个经典的例子：

```
var name = 'tom';
var obj = {
  name : "zhar",
  say : function(){
    console.log(this.name);
  }
}
var fun = obj.say;
fun();//输出 ?//tom-->fun定义在全局环境下，即window.fun()
//再次说明了this的指向是由运行时的执行环境来决定的
var name = 'tom';
var obj = {
  name : "zhar",
  say : function(){
    return function(){
      console.log(this.name);
    }
  }
}
obj.say()();//输出 ？//tom
```

## 3、构造函数环境

构造函数中的this 会指向创建出来的实例对象，使用new 调用构造函数时，会先创建出一个空对象，然后用call函数把构造函数中的this指针修改为指向这个空对象。执行完环境后，空对象也就有了相关的属性，然后将对象返回出去，所以说就不用我们自己手动返回啦~

```
function Person() {
    this.name = 'zhar';
}
var p = new Person();
console.log(p.name);
```

*综合以上，构造函数不需要返回值，如果我们指定一个返回值时，this的指向将发生变化*

```
function Person() {
  this.name = 'zhar';
  return {};
}
var p = new Person();
console.log(p.name);//undefined
//--------------------------------------
function Person() {
  this.name = 'zhar';
  return {name:'tom'};
}
var p = new Person();
console.log(p.name);//tom      如果构造函数返回对象(Object,Array,Function)，那 this 将指向这个对象，其它基础类型则不受影响
//--------------------------------------
function Person() {
  this.name = 'zhar';
  return 1;//number string boolean 等
}
var p = new Person();
console.log(p.name);//zhar
```

> 所以，如无必要我们通常不要设置构造函数的返回值

## 4、事件对象

在 DOM 事件中使用 this，this 指向了触发事件的 DOM 元素本身

```
li.onclick = function(){
    console.log(this.innerHTML);
}
```

> 总结下来就是一句话：是谁调用的，this就指向谁

**下面介绍一下如何来修改this 的指向**

## 1、可以使用局部变量来代替this指针

```
var name = "zhar";
var obj = {
  name : "zhar",
  say : function(){
    var _this = this;//使用一个变量指向 this
    setTimeout(function(){
      console.log(_this.name);
    },0);
  }
}
obj.say();
```

> 该方法为非常常用的一个方法

## 2、使用call 或 apply 方法

首先说明一下，call也是函数调用的一种形式，可以通过 函数名.call（）来调用函数。但是提供了一个修改this指向的方法。

fun.call(thisObj[,arg1[,arg2[,...]]])

调用方式和传入参数如上面的形式。其中，所以call(thisObj[,arg1[,arg2[,...]]])中的第一个参数就是要更改this指向的对象，为必选参数; 之后的参数要根据调用的函数是否需要传入参数(为可选的)

下面通过代码来展示call 如何使用：

```
var name = 'zhar';
function say(){
  console.log(this.name);
};
say();//zhar;
var obj = {
  name : 'tom',
  say : function(){
    console.log(this.name);
  }
}
say.call(obj);//tom      将 say 函数中的 this 替换为传入的对象
obj.say();//tom
obj.say.call(null);//zhar    将 obj.say 函数的 this 替换为了 null，也就意味着指向了全局环境
//前面课程的继承代码
function Person(){
  this.name = "人";
}
function Student(){
  Person.call(this,null);
}
var s = new Student();
console.log(s.name);
li.onclick = function(){
  console.log(this.innerHTML);//此处的 this 代表着 DOM 元素
  function update(){
    this.innerHTML += " new ";
  }
  //update();//这样做的话，this 的指向将变为window
  update.call(this);//通过 call 方法修改函数内 this 的指向
}
//call 的传参
function say(arg1,arg2){
  console.log(this.name,arg1,arg2);
};
var obj = {
  name : 'tom',
  say : function(){
    console.log(this.name);
  }
}
say.call(obj,'one','two');//tom one two
```

**apply**

apply的作用和call一样，不同的是传参的形式。apply需要以数组的形式传递参数

```
//apply 的传参
function say(arg1,arg2){
  console.log(this.name,arg1,arg2);
};
var obj = {
  name : 'tom',
  say : function(){
    console.log(this.name);
  }
}
say.apply(obj,['one','two']);//tom one two
```

> 以上就是关于this指向和如何修改this指向的介绍





# Javascript定时器中的this指向



使用js中的定时器（setInterval，setTimeout），很容易会遇到this指向的问题。

直接上例子：



```
 1 var name = 'my name is window';
 2 var obj = {
 3     name: 'my name is obj',
 4     fn: function () {
 5         var timer = null;
 6         clearInterval(timer);
 7         timer = setInterval(function () {
 8             console.log(this.name);  //my name is window
 9         }, 1000)
10     }
11 }
```



在这里，从this.name可以看出this的指向是window。

如果没有特殊指向，setInterval和setTimeout的回调函数中this的指向都是window。这是因为JS的定时器方法是定义在window下的。但是平时很多场景下，都需要修改this的指向。这里总结了几种：

1、最常用的方法：在外部函数中将this存为一个变量，回调函数中使用该变量，而不是直接使用this。



```
 1 var name = 'my name is window';
 2 var obj = {
 3     name: 'my name is obj',
 4     fn: function () {
 5         var that = this;
 6         var timer = null;
 7         clearInterval(timer);
 8         timer = setInterval(function () {
 9             console.log(that.name);   //my name is obj
10         }, 1000)
11     }
12 }
```



在fn中加了var that = this; 回调函数中使用that代替this即可。这种方法最常见，使用也最广泛。

2、使用bind()方法（bind()为ES5的标准，低版本IE下有兼容问题，可以引入es5-shim.js解决）

bind()的作用类似call和apply，都是修改this指向。但是call和apply是修改this指向后函数会立即执行，而bind则是返回一个新的函数，它会创建一个与原来函数主体相同的新函数，新函数中的this指向传入的对象。



```
 1 var name = 'my name is window';
 2 var obj = {
 3     name: 'my name is obj',
 4     fn: function () {
 5         var timer = null;
 6         clearInterval(timer);
 7         timer = setInterval(function () {
 8             console.log(this.name);   //my name is obj
 9         }.bind(this), 1000)
10     }
11 }
```



在这里为什么不能用call和apply，是因为call和apply不是返回函数，而是立即执行函数，那么，就失去了定时器的作用。

3、使用es6的箭头函数：箭头函数的最大作用就是this指向。



```
 1 var name = 'my name is window';
 2 var obj = {
 3     name: 'my name is obj',
 4     fn: function () {
 5         var timer = null;
 6         clearInterval(timer);
 7         timer = setInterval(() => {
 8             console.log(this.name);  //my name is obj
 9         }, 1000)
10     }
11 }
```



箭头函数没有自己的this，它的this继承自外部函数的作用域。所以，在该例中，定时器回调函数中的this，是继承了fn的this。当然箭头函数也有兼容问题，要是兼容低版本ie，需要使用babel编译，并且引入es5-shim.js才可以。







