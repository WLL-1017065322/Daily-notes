涉及面试题：
1. 从 URL 输入到页面展现背后发生了什么事？
2. 一次完整的 HTTP 事务是怎么一个过程？
3. 浏览器是如何渲染页面的？
4. 浏览器的内核有哪些？分别有什么代表的浏览器？
5. 刷新页面，js 请求一般会有哪些地方有缓存处理？



#### 一、从 URL 输入到页面展现背后发生了什么事？

1. 浏览器根据请求的 URL 交给 DNS 域名解析，找到真实 IP，向服务器发起请求；

2. 服务器交给后台处理完成后返回数据，浏览器接收文件（HTML、JS、CSS、图象等）；

3. 浏览器对加载到的资源（HTML、JS、CSS 等）进行语法解析，建立相应的内部数据结构（如 HTML 的 DOM）；

4. 载入解析到的资源文件，渲染页面，完成。

   

#### 二、一次完整的 HTTP 事务是怎么一个过程？

1. 域名解析；
2. 发起 TCP 的三次握手；
3. 建立 TCP 连接后发起 http 请求；
4. 服务器端响应 http 请求，浏览器得到 html 码；
5. 浏览器解析 html 代码，并请求 html 代码中的资源；
6. 浏览器对页面进行渲染并呈现给客户。

#### 三、浏览器是如何渲染页面的？

浏览器页面渲染流程：

浏览器从 HTTP 服务器获取 html 文档，到呈现页面给用户，会经过以下几个步骤：

**1. 解析文档构建 DOM 树**

浏览器的解析内容可以分为三个部分：

- HTML/XHTML/SVG：解析这三种文件后，会生成 DOM 树（DOM Tree）；
- CSS：解析样式表，生成 CSS 规则树（CSS Rule Tree）；
- JavaScript：解析脚本，通过 DOM API 和 CSSOM API 操作 DOM Tree 和 CSS Rule Tree，与用户进行交互。

以上三类文件的执行顺序会根据其在文档中的位置及其标签属性的不同而有异同。



**2. 构建渲染树**

解析文档完成后，浏览器引擎会将 CSS Rule Tree 附着到 DOM Tree 上，并根据 DOM Tree 和 CSS Rule Tree 构造 Rendering Tree（渲染树）。

此处需要注意：

- Render Tree 和 DOM Tree 的区别在于，类似 Head 或 display: none; 之类的东西不会放在渲染树中；
- 将 CSS Rule Tree 匹配到 DOM Tree需要解析 CSS 的选择器，为了提高该过程的性能，DOM 树应该尽量小，CSS Selector 应该尽量使用 id 和 class，避免过度层叠。



**3. 布局与绘制渲染树**

解析 position，overflow，z-index 等等属性，计算每一个渲染树节点的位置和大小，此过程被称为 reflow。最后调用操作系统的 Native GUI API 完成绘制（repain）。

注意：

渲染树的节点，在 Gecko 中称为 frame，而在 webkit 中称为 renderer。

#### 四、浏览器的内核有哪些？分别有什么代表的浏览器？

**Trident 内核**：代表作品是 IE。

**Gecko 内核**：代表作品是 Firefox，即火狐浏览器。

**Webkit 内核**：代表作品是 Safari Chromewebkit、曾经的 Chrome，是开源的项目。

**Presto 内核**：代表作品是 Opera ，Presto 是由 Opera Software 开发的浏览器排版引擎，它是世界公认最快的渲染速度的引擎。在 13 年之后，Opera 宣布加入谷歌阵营，弃用了 Presto。

**Blink 内核**：由 Google 和 Opera Software 开发的浏览器排版引擎，2013 年 4 月发布。现在 Chrome 内核是 Blink。谷歌还开发了自己的 JS 引擎，V8，使 JS 运行速度极大地提高了。



#### 五、刷新页面，js 请求一般会有哪些地方有缓存处理？

1. DNS 缓存：短时间内多次访问某个网站，在限定时间内，不用多次访问 DNS 服务器；
2. CDN 缓存：内容分发网络（人们可以在就近的代售点取火车票了，不用非得到火车站去排队）；
3. 浏览器缓存：浏览器在用户磁盘上，对最新请求过的文档进行了存储；
4. 服务器缓存：将需要频繁访问的 Web 页面和对象保存在离用户更近的系统中，当再次访问这些对象的时候加快了速度。

