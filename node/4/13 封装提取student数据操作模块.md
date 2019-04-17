

app.js

..

router.js

router2.get('/students',function(req,res){

Students.find(function(err,students){

​    if(err){

​        return res.status(500).send('server error')

​    }

​    res.render('index.html',{

​        students:students,

​        fruits:[

​            'pinguo',

​            'xiangjia',

​            'hamogua'

​        ]

})

/**

 \* student.js

 \* 数据操作文件模块

 \* 职责：操作文件中的数据，只处理数据，不关心业务

 *

 \* 这里才是我们学习 Node 的精华部分：奥义之所在

 \* 封装异步 API

 */

student.js:



var fs = require('fs')

var dbPath = './db.json'

/**

 \* 获取学生列表

 \* @param  {Function} callback 回调函数

 */



exports.find = function (callback) {

  fs.readFile(dbPath, 'utf8', function (err, data) {

​    if (err) {

​      return callback(err)

​    }

​    callback(null, JSON.parse(data).students)

  })

}