+express-crud

++起步

-初始化处理

-模板处理

++路由设计

请求方法  路径  get参数 post参数 备注

get  /students      渲染首页

get /students/new 渲染添加学生页面

post /students  name ,age,gender hobbies 处理学生请求

get /students/edit id                     渲染编辑页面

posr /students/edit     id,age,gender,name,hobbies   处理编辑请求

get /students/delete id   处理删除请求 