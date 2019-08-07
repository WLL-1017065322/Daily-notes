1. 如我把nodejs安装在C盘根目录，

   配置文件npmrc的路径为："C:\nodejs\node_modules\npm\npmrc"；

   记事本打开npmrc，修改内容为：

   registry = "https://registry.npm.taobao.org/"

   prefix = C:\Program Files\nodejs

   cache = C:\Program Files\nodejs\node_cache

   说明：registry是下载源，为淘宝npm镜像仓库，prefix是全局下载的路径，cache是缓存位置了。

   刚才的缓存文件夹要新建，即在nodejs下新建node_cache文件夹。

   [![npm使用淘宝镜像，npm修改全局安装路径](https://imgsa.baidu.com/exp/w=500/sign=55555e918e35e5dd902ca5df46c7a7f5/bd3eb13533fa828bbc892320f61f4134960a5a4e.jpg)](http://jingyan.baidu.com/album/6079ad0eb015ab28ff86db89.html?picindex=3)

   

   查看当前配置：npm config ls

ps: 主要是.npmrc里面的配置