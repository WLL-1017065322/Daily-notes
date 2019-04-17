- 模块中导出多个成员和导出单个成员

  导出多个成员(必须在对象中)：

  exports.a=123 

  exports.b=..

  exports.c=...

  或者

  module.exports={add:function(){}, str:'hello' }

  导出单个成员：

  module.exports='hh'

  module.exports='hh' ==>后者覆盖前者






\- exports 和 module.exports 的区别

  \+ 每个模块中都有一个 module 对象

  \+ module 对象中有一个 exports 对象

  \+ 我们可以把需要导出的成员都挂载到 module.exports 接口对象中

  \+ 也就是：`moudle.exports.xxx = xxx` 的方式

  \+ 但是每次都 `moudle.exports.xxx = xxx` 很麻烦，点儿的太多了

  \+ 所以 Node 为了你方便，同时在每一个模块中都提供了一个成员叫：`exports`

  \+ `exports === module.exports` 结果为  `true`s

  \+ 所以对于：`moudle.exports.xxx = xxx` 的方式 完全可以：`expots.xxx = xxx`

  \+ 当一个模块需要导出单个成员的时候，这个时候必须使用：`module.exports = xxx` 的方式

  \+ 不要使用 `exports = xxx` 不管用

  \+ 因为每个模块最终向外 `return` 的是 `module.exports`

  \+ 而 `exports` 只是 `module.exports` 的一个引用

  \+ 所以即便你为 `exports = xx` 重新赋值，也不会影响 `module.exports`

  \+ 但是有一种赋值方式比较特殊：`exports = module.exports` 这个用来重新建立引用关系的

  \+ 之所以让大家明白这个道理，是希望可以更灵活的去用它









// 如果你实在分不清楚 exports 和 module.exports

// 你可以选择忘记 exports

// 而只使用 module.exports 也没问题