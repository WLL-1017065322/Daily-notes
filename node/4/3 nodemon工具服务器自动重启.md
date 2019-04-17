使用第三方工具 nodemon 解决频繁重启服务器问题

是一个基于nodejs 第三方命令行工具

globle任意目录执行；

npm install --global nodemon



node app.js

nodemon app.js

只要是nodemon 启动的服务，会监视文件变化，自动重启服务器

验证 nodemon --version