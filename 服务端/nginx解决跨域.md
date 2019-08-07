## 什么是跨域？

使用js获取数据时，涉及到的两个url只要协议、域名、端口有任何一个不同，都被当作是不同的域，相互访问就会有跨域问题。
例如客户端的域名是www.redis.com.cn,而请求的域名是www.264.cn
如果直接使用ajax访问，会有以下错误
XMLHttpRequest cannot load http://www.264.cn/server.php. No 'Access-Control-Allow-Origin' header is present on the requested resource.Origin 'http://www.redis.com.cn' is therefore not allowed access.

## 如何解决跨域？

在服务器页面的Response header中加入如下内容，可以实现POST跨域。
// 指定允许其他域名访问
header('Access-Control-Allow-Origin:*');
// 响应类型
header('Access-Control-Allow-Methods:POST');
// 响应头设置
header('Access-Control-Allow-Headers:x-requested-with,content-type');

Access-Control-Allow-Origin:* 表示允许任何域名跨域访问
如果需要指定某域名才允许跨域访问，只需把Access-Control-Allow-Origin:*改为Access-Control-Allow-Origin:允许的域名
例如：header('Access-Control-Allow-Origin:http://www.redis.com.cn');

 

1.nginx配置文件增加响应头

在服务器端的nginx.conf中配置增加配置

```
http {
  ......
  add_header Access-Control-Allow-Origin *;
  add_header Access-Control-Allow-Headers X-Requested-With;
  add_header Access-Control-Allow-Methods GET,POST,OPTIONS;
  ......
}
```



这样就可以实现GET,POST,OPTIONS的跨域请求的支持

2.修改php代码加入响应头

例如，server.php 路径：http://www.264.cn/server.php

```
<?php  
$ret = array(  
    'name' => isset($_POST['name'])? $_POST['name'] : '',  
    'gender' => isset($_POST['gender'])? $_POST['gender'] : ''  
);  
  
header('content-type:application:json;charset=utf8');  
header('Access-Control-Allow-Origin:*');  
header('Access-Control-Allow-Methods:POST');  
header('Access-Control-Allow-Headers:x-requested-with,content-type');  
  
echo json_encode($ret);  
?>
```



3.修改客端的nginx配置，利用反向代理来实现

例如，www.redis.com.cn/html/request.html 想请求www.264.cn/api/msg?method=1&para=2；

```
var url = 'www.264.cn/api/msg?method=1&para=2'；
$.ajax({
type: "GET",
url:url,
success: function(res){..},
....
})
```



变成访问本地域名地址

```
var url = 'http://www.264.cn/api/msg?method=1&para=2'；
var proxyurl ＝ 'msg?method=1&para=2'；
$.ajax({
type: "GET",
url:proxyurl,
success: function(res){..},
....
})
```



通过nginx中增加location反向代理到服务器端

```
location ^~/proxy/html/{
    rewrite ^/proxy/html/(.*)$ /$1 break;
    proxy_pass http://www.redis.com.cn/api/;
}
```













