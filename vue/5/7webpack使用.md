npm init -y

npm i jquert -s

 <!-- 注意： 不推荐直接在这里引用任何包和任何CSS文件 -->

  <!-- 因为 main 中的代码，涉及到了ES6的新语法，但是浏览器不识别 -->

  <!-- <script src="./main.js"></script> -->

  <!-- 通过 webpack 这么一个前端构建工具， 把 main.js 做了一下处理，生成了一个 bundle.js 的文件 -->

  <!-- <script src="../dist/bundle.js"></script> -->

  <!-- 当使用 html-webpack-plugin 之后，我们不再需要手动处理 bundle.js 的引用路径了，因为 这个插件，已经帮我们自动 创建了一个 合适的 script , 并且，引用了 正确的路径 -->

  <!-- <script src="/bundle.js"></script> -->

  <!-- css 或发起二次请求，不推荐这么搞 -->

  <!-- <link rel="stylesheet" href="./css/index.css"> -->



main.js