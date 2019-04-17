构建一个web服务器

node提供http模块

1,加载http核心模块,

***var http=require('http')***  ====>前面的http可以随便起,后面不行

2使用 http.createServer() 方法创建一个 Web 服务器

返回一个 Server 实例

***var server=http.createServer()***

3. 服务器要干嘛？

   提供服务：对 数据的服务

   发请求

   接收请求

   处理请求

   给个反馈（发送响应）

   注册 request 请求事件

   当客户端请求过来，就会自动触发服务器的 request 请求事件，然后执行第二个参数：回调处理函数

***server.on('request',function(){console.log("受到客户请求"+request.url***

response.write('hello') response 对象有一个方法：write 可以用来给客户端发送响应数据

 write 可以使用多次，但是最后一定要使用 end 来结束响应，否则客户端会一直等待

response.end()***)})***告诉客户端，我的话说完了，你可以呈递给用户了

server.on('request',function(request,response){console.log("受到客户请求")})

4,绑定端口号,启动服务器

***server.listen(3000,function(){console.log("服务器启动成功 http://127.0.0.1:3000/")})***







request 请求事件处理函数，需要接收两个参数：

   Request 请求对象

​       请求对象可以用来获取客户端的一些请求信息，例如请求路径

   Response 响应对象

​       响应对象可以用来给客户端发送响应消息

ps ctrl+c 关闭服务器