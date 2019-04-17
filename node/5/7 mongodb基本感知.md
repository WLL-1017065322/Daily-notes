连接数据库

新建cmd窗口 ： mongo+回车

退出exit +回车

基本命令：

show dbs :查看当前数据库列表

use 数据库名称  切换到指定的数据（如果没有会新建）

插入数据：

db.students.insert({'name':'jack'})

show collections

db.studnets.find()