HTML&CSS：
    对Web标准的理解、浏览器内核差异、兼容性、hack、CSS基本功：布局、盒子模型、选择器优先级、
    HTML5、CSS3、Flexbox



1. doctype 有什么作用？怎么写？

2. 列出常见的标签，并简单介绍这些标签用在什么场景？

3. 页面出现了乱码，是怎么回事？如何解决？

4. title 属性和 alt 属性分别有什么作用？

5. html 的注释怎样写？

6. HTML5 为什么只写 \<!DOCTYPE HTML> ？

7. data- 属性的作用？

8. \<img> 的 title 和 alt 有什么区别？

9. WEB 标准以及 W3C 标准是什么？

   

   10. doctype 作用? 严格模式与混杂模式如何区分？它们有何意义?

   11. HTML 全局属性（global attribute）有哪些

       

   12. meta 有哪些常见的值？

   13. meta viewport 是做什么用的，怎么写？

   14. 

   15. 如何在 html 页面上展示 <div></div> 这几个字符？

   16. 你是如何理解 HTML 语义化的？

   17. 前端需要注意哪些 SEO?

   18. 你对网页标准和 W3C 重要性的理解?



19 post 和 get 方式提交数据有什么区别？

20 在 input 里，name 有什么作用？

21 label 有什么作用？如何使用？

22 radio 如何分组？

23 placeholder 属性有什么作用？

24 type=hidden 隐藏域有什么作用？举例说明。

25 CSRF 攻击是什么？如何防范？

26 网页验证码是干嘛的？是为了解决什么安全问题？

27 常见 web 安全及防护原理？

28 html5的新特性:

1、标签语义化，

2、音视频元素，

3、新增很多api，

4、websocket

5、webstorage，

6、缓存  html5允许我们自己控制哪些文件需要缓存，哪些不需要，具体的做法如下：

29 对html5的语义话的理解

30 cookie，sessionStorage，localeStorage的区别

31 多个页面之间如何进行通信

32 浏览器的渲染过程

33 重构、回流





**34.HTML 中 Doctype 的用途是什么？**

具体谈谈，以下每种情况下会发生什么：

1. Doctype 不存在。
2. 使用了 HTML4 Doctype，但 HTML 页面使用了 HTML5 的标签，如 `<audio>` 或 `<video>` 。它会导致任何错误吗？
3. 使用了无效的 Doctype。



**35 .使用单页应用将文件上传到服务器的有哪些方法？**

提示：XMLHttpRequest2（streaming），fetch（non-streaming），File API



**36.为 script 标签定义的 async 和 defer 属性有什么用？**



37 Doctype作用？标准模式与兼容模式各有什么区别?

38 HTML5 为什么只需要写 <!DOCTYPE HTML>？

39 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些

40 页面导入样式时，使用link和@import有什么区别？

41 介绍一下你对浏览器**内核**的理解

42 常见的浏览器内核有哪些？

43 html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？

44 简述一下你对HTML语义化的理解？

45 HTML5的离线储存怎么使用，工作原理能不能解释一下？

46 浏览器是怎么对HTML5的离线储存资源进行管理和加载的呢？

47 请描述一下 cookies，sessionStorage 和 localStorage 的区别？

48 iframe有那些缺点？

49 Label的作用是什么？是怎么用的？

50 HTML5的form如何关闭自动完成功能？

51 如何实现浏览器内多个标签页之间的通信? (阿里)

52 webSocket如何兼容低浏览器？(阿里)

53 页面可见性（Page Visibility API） 可以有哪些用途？

54 如何在页面上实现一个圆形的可点击区域？

55 实现不使用 border 画出1px高的线，在不同浏览器的标准模式与怪异模式下都能保持一致的效果。

56 网页验证码是干嘛的，是为了解决什么安全问题。

57 title与h1的区别、b与strong的区别、i与em的区别？

58 对web标准的理解

59 html5

60 你如何理解HTML结构的语意化?

61 Doctype文档声明的严格模式和混杂模式，如何触发这两种模式，区分它们有何意义? 

62 html元素的id跟class什么区别

63 html5 离线存储

64 iframe的优缺点？



1. doctype 有什么作用？怎么写？

   DOCTYPE 标签是一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义（DTD）来解析文档。

   每个页面都要从 doctype 开始，它为浏览器指定这个页面的文档类型，以便浏览器更正确的显示 HTML。只要按照`<!DOCTYPE html> `这样的格式和位置写，那么浏览器就会认为你在使用标准 HTML。

   **怎么写：**

   \1. doctype 之前只能有注释和空白；

   \2. doctype 拼写大小写无所谓，但推荐一致：

   \<!DOCTYPE html>

   \<!doctype html> 

1. 列出常见的标签，并简单介绍这些标签用在什么场景？

   - 如果是标题，就用 `<h1>` ~ `<h6>`；
   - 如果是一段话，就用 `<p>`；
   - 如果不知道他是什么，如果这个东西能占一行，就用`<div>`；
   - 如果没有一行，就一个小小的位置，就用`<span>`；
   - 如果是可点击的就用一个`<a>`链接；
   - 如果像那种并列一排排的，甚至还有一点一点，就用“列表”；
   - 如果看到一个表格，就用`<table>`；
   - 如果看到了一个输入框，就用`<input>`。

2. 页面出现了乱码，是怎么回事？如何解决？

   - 当我们保存一个写好的 HTML 文件，编码方式会保存为 UTF-8；
   - 一个文件就是一堆的数据，即我们写的内容变成了一堆的数据。那这个数据到底是变成了 123，还是 456 呢？
   - 这里我们就用到了“编码”，用的编码方式不一样，那么数据呈现的状态就不一样；
   - 然后，当我们把这个以适当编码方式保存好的数据再次展示在浏览器页面上时（或用其他编辑器打开时），这个数据还要再恢复出来；
   - 这时候，浏览器（或编辑器）需要使用相同的、与文件相对应的编码方式去解码（但浏览器不是万能的，你不告诉他，他就不知道用什么方式去解码，他会随意选择）；
   - 这时，当编码是一种方式，而解码又是另一种方式时，页面就会出现“乱码”；而解决乱码的方式就是：只需要知道我在编辑器保存这个 HTML 文件时，保存的什么编码格式，然后在头部 `<meta charset="?">`中告诉浏览器用什么方式来解码。

   

3. title 属性和 alt 属性分别有什么作用？

   title 属性有一个很好的用途：即为链接添加描述性文字，特别是当链接本身并不是十分清楚的表达了链接的目的。

   这样就使得访问者知道那些链接将会带他们到什么地方，他们就不会加载一个可能完全不感兴趣的页面。

   另外一个潜在的应用就是为图像提供额外的说明信息，比如日期或者其他非本质的信息。

   

   alt 这个属性主要是为了规避例如：因网速差、硬件设备限制等外部因素，我们的浏览器不能很好的显示出图像，那 alt 后边的文本将会取代图像告诉用户这里会是什么东西。

   ```
   <a href="这里写链接地址“ title="Oli的前端一万小时">知乎-oliver</a>
   
   <!-- 注释：这里的 title 属性，作用就是：当我们把鼠标停在 oliver 上时，会弹出一个文本框：
   Oli-Zhao的前端一万小时。 -->
   ```

4. html 的注释怎样写？

   <!--这是注释-->

5. HTML5 为什么只写 \<!DOCTYPE HTML> ？

   HTML5 不基于 SGML，因此不需要对 DTD 进行引用，但是需要 doctype 来规范浏览器的行为（让浏览器按照他们应该的方式来运行）。

   而 HTML4.01 基于 SGML，所以需要对 DTD 进行引用，才能告知浏览器文档所使用的文档类型。

   

6. data- 属性的作用？

   data- 为 H5 新增的为前端开发者提供自定义的属性，这些属性集可以通过对象的 dataset 属性获取；

   不支持该属性的浏览器可以通过 getAttribute 方法获取 。

   需要注意的是：data- 之后的以连字符分割的多个单词组成的属性，获取的时候使用驼峰风格。 所有主流浏览器都支持 data-* 属性。

   即：当没有合适的属性和元素时，自定义的 data 属性是能够存储页面或 App 的私有的自定义数据。

   

7. \<img> 的 title 和 alt 有什么区别？

   - title 通常当鼠标滑动到元素上的时候显示；
   - alt 是 <img> 的特有属性，是图片内容的等价描述，用于图片无法加载时显示、读屏器阅读图片。可提图片高可访问性，除了纯装饰图片外都必须设置有意义的值，搜索引擎会重点分析。

8. WEB 标准以及 W3C 标准是什么？

   标签闭合、标签小写、不乱嵌套、使用外链 css 和 js、结构行为表现的分离。

   

9. doctype 作用? 严格模式与混杂模式如何区分？它们有何意义?

   \<!DOCTYPE> 声明位于文档中的最前面，处于\<html> 标签之前。告知浏览器的解析器， 用什么文档类型 规范来解析这个文档。

   严格模式的排版和 JS 运作模式是 以该浏览器支持的最高标准运行。

   在混杂模式中，页面以宽松的向后兼容的方式显示，模拟老式浏览器的行为以防止站点无法工作。DOCTYPE 不存在或格式不正确会导致文档以混杂模式呈现。

   

10. HTML 全局属性（global attribute）有哪些

    - class：为元素设置类标识；
    - data-*：为元素增加自定义属性；
    - draggable：设置元素是否可拖拽；
    - id：元素 id，文档内唯一；
    - lang：元素内容的的语言；
    - style：行内 css 样式；
    - title：元素相关的建议信息。

    

    

    



##### 19 html中form里action方法的get和post有什么区别？

- 1、Get是用来从服务器上获得数据，而Post是用来向服务器上传递数据。
- 2、Get将表单中数据的按照variable=value的形式，添加到action所指向的URL后面，并且两者使用"?"连接，而各个变量之间使用"&"连接。Post是将表单中的数据放在form的数据体中，按照变量和值相对应的方式，传递到action所指向URL。
- 3、Get是不安全的，因为在传输过程，数据被放在请求的URL中，而如今现有的很多服务器、代理服务器或者用户代理都会将请求URL记录到日志文件中，然后放在某个地方，这样就可能会有一些隐私的信息被第三方看到。另外，用户也可以在浏览器上直接看到提交的数据，一些系统内部消息将会一同显示在用户面前。Post的所有操作对用户来说都是不可见的。
- 4、Get传输的数据量小，这主要是因为受URL长度限制。而Post可以传输大量的数据，所以在上传文件只能使用Post（当然还有一个原因，将在后面的提到）。
- 5、Get限制Form表单的数据集的值必须为ASCII字符。而Post支持整个ISO10646字符集。
- 6、Get是Form的默认方法。







**28 html5的新特性**

1、标签语义化，比如header，footer，nav，aside，article，section等，新增了很多表单元素，入email，url等，除去了center等样式标签，还有除去了有性能问题的frame，frameset等标签

2、音视频元素，video，audio的增加使得我们不需要在依赖外部的插件就可以往网页中加入音视频元素。

3、新增很多api，比如获取用户地理位置的window.navigator.geoloaction，

4、websocket

websocket是一种协议，可以让我们建立客户端到服务器端的全双工通信，这就意味着服务器端可以主动推送数据到客户端，

5、webstorage，webstorage是本地存储，存储在客户端，包括localeStorage和sessionStorage，localeStorage是持久化存储在客户端，只要用户不主动删除，就不会消失，sessionStorage也是存储在客户端，但是他的存在时间是一个回话，一旦浏览器的关于该回话的页面关闭了，sessionStorage就消失了，

6、缓存

html5允许我们自己控制哪些文件需要缓存，哪些不需要，具体的做法如下：

```js
1、首先给html添加manifest属性，并赋值为cache.manifest
2、cache.manifest的内容为: 
         CACHE MANIFEST
         #v1.2
         CACHE :           //表示需要缓存的文件
           a.js
           b.js
       NETWORK:    //表示只在用户在线的时候才需要的文件，不会缓存
         c.js
       FALLBACK
       /        /index.html     //表示如果找不到第一个资源就用第二个资源代替
```

7、web worker，web worker是运行在浏览器后台的js程序，他不影响主程序的运行，是另开的一个js线程，可以用这个线程执行复杂的数据操作，然后把操作结果通过postMessage传递给主线程，这样在进行复杂且耗时的操作时就不会阻塞主线程了。

**29 对html5的语义话的理解**

html5的语义化指的是用正确的标签包含正确的内容，比如nav标签，里面就应该包含导航条的内容，而不是用做其他的用途，标签语义化的好处就是结构良好，便于阅读，方便威化，也有利于爬虫的查找，提高搜索率。



**30 cookie，sessionStorage，localeStorage的区别**

cookie是存储在浏览器端，并且随浏览器的请求一起发送到服务器端的，它有一定的过期时间，到了过期时间自动会消失。sessionStorage和localeStorage也是存储在客户端的，同属于web Storage，比cookie的存储大小要大有8m，cookie只有4kb，localeStorage是持久化的存储在客户端，如果用户不手动清除的话，不会自动消失，会一直存在，sessionStorage也是存储在客户端，但是它的存活时间是在一个回话期间，只要浏览器的回话关闭了就会自动消失。

**31 多个页面之间如何进行通信**

使用cookie，使用web worker，使用localeStorage和sessionStorage

**32 浏览器的渲染过程**

1、首先获取html，然后构建dom树

2、其次根据css构建render树，render树中不包含定位和几何信息

3、最后构建布局数，布局是含有元素的定位和几何信息

**33 重构、回流**

浏览器的重构指的是改变每个元素外观时所触发的浏览器行为，比如颜色，背景等样式发生了改变而进行的重新构造新外观的过程。重构不会引发页面的重新布局，不一定伴随着回流，

回流指的是浏览器为了重新渲染页面的需要而进行的重新计算元素的几何大小和位置的，他的开销是非常大的，回流可以理解为渲染树需要重新进行计算，一般最好触发元素的重构，避免元素的回流；比如通过通过添加类来添加css样式，而不是直接在DOM上设置，当需要操作某一块元素时候，最好使其脱离文档流，这样就不会引起回流了，比如设置position：absolute或者fixed，或者display：none，等操作结束后在显示。













**34 .HTML 中 Doctype 的用途是什么？**

具体谈谈，以下每种情况下会发生什么：

1. Doctype 不存在。
2. 使用了 HTML4 Doctype，但 HTML 页面使用了 HTML5 的标签，如 `<audio>` 或 `<video>` 。它会导致任何错误吗？
3. 使用了无效的 Doctype。



**35.使用单页应用将文件上传到服务器的有哪些方法？**

提示：XMLHttpRequest2（streaming），fetch（non-streaming），File API





**36.为 script 标签定义的 async 和 defer 属性有什么用？**

现在我们有 HTTP/2 和 ES 模块，它们真的很有用吗？

列出的清单只是我们在面试中可能讨论的无限点的一瞥。Web Components，CORS，安全性，Cookies，CSS transform，Web Assembly，Service Workers，PWA，CSS架构等，还有许多我们没有考虑到的东西。我们也没有涉及框架或库的具体问题











37 Doctype作用？标准模式与兼容模式各有什么区别?

```
（1）、<!DOCTYPE>声明位于位于HTML文档中的第一行，处于 <html> 标签之前。告知浏览器的解析器用什么文档标准解析这个文档。DOCTYPE不存在或格式不正确会导致文档以兼容模式呈现。

（2）、标准模式的排版 和JS运作模式都是以该浏览器支持的最高标准运行。在兼容模式中，页面以宽松的向后兼容的方式显示,模拟老式浏览器的行为以防止站点无法工作。
```

38 HTML5 为什么只需要写 <!DOCTYPE HTML>？

```
HTML5 不基于 SGML，因此不需要对DTD进行引用，但是需要doctype来规范浏览器的行为（让浏览器按照它们应该的方式来运行）；

 而HTML4.01基于SGML,所以需要对DTD进行引用，才能告知浏览器文档所使用的文档类型。
```

39 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

```
首先：CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，如div的display默认值为“block”，则为“块级”元素；span默认display属性值为“inline”，是“行内”元素。

（1）行内元素有：a b span img input select strong（强调的语气）
（2）块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p

（3）常见的空元素：
    <br> <hr> <img> <input> <link> <meta>
    鲜为人知的是：
    <area> <base> <col> <command> <embed> <keygen> <param> <source> <track> <wbr>
```

40 页面导入样式时，使用link和@import有什么区别？

```
（1）link属于XHTML标签，除了加载CSS外，还能用于定义RSS, 定义rel连接属性等作用；而@import是CSS提供的，只能用于加载CSS;

（2）页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;

（3）import是CSS2.1 提出的，只在IE5以上才能被识别，而link是XHTML标签，无兼容问题;
```

41 介绍一下你对浏览器**内核**的理解？

```
42主要分成两部分：渲染引擎(layout engineer或Rendering Engine)和JS引擎。
渲染引擎：负责取得网页的内容（HTML、XML、图像等等）、整理讯息（例如加入CSS等），以及计算网页的显示方式，然后会输出至显示器或打印机。浏览器的内核的不同对于网页的语法解释会有不同，所以渲染的效果也不相同。所有网页浏览器、电子邮件客户端以及其它需要编辑、显示网络内容的应用程序都需要内核。

JS引擎则：解析和执行javascript来实现网页的动态效果。

最开始渲染引擎和JS引擎并没有区分的很明确，后来JS引擎越来越独立，内核就倾向于只指渲染引擎。
```

42 常见的浏览器内核有哪些？

```
Trident内核：IE,MaxThon,TT,The World,360,搜狗浏览器等。[又称MSHTML]
Gecko内核：Netscape6及以上版本，FF,MozillaSuite/SeaMonkey等
Presto内核：Opera7及以上。      [Opera内核原为：Presto，现为：Blink;]
Webkit内核：Safari,Chrome等。   [ Chrome的：Blink（WebKit的分支）]
```

详细文章：[浏览器内核的解析和对比](http://www.cnblogs.com/fullhouse/archive/2011/12/19/2293455.html)

43 html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？

```
* HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，多任务等功能的增加。
      绘画 canvas;
      用于媒介回放的 video 和 audio 元素;
      本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失;
      sessionStorage 的数据在浏览器关闭后自动删除;
      语意化更好的内容元素，比如 article、footer、header、nav、section;
      表单控件，calendar、date、time、email、url、search;
      新的技术webworker, websocket, Geolocation;

  移除的元素：
      纯表现的元素：basefont，big，center，font, s，strike，tt，u;
      对可用性产生负面影响的元素：frame，frameset，noframes；

* 支持HTML5新标签：
     IE8/IE7/IE6支持通过document.createElement方法产生的标签，
     可以利用这一特性让这些浏览器支持HTML5新标签，
     浏览器支持新标签后，还需要添加标签默认的样式。

     当然也可以直接使用成熟的框架、比如html5shim;
     <!--[if lt IE 9]>
        <script> src="//cdn.bootcss.com/html5shiv/r29/html5.min.js"</script>
     <![endif]-->

* 如何区分HTML5： DOCTYPE声明\新增的结构元素\功能元素
```

44 简述一下你对HTML语义化的理解？

```
用正确的标签做正确的事情。
html语义化让页面的内容结构化，结构更清晰，便于对浏览器、搜索引擎解析;
即使在没有样式CSS情况下也以一种文档格式显示，并且是容易阅读的;
搜索引擎的爬虫也依赖于HTML标记来确定上下文和各个关键字的权重，利于SEO;
使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。
```

45 HTML5的离线储存怎么使用，工作原理能不能解释一下？

```
在用户没有与因特网连接时，可以正常访问站点或应用，在用户与因特网连接时，更新用户机器上的缓存文件。
原理：HTML5的离线存储是基于一个新建的.appcache文件的缓存机制(不是存储技术)，通过这个文件上的解析清单离线存储资源，这些资源就会像cookie一样被存储了下来。之后当网络在处于离线状态下时，浏览器会通过被离线存储的数据进行页面展示。


如何使用：
1、页面头部像下面一样加入一个manifest的属性；
2、在cache.manifest文件的编写离线存储的资源；
    CACHE MANIFEST
    #v0.11
    CACHE:
    js/app.js
    css/style.css
    NETWORK:
    resourse/logo.png
    FALLBACK:
    / /offline.html
3、在离线状态时，操作window.applicationCache进行需求实现。
```

详细的使用请参考：[有趣的HTML5：离线存储](http://segmentfault.com/a/1190000000732617)

46 浏览器是怎么对HTML5的离线储存资源进行管理和加载的呢？

```
在线的情况下，浏览器发现html头部有manifest属性，它会请求manifest文件，如果是第一次访问app，那么浏览器就会根据manifest文件的内容下载相应的资源并且进行离线存储。如果已经访问过app并且资源已经离线存储了，那么浏览器就会使用离线的资源加载页面，然后浏览器会对比新的manifest文件与旧的manifest文件，如果文件没有发生改变，就不做任何操作，如果文件改变了，那么就会重新下载文件中的资源并进行离线存储。
离线的情况下，浏览器就直接使用离线存储的资源。
```

详细的使用请参考：[有趣的HTML5：离线存储](http://segmentfault.com/a/1190000000732617)

47 请描述一下 cookies，sessionStorage 和 localStorage 的区别？

```
cookie是网站为了标示用户身份而储存在用户本地终端（Client Side）上的数据（通常经过加密）。
cookie数据始终在同源的http请求中携带（即使不需要），记会在浏览器和服务器间来回传递。
sessionStorage和localStorage不会自动把数据发给服务器，仅在本地保存。

存储大小：
    cookie数据大小不能超过4k。
    sessionStorage和localStorage 虽然也有存储大小的限制，但比cookie大得多，可以达到5M或更大。

有期时间：
    localStorage    存储持久数据，浏览器关闭后数据不丢失除非主动删除数据；
    sessionStorage  数据在当前浏览器窗口关闭后自动删除。
    cookie          设置的cookie过期时间之前一直有效，即使窗口或浏览器关闭
```

48 iframe有那些缺点？

```
*iframe会阻塞主页面的Onload事件；
*搜索引擎的检索程序无法解读这种页面，不利于SEO;

*iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。

使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript
动态给iframe添加src属性值，这样可以绕开以上两个问题。
```

49 Label的作用是什么？是怎么用的？

```
label标签来定义表单控制间的关系,当用户选择该标签时，浏览器会自动将焦点转到和标签相关的表单控件上。

<label for="Name">Number:</label>
<input type=“text“name="Name" id="Name"/>

<label>Date:<input type="text" name="B"/></label>
```

50 HTML5的form如何关闭自动完成功能？

```
给不想要提示的 form 或某个 input 设置为 autocomplete=off。
```

51 如何实现浏览器内多个标签页之间的通信? (阿里)

```
WebSocket、SharedWorker；
也可以调用localstorge、cookies等本地存储方式；

localstorge另一个浏览上下文里被添加、修改或删除时，它都会触发一个事件，
我们通过监听事件，控制它的值来进行页面信息通信；
注意quirks：Safari 在无痕模式下设置localstorge值时会抛出 QuotaExceededError 的异常；
```

52 webSocket如何兼容低浏览器？(阿里)

```
Adobe Flash Socket 、
ActiveX HTMLFile (IE) 、
基于 multipart 编码发送 XHR 、
基于长轮询的 XHR
```

53 页面可见性（Page Visibility API） 可以有哪些用途？

```
通过 visibilityState 的值检测页面当前是否可见，以及打开网页的时间等;
在页面被切换到其他后台进程的时候，自动暂停音乐或视频的播放；
```

54 如何在页面上实现一个圆形的可点击区域？

```
1、map+area或者svg
2、border-radius
3、纯js实现 需要求一个点在不在圆上简单算法、获取鼠标坐标等等
```

55 实现不使用 border 画出1px高的线，在不同浏览器的标准模式与怪异模式下都能保持一致的效果。

```
<div style="height:1px;overflow:hidden;background:red"></div>
```

56 网页验证码是干嘛的，是为了解决什么安全问题。

```
区分用户是计算机还是人的公共全自动程序。可以防止恶意破解密码、刷票、论坛灌水；
有效防止黑客对某一个特定注册用户用特定程序暴力破解方式进行不断的登陆尝试。
```

57 title与h1的区别、b与strong的区别、i与em的区别？

```
title属性没有明确意义只表示是个标题，H1则表示层次明确的标题，对页面信息的抓取也有很大的影响；

strong是标明重点内容，有语气加强的含义，使用阅读设备阅读网络时：<strong>会重读，而<B>是展示强调内容。

i内容展示为斜体，em表示强调的文本；

Physical Style Elements -- 自然样式标签
b, i, u, s, pre
Semantic Style Elements -- 语义样式标签
strong, em, ins, del, code
应该准确使用语义样式标签, 但不能滥用, 如果不能确定时首选使用自然样式标签。
```

58 对web标准的理解

```
WEB标准不是某一个标准，而是一系列标准的集合。
网页主要由三部分组成：结构（Structure）、表现（Presentation）和行为（Behavior）。对应的标准也分三方面：结构化标准语言主要包括XHTML和XML，表现标准语言主要包括CSS，行为标准主要包括对象模型（如W3C DOM）、ECMAScript等

WEB标准（结构、表现、行为分离）有哪些优点呢?
易于维护：只需更改CSS文件，就可以改变整站的样式
页面响应快：HTML文档体积变小，响应时间短
可访问性：语义化的HTML（结构和表现相分离的HTML）编写的网页文件，更容易被屏幕阅读器识别
设备兼容性：不同的样式表可以让网页在不同的设备上呈现不同的样式
搜索引擎：语义化的HTML能更容易被搜索引擎解析，提升排名

```

59 html5

HTML5的设计目的是为了在移动设备上支持多媒体。

HTML , HTML 4.01的上一个版本诞生于 1999 年

H5新特性：

- 新增选择器 document.querySelector、document.querySelectorAll
- 拖拽释放(Drag and drop) API
- 媒体播放的 video 和 audio
- 本地存储 localStorage 和 sessionStorage
- 离线应用 manifest
- 桌面通知 Notifications
- 语意化标签8个 header, section, footer, aside, nav, main, article, figure
- 增强表单控件 calendar、date、time、email、url、search
- 地理位置 Geolocation
- 多任务 webworker
- 全双工通信协议 websocket
- 历史管理 history
- 跨域资源共享(CORS) Access-Control-Allow-Origin
- 页面可见性改变事件 visibilitychange
- 跨窗口通信 PostMessage
- Form Data 对象
- 绘画 canvas

H5移除的元素：

- 纯表现的元素：basefont、big、center、font、s、strike、tt、u

- 对可用性产生负面影响的元素：frame、frameset、noframes

  ```
  (一)语义化标签 
  ```

     （二）增强型表单
     （三）视频和音频
     （四）Canvas绘图
     （五）SVG绘图
     （六）地理定位
     （七）拖放API
     （八）WebWorker
     （九）WebStorage
     （十）WebSocket
     	MathML 
     	websql
     	应用程序缓存
     	sse服务器发送事件(Server-Sent Events)
     	

（一）   语义标签

```
HTML语义化是什么？
语义化是指根据内容的结构化（内容语义化），选择合适的标签（代码语义化），便于开发者阅读和写出更优雅的代码的同时，让浏览器的爬虫和机器很好的解析。
为什么要语义化？
有利于SEO，有助于爬虫抓取更多的有效信息，爬虫是依赖于标签来确定上下文和各个关键字的权重。
语义化的HTML在没有CSS的情况下也能呈现较好的内容结构与代码结构
方便其他设备的解析
便于团队开发和维护
　　1、<section></section>
　　　　定义文档中的主体部分的节、段。
　　2、<article></article>
　　　　一个特殊的section标签，比section有更明确的语义。定义来自外部的一个独立的、完整的内容块，例如什么论坛的文章，博客的文本。。。
　　3、<aside></aside>
　　　　用来装载页面中非正文的内容，独立于其他模块。例如广告、成组的链接、侧边栏。。。
　　4、<header></header>
　　　　定义文档、页面的页眉。通常是一些引导和导航信息，不局限于整个页面头部，也可以用在内容里。
　　5、<footer></footer>
　　　　定义了文档、页面的页脚，和header类似。
　　6、<nav></nav>
　　　　定义了一个链接组组成的导航部分，其中的链接可以链接到其他网页或者当前页面的其他部分。
　　7、<hgroup></hgroup>
　　　　用于对网页或区段(section)的标题元素(h1~h6)进行组合。
　　8、<figure></figure>
　　　　用于对元素进行组合。
　　9、<figcaption></figcaption>
　　　　为figure元素加标题。一般放在figure第一个子元素或者最后一个。
　　10、<details></details>
　　　　定义元素的细节，用户可以点击查看或者隐藏。
　　11、<summary></summary>
　　　　和details连用，用来包含details的标题。
　　12、<canvas></canvas>
　　　　用来进行canvas绘图。
　　13、<video></video>
　　　　定义视频。
　　14、<audio></audio>
　　　　定义音频。
　　15、<embed></embed>
　　　　定义嵌入网页的内容。比如插件。
　　16、<source></source>
　　　　该标签为媒介元素(比如video、audio)定义媒介元素。
　　17、<datalist id='dl'></datalist>
　　　　定义可选数据的列表，与input配合使用(<input list='dl'>)可制作输入值的下拉列表。
　　18、<mark></mark>
　　　　在视觉上向用户展现出那些想要突出的文字。比如搜索结果中向用户高亮显示搜索关键词。
　　19、<meter [min/max/low/high/optimum/value]></meter>
　　　　度量衡，用红黄绿表示出一个数值所在范围。
　　20、<output></output>
　　　　定义不同类型的输出，样式与span无异。
　　21、<progress></progress>
　　　　进度条，运行中的进度。
　　22、<time></time>
　　　　定义日期或者时间。
　　23、<keygen></keygen>
　　　　定义加密内容。
　　24、<command></command>
　　　　定义命令行为。
```



（二）增强型表单/表单2.0

```
      1)新的input type

       2)新的表单元素

              <input><textarea><select><option>....

               <datalist>：数据列表，为input提供输入建议列表

               <progress>：进度条，展示连接/下载进度

               <meter>：刻度尺/度量衡，描述数据所处的阶段，红色(危险)=>黄色(警告)=>绿色(优秀)

               <output>：输出内容，语义上表示此处的数据是经过计算而输出得到的

       3)表单元素的新属性

               通用属性：

                        placeholder：占位提示文字

                        mutiple：是否允许多个输入

                        autofocus：自动获得输入焦点

                        form：指定输入元素所从属的表单，可以实现输入框放在表单外部并能被提交的效果

               验证属性(了解即可)：

                        required：输入框内容不能为空

                        min：允许输入的数字最小值

                        max：允许输入的数字最大值

                        minlength：允许输入的字符串最小长度

                        maxlength：允许输入的字符串最大长度

                        pattern：输入框内容必须符合的正则表达式
```

（三）视频和音频         

```
       视频播放：<video src=""><video>

       查看视频的所有属性、方法、事件：console.log(videoBirds);

       音频播放：<audio src=""></audio>

       查看视频的所有属性、方法、事件：console.log(bgMusic);
```

```
		WEB中可用的绘图技术：

		(1)Canvas绘图：H5原生技术，基于网页画布绘制2D位图绘图技术，善于表现细腻颜色

		(2)SVG绘图：H5借鉴技术，基于SVG绘图空间绘制2D矢量图绘图技术，缩放不会失真

		(3)WebGL绘图：尚不是H5标准技术，基于HTML5 Canvas提供硬件3D加速渲染；有一个非常强大3D扩展库：three.js
		
	（四）Canvas绘图         

      H5原生技术，基于网页画布2D位图绘图技术，善于表现细腻颜色，可用于统计图表、页面游戏、地图应用、网页特效等。

      使用Canvas的步骤：

       <canvas id="c2" width="400" height="300"></canvas>

     Canvas自身是一个300*150的inline-block元素；注意：Canvas画布尺寸不能使用CSS设置——会对整个图像进行扭曲！

     使用H5 Canvas API进行绘图：

         var ctx = c2.getContext('2d'); 

         //绘制矩形

         ctx.fillStyle = '#000'                  填充颜色/渐变色对象

         ctx.strokeStyle = '#000'           描边颜色/渐变色对象

         ctx.lineWidth = 1                      描边线宽度

         ctx.fillRect(x, y, w, h)：              填充矩形

         ctx.strokeRect(x, y, w, h)：       描边矩形

         ctx.clearRect(x, y, w, h)：          描边矩形

         //绘制文本

         ctx.font = '10px sans-serif'    

         ctx.textBaseline = 'alphabetic/top/bottom'

         ctx.fillStyle = '#000'                 

         ctx.strokeStyle = '#000'

         ctx.fillText(txt, x, y)                    填充文本

         ctx.strokeText(txt, x, y)             描边文本

         ctx.measureText(txt).width     测量文本基于当前字体设置的宽度

         //绘制路径——概念上类似于PS中的钢笔工具

         ctx.beginPath()

         ctx.moveTo()

         ctx.lineTo()

         ctx.arc()

         ctx.rect()

         ctx.ellipse()

         ctx.closePath()

          -----------------------------

         ctx.stroke()                                基于现有路径进行描边

         ctx.fill()                                       基于现有路径进行填充

         ctx.clip()                                     基于现有路径进行裁切

         //绘制图像

         ctx.drawImage(img, x, y)         绘制图像(原始尺寸)

         ctx.drawImage(img, x, y, w, h) 绘制图像(指定尺寸)

         //绘图上下文变形和状态保持

         ctx.rotate()                                 图像旋转

         ctx.translate()                            图像平移

         ctx.scale()                                   图像缩放

          ------------------

         ctx.save()                                    绘图上下文的保存

         ctx.restore()                               绘图上下文的恢复

   2.Chart.js —— 了解

      简单且灵活的JS图表绘制工具库，基于Canvas实现。类似于的工具还有ECharts、FreeChart、FusionCharts.....

      官网：http://www.chartjs.org/

      基本使用方法：

         <canvas id="c3"></canvas>

         <script src="js/Chart.js"></script>

         <script>

              new Chart(c13, {

                  type: 'bar/line/pie',

                   data: {

                        labels: ['','','',''],

                        datasets: [{

                                        label: '',

                                        data: [...]

                               } ]

                   }

               });

         </script>
```

（五）SVG绘图         

```
       Scalable Vector Graphic，可缩放向量图

       在H5标准之前的使用方法：SVG标签不能直接书写在网页中，只能编写在独立的XML文档中；

       网页中使用<img src="x.svg">进行嵌入

       纳入H5标准后的使用方法：SVG标签可以直接书写在网页中。
```

```
		Canvas与SVG的不同：

		(1)Canvas是位图；SVG是矢量图

		(2)Canvas是JS绘图技术(不是DOM元素)；SVG是标签绘图技术(是DOM元素)

		(3)Canvas内容不能使用CSS；SVG内容可以使用CSS；

		(4) Canvas内容不方便绑定事件处理；SVG内容方便进行事件绑定
		
	           常用的SVG图形：

       (1)矩形

          <rect width="100" height="50" x="400" y="350" fill="#f0f" fill-opacity="0.3" stroke="#00f" stroke-width="6" stroke-opacity=".3"></rect>

       (2)圆形

      <circle r="100" cx="400" cy="300" fill="#f0f" fill-opacity="0.4" stroke="#00f" stroke-width="6" stroke-opacity=".4"></circle>

       (3)椭圆

    <ellipse rx="100" ry="50" cx="400" cy="350" fill="#f0f" fill-opacity=".4" stroke="#00f" stroke-width="6" stroke-opacity=".4"></ellipse>        

       (4)直线（没有fill只有stroke）

             <line x1="45" y1="350" x2="450" y2="350" stroke="#f00" stroke-width="4px" stroke-opacity=".4"></line>

       (5)折线（fill必须设置透明/stroke必须手工指定）

   <polyline points="150,200  250,100  350,300  450,50" stroke="#00f" stroke-width="6" stroke-opacity=".4" fill="transparent"></polyline>

       (6)多边形

     <polygon points="100,150 100,300  400,300  400,150  250,220" fill="#f0f" fill-opacity=".4" stroke="#00f" stroke-width="6" stroke-opacity=".4"></polygon>

       (7)文本

           <text alignment-baseline="before-edge" font-size="40" fill="#f0f" stroke="#00f">达内科技2018ajgy</text>

       (8)图像

           <image xlink:href="img/p3.png" x="400" y="200" width="100" height="200"></image>

       扩展小知识：

       (1)使用滤镜（高斯模糊）

         参考MDN手册：https://developer.mozilla.org/zh-CN/docs/Web/SVG/Element/filter

              声明滤镜：

           <filter id="f2">

             <feGaussianBlur stdDeviation="3"></feGaussianBlur>

           </filter>

              使用滤镜：

               <image/text/rect  filter="url(#f2)">

      (2)使用颜色渐变对象

              声明渐变对象：

               <linearGradient id="g2" x1="0" y1="0" x2="100%" y2="0">

               <stop offset="0" stop-color="red"></stop>

               <stop offset="0.5" stop-color="yellow"></stop>

               <stop offset="1" stop-color="green"></stop>

               </linearGradient>

              使用渐变对象：

              <text/rect fill="url(#g2)" stroke="url(#g2)">
```

（六）地理定位 —— 了解

```
       通过浏览器获取当前用户的所在地理坐标，以实现“LBS服务”（Location Based Service），如实时导航、周边推荐。

       情形1：用户使用手机浏览器——可以根据内置GPS芯片读取数据

       情形2：用户使用PC浏览器——可以根据电脑的IP地址进行反向查询(需要很大的IP分配库)

                window.navigator.geolocation : {

                         watchPosition(){},

                         clearWatch(){},

                         getCurrentPosition(function(pos){

                                 '定位成功'

                                 定位时间：pos.timestamp

                                 维度：pos.coords.latitude

                                 经度：pos.coords.longitude

                                 海拔：pos.coords.altitude

                                 速度：pos.coods.speed

                         }, function(err){

                                 '定位失败'

                         }){},

                }
```

（七）拖放API       

```
       H5之前没有拖放API，可以使用“鼠标按下 + 鼠标移动”两个事件来模拟用户拖动事件。

       H5之后专门提供了七个鼠标拖动相关事件句柄：

         拖动的源对象(source)可能触发的事件：

                dragstart：拖动开始

                drag：拖动中

                dragend：拖动结束

         拖动的目标对象(target)可能触发的事件：

                dragenter：拖动进入

                dragover：拖动悬停

                drop：松手释放

                dragleave：拖动离开

       注意：拖放API事件句柄中所有的事件对象都有一个dataTransfer属性（数据运输对象），用于在源对象和目标对象间传递数据。

       源对象：event.dataTransfer.setData(key, value)

       目标对象：var value = event.dataTransfer.getData(key)
```

（八） WebWorker       

```
       背景：Chrome浏览器中发起资源请求的有6个线程；但是只有1个线程负责渲染页面——称为UI主线程——浏览器中所有的代码只能由一个线程来执行。

       问题：若浏览器加载了一个很耗时的JS文件(可能影响DOM树结构)，浏览器必须等待该文件执行完成才会继续执行后续的代码(HTML/CSS/JS等)——如果一个JS文件要执行10s(可能有很深的循环/递归等科学计算/解密)，会发生什么？——执行耗时JS任务过程中，会暂停页面中一切内容的渲染以及事件的处理。

       解决方案：H5新特性——Web Worker

       Worker的本质：就是一个执行指定任务的独立线程；且该线程可以与UI主线程进行消息数据传递。使用方法：

       HTML文件中：

                var w = new Worker('js/x.js')

                w.postMessage('发送给Worker线程的消息');

                w.onmessage = function(e){

                         e.data; //来自Worker线程的消息

                }

       JS文件中：

                onmessage = function(e){

                         var data = e.data;  //接收UI线程的消息

                         //执行耗时任务....

                         postMessage(result);   //给UI线程发送消息

                }

       注意：Worker任务不允许直接操作DOM树，也不允许使用任何的BOM对象！需要的数据只能由UI主线程来传递，处理的结果也必须交由UI线程来显示。
```

（九） WebStorage   

```
localStorage:本地缓存，持久的保持数据在客户端。
sessionStorage:会话缓存，随着浏览器的关闭而清空。
Web项目存储数据常用的方案：

         (1)服务器端存储

                1)数据库存储，如商品、用户等核心数据

                2)Session/内存存储，如用户的登录信息

         (2)客户端存储

                3)Cookie存储，如用户偏好、访问历史，浏览器兼容性好但处理麻烦且容量限制

                4)H5 WebStorage存储，如用户偏好、访问历史等安全要求的数据，老IE不兼容但易使用且容量大

         H5WebStorage存储具体涉及到两个对象：

                    (1)window.sessionStorage：类数组对象，通过key=>value对存储字符串数据——会话级存储

                           添加数据：sessionStorage['key'] = 'value'

                          修改数据：sessionStorage['key'] = 'newValue'

                           删除数据：delete sessionStorage['key']

                           获得数据：var  v = sessionStorage['key']

                    (2)window.localStorage：类数组对象，通过key=>value对存储字符串数据——本地/跨会话级/永久存储

                           添加数据：localStorage['key'] = 'value'

                           修改数据：localStorage['key'] = 'newValue'

                           删除数据：delete localStorage['key']

                           获得数据：var  v = localStorage['key']
```

（十）WebSocket

```js
WebSocket 是 HTML5 开始提供的一种在单个 TCP 连接上进行全双工通讯的协议。
WebSocket 使得客户端和服务器之间的数据交换变得更加简单，允许服务端主动向客户端推送数据。在 WebSocket API 中，浏览器和服务器只需要完成一次握手，两者之间就直接可以创建持久性的连接，并进行双向数据传输。
在 WebSocket API 中，浏览器和服务器只需要做一个握手的动作，然后，浏览器和服务器之间就形成了一条快速通道。两者之间就直接可以数据互相传送。
现在，很多网站为了实现推送技术，所用的技术都是 Ajax 轮询。轮询是在特定的的时间间隔（如每1秒），由浏览器对服务器发出HTTP请求，然后由服务器返回最新的数据给客户端的浏览器。这种传统的模式带来很明显的缺点，即浏览器需要不断的向服务器发出请求，然而HTTP请求可能包含较长的头部，其中真正有效的数据可能只是很小的一部分，显然这样会浪费很多的带宽等资源。
HTML5 定义的 WebSocket 协议，能更好的节省服务器资源和带宽，并且能够更实时地进行通讯。
```





##### 60 你如何理解HTML结构的语意化?

- 1、去掉或样式丢失的时候能让页面呈现清晰的结构。
- 2、屏幕阅读器（如果访客有视障）会完全根据你的标记来"读"你的网页。
- 3、PDA、手机等设备可能无法像普通电脑的浏览器一样来渲染网页（通常是因为这些设备对CSS的支持较弱）。
- 4、搜索引擎的爬虫也依赖于标记来确定上下文和各个关键字的权重。
- 5、你的页面是否对爬虫容易理解非常重要,因为爬虫很大程度上会忽略用于表现的标记，而只注重语义标记。
- 6、便于团队开发和维护。

##### 61 Doctype文档声明的严格模式和混杂模式，如何触发这两种模式，区分它们有何意义? 

1、如何触发两种模式

加入xml头部声明，可以触发IE浏览器的Quirks mode，触发之后，浏览器解析方式就和IE5.5一样，拥有IE5.5一样的bug和其他问题，行为（Javascript）也是如此。 

2、IE6的触发：在XHTML的DOCTYPE前加入XML声明

```
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

3、IE7的触发：在XML声明和XHTML的DOCTYPE之间，加入HTML注释

```
<?xml version="1.0" encoding="utf-8"?>
<!-- ... and keep IE7 in quirks mode -->
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

4、IE6和IE7都可以触发的：在HTML4.01的DOCTYPE文档头部，加入HTML注释

```
<!-- quirks mode -->  <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```

5、在页面顶部加 ` <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"> `，将触发"怪异模式"

6、没有使用DTD声明或者使用HTML4以下（不包括HTML4）的DTD声明时，基本上所有的浏览器都是使用quirks mode呈现









#####  62 html元素的id跟class什么区别

id和class是网页中两个通用属性，他们协同工作使整个页面丰富多彩，当我们为一个元素定义样式时，二者都可用，但有区别？

- 1、在css样式表中书写时，id选择符前缀应加"#"，class选择符前缀应加"."
- 2、id属性在一个页面中书写时只能使用一次，而class可以反复使用
- 3、id作为元素标签用于区分不同结构和内容，而class作为一个样式，可以应用到任何结构和内容当中去
- 4、布局上的一般原则：id先确定结构和内容再为它定义样式。而class正好相反，是先定义样式，然后在页面中根据不同需求把样式应用到不同结构和内容上
- 5、目前浏览器都允许同一个页面出现多个相同属性值的id，一般情况能正常显示，不过当javascript通过id来控制元素时就会出错
- 6、在实际应用中，class常被用到文字版块和页面修饰上，而id多被用在宏伟布局和设计包含块，或包含框的样式。

















##### 63 html5 离线存储

Html5的一个重要特性就是离线存储，所谓的离线存储就是将一些资源文件保存在本地，这样后续的页面重新加载将使用本地资源文件，在离线情况下可以继续访问web应用，同时通过一定的手法（更新相关文件或者使用相关API），可以更新、删除离线存储等操作。 

Html5的离线存储使用一个manifest文件来标明哪些文件是需要被存储的，使用如 `<html manifest='offline.manifest'>` 来引入一个manifest文件，这个文件的路径可以是相对的，也可以是绝对的，如果你的web应用很多，而且希望能集中管理manifest文件，那么静态文件服务器是个不错的选择。



##### 64 iframe的优缺点？

1、缺点：

在网页中使用框架结构最大的弊病是搜索引擎的"蜘蛛"程序无法解读这种页面。当"蜘蛛"程序遇到由数个框架组成的网页时，它们只看到框架而无法找到链 接，因此它们会以为该网站是个死站点，并且很快转身离去。对一个网站来说这无异于一场灾难。如果你想销售产品，你需要客户;如想得到客户，你首先要让人们 访问你的网站，而要做到这一点，你就非求助于搜索引擎不可。你花费了大量的时间、精力和金钱开设了一家网上商店，却又故意不让搜索引擎检索你，这就好象开 家零售商店，却将窗户全部漆成黑色，而且还不挂任何招牌一样。 

2、优点：

从上文中我们可以发现，使用ifame框架的弊端是无法被搜索引擎所爬行抓取。但凡事总是具有两面性。它的这个缺点也可能是他的优点。利用这一点那我 们就可以把我们站点上一些需要给我们的用户查看，但是不需要搜索引擎爬行的内容用ifame框架进行显示，这样就可以让ifram发挥真正的效果了，而且 有我们站点中的代码也可以得到很大的精简，举一个例子，就如笔者上文提到的添加微博直播信息，这些微博信息我们并不需要提供给搜索引擎，而我们需要提供的 是与访客的一个互动的体验，如下图所示，而如果我们使用ifame框架嵌入微博的信息，不仅可以简便的添加站点的微博直播平台，同时我们看到代码也十分的 精简。 

iframe好在能够把原先的网页全部原封不动显示下来,但是如果用在首页,是搜索引擎最套讨厌的.那么你的网站即使做的在好,也排不到好的名次!如 果是动态网页，用include还好点！但是必须要去除他 的<html><head><title><body>标签！ 