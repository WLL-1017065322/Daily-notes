\- jQuery 的 each 和 原生的 JavaScript 方法 forEach

  \+ EcmaScript 5 提供的

​    \* 不兼容 IE 8

  \+ jQuery 的 each 由 jQuery 这个第三方库提供

​    \* jQuery 2 以下的版本是兼容 IE 8 的

​    \* 它的 each 方法主要用来遍历 jQuery 实例对象（伪数组）

​    \* 同时它也可以作为低版本浏览器中 forEach 替代品

​    \* jQuery 的实例对象不能使用 forEach 方法，如果想要使用必须转为数组才可以使用

​    \* `[].slice.call(jQuery实例对象)`



Array.prototype.mySlice = function () {

  var start = 0

  var end = this.length

  if (arguments.length === 1) {

​    start = arguments[0]

  } else if (arguments.length === 2) {

​    start = arguments[0]

​    end = arguments[1]

  }

  var tmp = []

  for (var i = start; i < end; i++) {

​    // fakeArr[0]

​    // fakeArr[1]

​    // fakeArr[2]

​    tmp.push(this[i])

  }

  return tmp

}

var fakeArr = {

  0: 'abc',

  1: 'efg',

  2: 'haha',

  length: 3

}

// 所以你就得到了真正的数组。 

[].mySlice.call(fakeArr)

\```