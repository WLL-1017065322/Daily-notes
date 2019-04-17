 var login = {

​            template:"<h1>nihaoo</h1> "

​        }



render：function(createElements){

//createEllement是哟个方法，可将指定组件模板渲染为html结构

return createElements(login)

//return 的结果会替换页面中的el指定的那个页面

}



和components区别：

render，整个都清空，替换，一个http只能有一个组件

