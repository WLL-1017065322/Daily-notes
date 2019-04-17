-npm网站 :https://www.npmjs.com/

-npm 命令行工具   装了node就是装了npm

​	+npm --version

​	+升级npm npm install --global npm

-常用命令

 +npm init [--yes]

​	npm init -y 快速生成，跳过

+npm install 一次性把dependencies选项中的依赖项全部安装 npm i

+npm install 包名----只下载 npm i 包名

+npm install --save--下载并保存依赖项 npm i -S

+npm uninstall 只删除，保存依赖项 npm un

+npm uninstall 同时删除依赖项 npm un -S

+npm --help

+npm 命令 --help 例如;npm unstall --help-s



解决npm 被墙问题 http://npm.taobao.org/ 淘宝开发团队 做了一个备份

安装淘宝的cnpm: npm install --globa cnpm  --globa不可省略

把之前的npm替换成cnpm

不想安装cnpm但用淘宝服务器：

npm install jquery --registry=https：//registry.npm.taobao.org

麻烦，可把这个选项加入到配置文件中：

npm config set registry https：//registry.npm.taobao.org

以后默认通过淘宝的服务器下载

验证：npm config list



