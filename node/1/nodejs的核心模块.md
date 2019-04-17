node为js提供了很多服务器级别的API,这些api大部分包装到一个具名的核心模块了,例如,文件的fs,http服务构建的http,path路径操作模块,os操作系统信息模块



require是一个方法,用来加载模块的

加载执行代码,同时导出接口对象

exports用来导出,require用来加载

node有三种:具名的核心模块:fs,http;用户自己编写的文件模块:相对路径要加./

require('package')

var ret=require(''./....'') 默认空对象

exports.foo='hello'

+ 模块化系统:

node中没有全局作用域.只有模块作用域

外部访问不到内部,内部访问不到外部

默认都是封闭的