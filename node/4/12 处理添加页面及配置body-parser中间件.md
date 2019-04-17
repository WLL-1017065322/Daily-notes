引入三方包：npm install --save body-parser

app.js

 \* app.js 入门模块

 \* 职责：

 \*   创建服务

 \*   做一些服务相关配置

 \*     模板引擎

 \*     body-parser 解析表单 post 请求体

 \*     提供静态资源服务

 \*   挂载路由

 \*   监听端口启动服务

 */

// 配置模板引擎和 body-parser 一定要在 app.use(router) 挂载路由之前

// parse application/x-www-form-urlencoded

app.use(bodyParser.urlencoded({ extended: false }))

// parse application/json

app.use(bodyParser.json())

// 把路由容器挂载到 app 服务中

app.use(router)

ronter.js

/ 1. 创建一个路由容器

// 2. 把路由都挂载到 router 路由容器中

  // // 3. 把 router 导出



var router = express.Router()

router.get('/students/new', function (req, res) {

  res.render('new.html')

})

module.exports = router



 // 1. 获取表单数据

  // 2. 处理

  //    将数据保存到 db.json 文件中用以持久化

  // 3. 发送响应





 // 1. 在客户端的列表页中处理链接问题（需要有 id 参数）

  // 2. 获取要编辑的学生 id





  // 3. 渲染编辑页面

  //    根据 id 把学生信息查出来

  //    使用模板引擎渲染页面