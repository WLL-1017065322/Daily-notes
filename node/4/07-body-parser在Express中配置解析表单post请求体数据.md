get post 获取方式不一样

没有内置获取表单post请求api需要第三方 body-parser

使用插件express<http://expressjs.com/en/resources/middleware.html>

1，安装

```sh
$ npm install --save body-parser

2,配置 

var express = require('express')
var bodyParser = require('body-parser')

var app = express()
//配置body-parser
//只要加入之歌配置，则在req请求对象上会多一个属性：body
//即可以直接通过req.body获取表单post请求数据了

// parse application/x-www-form-urlencoded
app.use(bodyParser.urlencoded({ extended: false }))

// parse application/json
app.use(bodyParser.json())

//app.use(function (req, res) {
//  res.setHeader('Content-Type', 'text/plain')
//  res.write('you posted:\n')
//  res.end(JSON.stringify(req.body, null, 2))
})



app.post('/post',function(req,res){
    console.log(req.body)

    var comment=req.body
    comment.dataTime='2017-11-5 10:58:51'
    comments.unshift(comment)
    //res.status=302
    //res.setHeader('Location','/')
    res.redirect('/')
    
})


```