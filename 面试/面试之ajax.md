1、什么是AJAX，为什么要使用Ajax（请谈一下你对Ajax的认识）

2、为什么要用ajax：

3、AJAX最大的特点是什么。

4、请介绍一下XMLhttprequest对象。

5、AJAX技术体系的组成部分有哪些。

6、AJAX应用和传统Web应用有什么不同。

7、AJAX请求总共有多少种CALLBACK。

8.Ajax和javascript的区别。

9、在浏览器端如何得到服务器端响应的XML数据。

10、 XMLHttpRequest对象在IE和Firefox中创建方式有没有不同。

11、介绍一下XMLHttpRequest对象的常用方法和属性。

12、什么是XML

13、XML的解析方式

14、你采用的是什么框架（架包）

15、如果熟悉某种ajax框架，他可能会问到怎样在程序中使用这种框架

DWR框架介绍

16、介绍一下Prototype的$()函数，$F()函数，$A()函数都是什么作用

17、介绍一下XMLHttpRequest对象

18、AJAX的全称是什么？ 介绍一下AJAX？

19、Ajax主要包含了哪些技术？

20、AJAX都有哪些优点和缺点？

21、ajax的缺点

22  首先了解下浏览器的同源策略

23 那么怎样解决跨域问题的呢？







**1、什么是AJAX，为什么要使用Ajax（请谈一下你对Ajax的认识）**

什么是ajax：

Ajax不是一个技术，它实际上是几种技术，每种技术都有其独特这处，合在一起就成了一个功能强大的新技术

AJAX是“Asynchronous JavaScript and XML”的缩写。他是指一种创建交互式网页应用的网页开发技术。

Ajax包含下列技术：

基于web标准（standards-basedpresentation）XHTML+CSS的表示；

使用 DOM（Document ObjectModel）进行动态显示及交互；

使用 XML 和 XSLT 进行数据交换及相关操作；

使用 XMLHttpRequest 进行异步数据查询、检索；

使用 JavaScript 将所有的东西绑定在一起。



**2、为什么要用ajax：**

Ajax应用程序的优势在于：

\1. 通过异步模式，提升了用户体验

\2. 优化了浏览器和服务器之间的传输，减少不必要的数据往返，减少了带宽占用

\3. Ajax引擎在客户端运行，承担了一部分本来由服务器承担的工作，从而减少了大用户量下的服务器负载。

**3、AJAX最大的特点是什么。**

Ajax可以实现动态不刷新（局部刷新）

就是能在不更新整个页面的前提下维护数据。这使得Web应用程序更为迅捷地回应用户动作，并避免了在网络上发送那些没有改变过的信息。

**4、请介绍一下XMLhttprequest对象。**

Ajax的核心是JavaScript对象XmlHttpRequest。该对象在Internet Explorer 5中首次引入，它是一种支持异步请求的技术。简而言之，XmlHttpRequest使您可以使用JavaScript向服务器提出请求并处理响应，而不阻塞用户。通过XMLHttpRequest对象，Web开发人员可以在页面加载以后进行页面的局部更新。

**5、AJAX技术体系的组成部分有哪些。**

HTML，css，dom，xml，xmlHttpRequest，javascript

**6、AJAX应用和传统Web应用有什么不同。**

在传统的Javascript编程中，如果想得到服务器端数据库或文件上的信息，或者发送客户端信息到服务器，需要建立一个HTML form然后GET或者POST数据到服务器端。用户需要点击”Submit”按钮来发送或者接受数据信息，然后等待服务器响应请求，页面重新加载。

因为服务器每次都会返回一个新的页面， 所以传统的web应用有可能很慢而且用户交互不友好。

使用AJAX技术， 就可以使Javascript通过XMLHttpRequest对象直接与服务器进行交互。

通过HTTP Request， 一个web页面可以发送一个请求到web服务器并且接受web服务器返回的信息(不用重新加载页面)，展示给用户的还是通一个页面，用户感觉页面刷新，也看不到到Javascript后台进行的发送请求和接受响应。

**7、AJAX请求总共有多少种CALLBACK。**

Ajax请求总共有八种Callback

```
`onSuccess``onFailure``onUninitialized``onLoading``onLoaded``onInteractive``onComplete``onException`
```

**8.Ajax和javascript的区别。**

javascript是一种在浏览器端执行的脚本语言，Ajax是一种创建交互式网页应用的开发技术 ，它是利用了一系列相关的技术其中就包括javascript。

Javascript是由网景公司开发的一种脚本语言，它和sun公司的java语言是没有任何关系的，它们相似的名称只是一种行销策略。

在一般的web开发中，javascript是在浏览器端执行的，我们可以用javascript控制浏览器的行为和内容。

在 Ajax应用中信息是如何在浏览器和服务器之间传递的

通过XML数据或者字符串

**9、在浏览器端如何得到服务器端响应的XML数据。**

XMLHttpRequest对象的responseXMl属性

**10、 XMLHttpRequest对象在IE和Firefox中创建方式有没有不同。**

有，IE中通过new ActiveXObject()得到，Firefox中通过newXMLHttpRequest()得到

**11、介绍一下XMLHttpRequest对象的常用方法和属性。**

open(“method”,”URL”) 建立对服务器的调用，第一个参数是HTTP请求 方式可以为GET，POST或任何服务器所支持的您想调用的方式。

第二个参数是请求页面的URL。

send()方法，发送具体请求

abort()方法，停止当前请求

readyState属性 请求的状态 有5个可取值0=未初始化 ，1=正在加载
2=以加载，3=交互中，4=完成

responseText 属性 服务器的响应，表示为一个串

reponseXML 属性 服务器的响应，表示为XML

status 服务器的HTTP状态码，200对应ok 400对应not found

**12、什么是XML**

XML是扩展标记语言，能够用一系列简单的标记描述数据

**13、XML的解析方式**

常用的用dom解析和sax解析。dom解析是一次性读取xml文件并将其构造为DOM对象供程序使用，优点是操作方便，但是比较耗内存。Sax是按事件驱动的方式解析的，占用内存少，但是编程复杂

**14、你采用的是什么框架（架包）**

这题是必问的，一般也是最开始就会问到。

在java中比较流行的有 dojo, Prototype , JQuery, Dwr, extjs 等等

**15、如果熟悉某种ajax框架，他可能会问到怎样在程序中使用这种框架**

**DWR框架介绍**

DWR(DirectWeb Remoting)是一个WEB远程调用框架.利用这个框架可以让AJAX开发变得很简单.利用DWR可以在客户端利用JavaScript直接调用服务端的Java方法并返回值给JavaScript就好像直接本地客户端调用一样(DWR根据Java类来动态生成JavaScrip代码).

DWR的实现原理是通过反射，将java翻译成javascript，然后利用回调机制，从而实现了javascript调用Java代码

**16、介绍一下Prototype的$()函数，$F()函数，$A()函数都是什么作用**

$() 方法是在DOM中使用过于频繁的document.getElementById() 方法的一个便利的简写，就像这个DOM方法一样，这个方法返回参数传入的id的那个元素。

$F()函数是另一个大收欢迎的“快捷键”，它能用于返回任何表单输入控件的值，比如textbox,drop-down list。这个方法也能用元素id或元素本身做为参数。

$A()函数能把它接收到的单个的参数转换成一个Array对象。

**17、介绍一下XMLHttpRequest对象**

通过XMLHttpRequest对象，Web开发人员可以在页面加载以后进行页面的局部更新。

AJAX开始流行始于Google在2005年使用的”Google Suggest”。

“Google Suggest”就是使用XMLHttpRequest对象来创建动态的Web接口：

当用户开始输入google的搜索框，Javascript发送用户输入的字符到服务器，然后服务器返回一个建议列表。

XMLHttpRequest对象在IE5.0+, Safari 1.2, Mozilla1.0/Firefox, Opera 8+ 和NetScapt7 开始被支持。

**18、AJAX的全称是什么？ 介绍一下AJAX？**

AJAX的全称是Asynchronous JavaScript And XML.

AJAX是2005年由Google发起并流行起来的编程方法， AJAX不是一个新的编程语言，但是它是一个使用已有标准的新的编程技术。

使用AJAX可以创建更好，更快，更用户界面友好的Web应用。

AJAX技术基于Javascript和HTTP Request.

**19、Ajax主要包含了哪些技术？**

Ajax（Asynchronous JavaScript + XML）的定义

基于web标准（standards-based presentation）XHTML+CSS的表示；

使用 DOM（Document Object Model）进行动态显示及交互；

使用 XML 和 XSLT 进行数据交换及相关操作；

使用XMLHttpRequest 进行异步数据查询、检索；
使用 JavaScript 将所有的东西绑定在一起。英文参见Ajax的提出者Jesse James Garrett的原文,原文题目(Ajax: A New Approach to

Web Applications)。

类似于DHTML或LAMP，AJAX不是指一种单一的技术，而是有机地利用了一系列相关的技术。事实上，一些基于AJAX的“派生/合成”式（derivative/composite）的技术正在出现，如“AFLAX”。

AJAX的应用使用支持以上技术的web浏览器作为运行平台。这些浏览器目前包括：Mozilla、Firefox、Internet Explorer、Opera、Konqueror及Safari。但是Opera不支持XSL格式对象，也不支持XSLT。

**20、AJAX都有哪些优点和缺点？**

1、最大的一点是页面无刷新，用户的体验非常好。

2、使用异步方式与服务器通信，具有更加迅速的响应能力。

3、可以把以前一些服务器负担的工作转嫁到客户端，利用客户端闲置的能力来处理，减轻服务器和带宽的负担，节约空间和宽带租用成本。并且减轻服务器的负担，ajax的原则是“按需取数据”，可以最大程度的减少冗余请求，和响应对服务器造成的负担。

4、基于标准化的并被广泛支持的技术，不需要下载插件或者小程序。

**21 ajax的缺点**

1、ajax不支持浏览器back按钮。

2、安全问题 AJAX暴露了与服务器交互的细节。

3、对搜索引擎的支持比较弱。

4、破坏了程序的异常机制。

5、不容易调试。





**22  首先了解下浏览器的同源策略**

   

同源策略/SOP（Same origin policy）是一种约定，由Netscape公司1995年引入浏览器，它是浏览器最核心也最基本的安全功能，如果缺少了同源策略，浏览器很容易受到XSS、CSRF等攻击。所谓同源是指"协议+域名+端口"三者相同，即便两个不同的域名指向同一个ip地址，也非同源。

  

**23 那么怎样解决跨域问题的呢？**

  

**1 通过jsonp跨域，原生实现：**

 

```
<script>
var script = document.createElement('script');
script.type = 'text/javascript';

// 传参并指定回调执行函数为onBack
script.src = 'http://www.....:8080/login?user=admin&callback=onBack';
document.head.appendChild(script);

// 回调执行函数
function onBack(res) {
    alert(JSON.stringify(res));
}
</script>
```

 

**2、document.domain + iframe 跨域**  

 

此方案仅限主域相同，子域不同的跨域应用场景。

 

1.）父窗口：(http://www.domain.com/a.html)

  

```
<iframe id="iframe" src="http://child.domain.com/b.html"></iframe>
<script>
document.domain = 'domain.com';
var user = 'admin';
</script>
```

 

2.）子窗口：(http://child.domain.com/b.html)         

```
<script>
document.domain = 'domain.com';
// 获取父窗口中变量
alert('get js data from parent ---> ' + window.parent.user);
</script>
```

弊端：请看下面渲染加载优化

3、nginx 代理跨域

4、nodejs 中间件代理跨域

5、后端在头部信息里面设置安全域名









