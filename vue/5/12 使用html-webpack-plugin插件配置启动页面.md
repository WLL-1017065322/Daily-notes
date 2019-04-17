

 <!-- 当使用 html-webpack-plugin 之后，我们不再需要手动处理 bundle.js 的引用路径了，因为 这个插件，已经帮我们自动 创建了一个 合适的 script , 并且，引用了 正确的路径 -->

  <!-- <script src="/bundle.js"></script> -->

## 使用`html-webpack-plugin`插件配置启动页面**

由于使用`--contentBase`指令的过程比较繁琐，需要指定启动的目录，同时还需要修改index.html中script标签的src属性，所以推荐大家使用`html-webpack-plugin`插件配置启动页面.

\1. 运行`cnpm i html-webpack-plugin --save-dev`安装到开发依赖

\2. 修改`webpack.config.js`配置文件如下：

\```

​    // 导入处理路径的模块

​    var path = require('path');

​    // 导入自动生成HTMl文件的插件

​    var htmlWebpackPlugin = require('html-webpack-plugin');

​    module.exports = {

​        entry: path.resolve(__dirname, 'src/js/main.js'), // 项目入口文件

​        output: { // 配置输出选项

​            path: path.resolve(__dirname, 'dist'), // 配置输出的路径

​            filename: 'bundle.js' // 配置输出的文件名

​        },

​        plugins:[ // 添加plugins节点配置插件

​            new htmlWebpackPlugin({

​                template:path.resolve(__dirname, 'src/index.html'),//模板路径

​                filename:'index.html'//自动生成的HTML文件的名称

​            })

​        ]

​    }





webpack.config.js

module.exports=>{}

  plugins: [ // 配置插件的节点

​    new webpack.HotModuleReplacementPlugin(), // new 一个热更新的 模块对象， 这是 启用热更新的第 3 步

​    new htmlWebpackPlugin({ // 创建一个 在内存中 生成 HTML  页面的插件

​      template: path.join(__dirname, './src/index.html'), // 指定 模板页面，将来会根据指定的页面路径，去生成内存中的 页面

​      filename: 'index.html' // 指定生成的页面的名称

​    })

  ],

