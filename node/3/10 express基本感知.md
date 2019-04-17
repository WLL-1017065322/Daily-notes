// 0. 安装

// 1. 引包

var express =require('express')

var app=express()

app.get('/',function(req,res){res.send('hello express!')})

app.get('/',function(req,res){res.send('hello express!')})



// 在 Express 中开放资源就是一个 API 的事儿

// 公开指定目录

// 只要这样做了，你就可以直接通过 /public/xx 的方式访问 public 目录中的所有资源了

app.use('/public/', express.static('./public/'))

app.use('/static/', express.static('./static/'))

app.use('/node_modules/', express.static('./node_modules/'))



// 模板引擎，在 Express 也是一个 API 的事儿

// 得到路径

// 一个一个的判断

// 以前的代码很丑





app.listen(3000,function(){

console.log('aa')})