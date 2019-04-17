**router.js**



router2.post('/students/new',function(req,res){

   // console.log(req.body)

​      // 1. 获取表单数据

  // 2. 处理

  //    将数据保存到 db.json 文件中用以持久化

  // 3. 发送响应

  Students.save(req.body,function(err){

​      if(err){

​          return res.status(500).send('server error')

​      }

​      //返回主页

​      res.redirect('/students')

  })

})



**student.js**

/**

 \* 添加保存学生

 \* @param  {Object}   student  学生对象

 \* @param  {Function} callback 回调函数

 */

exports.save = function (student, callback) {

  fs.readFile(dbPath, 'utf8', function (err, data) {

​    if (err) {

​      return callback(err)

​    }

​    var students = JSON.parse(data).students

​    // 添加 id ，唯一不重复

​    student.id = students[students.length - 1].id + 1

​    // 把用户传递的对象保存到数组中

​    students.push(student)

​    // 把对象数据转换为字符串

​    var fileData = JSON.stringify({

​      students: students

​    })

​    // 把字符串保存到文件中

​    fs.writeFile(dbPath, fileData, function (err) {

​      if (err) {

​        // 错误就是把错误对象传递给它

​        return callback(err)

​      }

​      // 成功就没错，所以错误对象是 null

​      callback(null)

​    })

  })

}

