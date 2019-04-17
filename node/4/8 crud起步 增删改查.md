1，安装 npm ...i -S bootstrop，express。。。

npm install --save art-template
npm install --save express-art-template

2,修改样式



var express=require('express')

var bodyParser = require('body-parser')

var app=express()

app.use('/node_modules/',express.static('./node_modules/'))

app.use('/public/',express.static('./public/'))

//app.use(bodyParser.urlencoded({ extended: false }))

app.engine('html', require('express-art-template'))

app.get('/',function(req,res){

​    res.render('index.html',{

​        // fruits:[

​        //     'pinguo',

​        //     'xiangjia'

​        // ]

​    })

​    

})

app.listen(3000,function(){

​    console.log('express is running')

})