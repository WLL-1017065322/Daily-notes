所有联网的程序都要进行网络通信;

计算机只有一个物理网卡,而且同一个局域网,网卡的地址必须是唯一的;

网卡是通过的唯一ip地址,进行定位的

所有需要联网通信的软件都必须具有端口号

端口号范围0~65536

默认端口号:http:80

没含义:3000,5000

www.baidu.com dns->ip 111.111.1.1

请求的地址及端口号

server.on('request',function(request,response){ console.log('请求的端口 url',request.socket.remotePort,request.socket.remoteAddress)})