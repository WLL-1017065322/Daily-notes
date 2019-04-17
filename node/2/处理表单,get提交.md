发表留言限制

required minlength="5" maxlength="20"



  以前表单是如何提交的？

​      表单中需要提交的表单控件元素必须具有 name 属性

​      表单提交分为：

​        \1. 默认的提交行为

​        \2. 表单异步提交

​        action 就是表单提交的地址，说白了就是请求的 url 地址

​        method 请求方法

​            get

​            post





// /pinglun?name=的撒的撒&message=的撒的撒的撒

// 对于这种表单提交的请求路径，由于其中具有用户动态填写的内容

// 所以你不可能通过去判断完整的 url 路径来处理这个请求

// 

// 结论：对于我们来讲，其实只需要判定，如果你的请求路径是 /pinglun 的时候，那我就认为你提交表单的请求过来了





var url=require('url')

 // 使用 url.parse 方法将路径解析为一个方便操作的对象，第二个参数为 true 表示直接将查询字符串转为一个对象（通过 query 属性来访问）

var parseObj = url.parse(req.url, true)

 var pathname = parseObj.pathname

// 单独获取不包含查询字符串的路径部分（该路径不包含 ? 之后的内容）

else if (pathname === '/pinglun') {

res.end(JSON.stringify(parseObj.query))

 comment.dateTime = '2017-11-2 17:11:22'

comments.unshift(comment) //comments.push(comment) 

我们已经使用 url 模块的 parse 方法把请求路径中的查询字符串给解析成一个对象了

​      // 所以接下来要做的就是：

​      //    1. 获取表单提交的数据 parseObj.query

​      //    2. 将当前时间日期添加到数据对象中，然后存储到数组中

​      //    3. 让用户重定向跳转到首页 /

​      //       当用户重新请求 / 的时候，我数组中的数据已经发生变化了，所以用户看到的页面也就变了

parseObj.pathname

parseObj.query

表单提交重定向



/ 服务端这个时候已经把数据存储好了，接下来就是让用户重新请求 / 首页，就可以看到最新的留言内容了

​      // 如何通过服务器让客户端重定向？

​      //    1. 状态码设置为 302 临时重定向

​      //        statusCode

​      //    2. 在响应头中通过 Location 告诉客户端往哪儿重定向

​      //        setHeader

​      // 如果客户端发现收到服务器的响应的状态码是 302 就会自动去响应头中找 Location ，然后对该地址发起新的请求

​      // 所以你就能看到客户端自动跳转了

一次请求  一次响应

res.statusCode = 302

​      res.setHeader('Location', '/')

​      res.end()







var url = require('url')

server.on('',function(){

var parseObj = url.parse(request.url, true)

 var pathname = parseObj.pathname

} else if (pathname === '/pinglun') {

​	comment.dateTime=ctime

​        comments.push(comment)



​        response.statusCode=302

​        response.setHeader('Location','/')

​        response.end()























