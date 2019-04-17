1，找到官方文档

 https://github.com/aui/art-template



https://aui.github.io/art-template/

安装：

npm install --save art-template
npm install --save express-art-template 依赖上面

**配置：app.engine('html', require('express-art-template'))**

使用：express默认回去views目录找index.html

app.get('/admin',function(req,res){

​    res.render('admin/index.html',{

​        title:'管理系统'

​    })

})

如果希望修改默认的views视图渲染存储目录可以

// **app.set('views', render函数的默认路径)







// 配置使用 art-template 模板引擎

// 第一个参数，表示，当渲染以 .art 结尾的文件的时候，使用 art-template 模板引擎

// express-art-template 是专门用来在 Express 中把 art-template 整合到 Express 中

// 虽然外面这里不需要记载 art-template 但是也必须安装

// 原因就在于 express-art-template 依赖了 art-template



// Express 为 Response 相应对象提供了一个方法：render

/**/ render** 方法默认是不可以使用，但是如果配置了模板引擎就可以使用了

**// res.render('html模板名', {模板数据})**

// 第一个参数不能写路径，默认会去项目中的 views 目录查找该模板文件

// 也就是说 Express 有一个约定：开发人员把所有的视图文件都放到 **views** 目录中

// **如果想要修改默认的 views 目录，则可以**

// **app.set('views', render函数的默认路径)**

// 配置 body-parser 中间件（插件，专门用来解析表单 POST 请求体）

// parse application/x-www-form-urlencoded





var express = require('express');
var app = express();
**app.engine('art', require('express-art-template'));**// art可以改成html否则改文件名
app.set('view options', {
    debug: process.env.NODE_ENV !== 'production'
});

app.get('/', function (req, res) {
    res.render('index.art', {
        user: {
            name: 'aui',
            tags: ['art', 'template', 'nodejs']
        }
    });
});

