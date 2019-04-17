异步无法保证顺序，嵌套来保证  回调地狱嵌套



es6 新增api  promise 构造函数

promise 容器 promise本生不是异步但内部封装的是一个异步

容器存放了一个同步任务

1，创建promise容器

pending ===》resolve

=====reject

promise本生不是异步但内部封装的是一个异步

var p1 = new Promise(function (resolve, reject) {

  fs.readFile('./data/a.txt', 'utf8', function (err, data) {

​    if (err) {

​      reject(err)

​    } else {

​      resolve(data)

​    }

  })

})

then方法接受的function就是容器中的resolve

p1.then(function(data){

console.log(data),

},function(err){

console.log('读取文件失败了', err)

})















var fs = require('fs')

var p1 = new Promise(function (resolve, reject) {

  fs.readFile('./data/a.txt', 'utf8', function (err, data) {

​    if (err) {

​      reject(err)

​    } else {

​      resolve(data)

​    }

  })

})

var p2 = new Promise(function (resolve, reject) {

  fs.readFile('./data/b.txt', 'utf8', function (err, data) {

​    if (err) {

​      reject(err)

​    } else {

​      resolve(data)

​    }

  })

})

var p3 = new Promise(function (resolve, reject) {

  fs.readFile('./data/c.txt', 'utf8', function (err, data) {

​    if (err) {

​      reject(err)

​    } else {

​      resolve(data)

​    }

  })

})

p1

  .then(function (data) {

​    console.log(data)

​    // 当 p1 读取成功的时候

​    // 当前函数中 return 的结果就可以在后面的 then 中 function 接收到

​    // 当你 return 123 后面就接收到 123

​    //      return 'hello' 后面就接收到 'hello'

​    //      没有 return 后面收到的就是 undefined

​    // 上面那些 return 的数据没什么卵用

​    // 真正有用的是：我们可以 return 一个 Promise 对象

​    // 当 return 一个 Promise 对象的时候，后续的 then 中的 方法的第一个参数会作为 p2 的 resolve

​    // 

​    return p2

  }, function (err) {

​    console.log('读取文件失败了', err)

  })

  .then(function (data) {

​    console.log(data)

​    return p3

  })

  .then(function (data) {

​    console.log(data)

​    console.log('end')

  })