npm i vue -S



包的查找规则

// 1. 找 项目根目录中有没有 node_modules 的文件夹

// 2. 在 node_modules 中 根据包名，找对应的 vue 文件夹

// 3. 在 vue 文件夹中，找 一个叫做 package.json 的包配置文件

// 4. 在 package.json 文件中，查找 一个 main 属性【main属性指定了这个包在被加载时候，的入口文件】



1，

main.js

import Vue from '../node_modules/vue/dist/vue.js'

2main.js:



import Vue from 'vue'

webpack.config.js:

module.exports=>

resolve: {

​    alias: { // 修改 Vue 被导入时候的包的路径

​      // "vue$": "vue/dist/vue.js"

​    }

  }