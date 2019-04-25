# 为什么下面的两个getElementById前面一个必须加document.另一个可以不用？

就是第一个id的demo里面可以省略document.

而第二个id的demo2不可以

![img](https://pic4.zhimg.com/v2-3a8e84289916b370f0db234d55378b1f_b.png)









作者：紫云飞

链接：https://www.zhihu.com/question/313671837/answer/609113389

来源：知乎

著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。





首先不推荐你使用 `onxxx=` 这种事件处理器，它是历史遗留产物，最好完全不要学。

你在 `onclick`中写一条语句，浏览器会给你包装成为一个函数，然后再在事件触发时执行它。比如你写的是 `getElementById("demo").innerHTML = Date()`，实际执行的函数会是：

```js
function onclick(event) {
  getElementById("demo").innerHTML = Date()
}
```

浏览器还额外加了个事件对象的形参 `event`，多贴心。但这不重要，重要的是这个函数声明外层还有两层 `with`语句，像这样： 

```js
with(document) {
  with(button) { // 当前元素 button
    function onclick(event) {
      getElementById("demo").innerHTML = Date()
    }
  }
}
```

正因为有了这层`with(document)`，所以你才可以省略不写 `document.`。

还有，如果当前元素是个包含在`form`里的合法的表单元素比如`input`，`with`语句会有三层， 多了一层`with(form)`，比如说下面这段毫无意义的代码：

```html
<form><input onclick="submit()"></form>
```

`submit()`函数能执行成功，就是因为它执行的其实是 `form`元素上的 `submit`方法：

```js
with(document) {
  with(form) { // 实际执行的 submit 方法是它身上的 
    with(input) {
      function onclick(event) {
        submit()
      }
    }
  }
}
```

你可以在 Chrome DevTools 里直观的看到我讲的这三层`with`语句的作用域，先打开一个页面，再打开 DevTools，然后在地址看上粘贴打开：`data:text/html,<form><input onfocus="debugger" autofocus>`，在 Sources 面板里，你就能清楚的看到存在有五层作用域：

![img](https://pic4.zhimg.com/80/v2-56273cfc75f41999b6aa231008a632e1_hd.jpg)

 如果真有读者好奇规范是怎么写的，那规范在这里 [https://html.spec.whatwg.org/multipage/webappapis.html#event-handler-attributes:event-handlers-34](https://link.zhihu.com/?target=https%3A//html.spec.whatwg.org/multipage/webappapis.html%23event-handler-attributes%3Aevent-handlers-34)

你写的 `demo2`里虽然也会有 `with(document)`，但你的 `.getElementById()` 函数调用没有静态的写在 `with` 语句里， 而是写在外部的 `myFunction`函数声明里，JavaScript 里的变量查找采用静态语义，所以是找不到 `document`的。 