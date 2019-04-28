```
A this value is a special object which is related with the execution context. 
Therefore, it may be named as a context object (i.e. an object in which context the execution context is activated).
this适合执行的上下文环境息息相关的一个特殊对象。因此，它也可以称为上下文对象[context object](激活执行上下文的上下文)。
```

任何对象都可以作为上下文的this值。我想再次澄清对与ECMAScript中，与执行上下文相关的一些描述——特别是this的误解。通常，this 被错误地，描述为变量对象的属性。最近比如在[这本书](http://yuiblog.com/assets/High_Perf_JavaScr_Ch2.pdf)中就发现了(尽管书中提及this的那一章还不错)。 请牢记：

```
a this value is a property of the execution context, but not a property of the variable object.
this是执行上下文环境的一个属性，而不是某个变量对象的属性
```

这个特点很重要，因为和变量不同，this是没有一个类似搜寻变量的过程。当你在代码中使用了this,这个 this的值就直接从执行的上下文中获取了，而不会从作用域链中搜寻。this的值只取决中进入上下文时的情况。

顺便说一句，和ECMAScript不同，Python有一个self的参数，和this的情况差不多，但是可以在执行过程中被改变。在ECMAScript中，是不可以给this赋值的，因为，还是那句话，this不是变量。

在global context(全局上下文)中，this的值就是指全局这个对象，这就意味着，this值就是这个变量本身。

```
var x = 10;
 
console.log(
  x, // 10
  this.x, // 10
  window.x // 10
);
```

在函数上下文[function context]中，this会可能会根据每次的函数调用而成为不同的值.this会由每一次caller提供,caller是通过调用表达式[call expression]产生的（也就是这个函数如何被激活调用的）。例如，下面的例子中foo就是一个callee，在全局上下文中被激活。下面的例子就表明了不同的caller引起this的不同。

```
// "foo"函数里的alert没有改变
// 但每次激活调用的时候this是不同的
 
function foo() {
  alert(this);
}
 
// caller 激活 "foo"这个callee，
// 并且提供"this"给这个 callee
 
foo(); // 全局对象
foo.prototype.constructor(); // foo.prototype
 
var bar = {
  baz: foo
};
 
bar.baz(); // bar
 
(bar.baz)(); // also bar
(bar.baz = bar.baz)(); // 这是一个全局对象
(bar.baz, bar.baz)(); // 也是全局对象
(false || bar.baz)(); // 也是全局对象
 
var otherFoo = bar.baz;
otherFoo(); // 还是全局对象
```

如果要深入思考每一次函数调用中，this值的变化(更重要的是怎样变化)，你可以阅读本系列教程第10章This。上文所提及的情况都会在此章内详细讨论。