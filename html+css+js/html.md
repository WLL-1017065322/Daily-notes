引用MDN：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element



## 根元素：<html>

## **文档元数据**:

元数据（Metadata）含有页面的相关信息，包括样式、脚本及数据，能帮助一些软件（例如 [搜索引擎](https://developer.mozilla.org/en-US/docs/Glossary/search_engine)、[浏览器](https://developer.mozilla.org/en-US/docs/Glossary/Browser) 等等）更好地运用和渲染页面。对于样式和脚本的元数据，可以直接在网页里定义，也可以链接到包含相关信息的外部文件。

+base:html base元素指定用于一个文档中包含的所有相对的URL的基本URL。一份中只能有一个base元素

+head：html head元素 规定文档的相关的配置信息（元数据），包括文档的标题，引用的文档样式和脚本等

+link  html中的link元素规定了外部资源与当前文档的关系。这个元素可用来为导航定义一个关系框架。 这个元素常用于链接**样式表**

+meta:**HTML <meta> 元素**表示那些不能由其它HTML元相关元素 ([base link script style title 之一表示的任何元数据信息.

+style:**HTML的<style>元素**包含文档的样式信息或者文档的部分内容。默认情况下，该标签的样式信息通常是css的格式。

+title:**HTML <title> 元素** 定义文档的标题，显示在浏览器的标题栏或标签页上。它只可以包含文本，若是包含有标签，则包含的任何标签都不会被解释。

## 分区根元素：

body：**HTML body 元素**表示文档的内容。[`document.body属性提供了可以轻松访问文档的 body 元素的脚本。

## 内容分区：

内容分区元素允许你将文档内容从逻辑上进行组织划分。使用包括页眉(header)、页脚(footer)、导航(nav)和标题(h1~h6)等分区元素，来为页面内容创建明确的大纲，以便区分各个章节的内容。

address：*HTML* `的`*<address>*元素可以让作者为它最近的[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article)或者[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body)祖先元素提供联系信息。在后一种情况下，它应用于整个文档。

article：`<article>`元素表示文档、页面、应用或网站中的独立结构，其意在成为可独立分配的或可复用的结构，如在发布中，它可能是论坛帖子、杂志或新闻文章、博客、用户提交的评论、交互式组件，或者其他独立的内容项目。

aside:*<aside>* 元素表示一个和其余页面内容几乎无关的部分，被认为是独立于该内容的一部分并且可以被单独的拆分出来而不会使整体受影响。其通常表现为侧边栏或者嵌入内容。他们通常包含在工具条，例如来自词汇表的定义。也可能有其他类型的信息，例如相关的广告、笔者的传记、web 应用程序、个人资料信息，或在博客上的相关链接。

footer:**HTML <footer> 元素**表示最近一个[章节内容](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Sections_and_Outlines_of_an_HTML5_document#Defining_Sections_in_HTML5)或者[根节点](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Sections_and_Outlines_of_an_HTML5_document#Sectioning_root)（sectioning root ）元素的页脚。一个页脚通常包含该章节作者、版权数据或者与文档相关的链接等信息。

header:**HTML <header> 元素**用于展示介绍性内容，通常包含一组介绍性的或是辅助导航的实用元素。它可能包含一些标题元素，但也可能包含其他元素，比如 Logo、搜索框、作者名称，等等。

h1,h2,h3,h4,h5,h6:**HTML <h1>–<h6> 标题(Heading)元素**呈现了六个不同的级别的标题，`<h1>` 级别最高，而 `<h6>` 级别最低。一个标题元素能简要描述该节的主题。标题信息可以由用户代理可以使用，例如，自动构造某个文档中的内容表（就像本文档右边浮动栏一样）。

hgroup:**HTML <hgroup> Element** (*HTML Headings Group Element*) 代表一个段的标题。它规定了在文档轮廓里（[the outline of the document](https://developer.mozilla.org/en-US/docs/Sections_and_Outlines_of_an_HTML5_document) ）的单一标题是它所属的隐式或显式部分的标题。

main:HTML **<main>元素**呈现了文档[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body)或应用的主体部分。主体部分由与文档直接相关，或者扩展于文档的中心主题、应用的主要功能部分的内容组成。这部分内容在文档中应当是独一无二的，不包含任何在一系列文档中重复的内容，比如侧边栏，导航栏链接，版权信息，网站logo，搜索框（除非搜索框作为文档的主要功能）。



nav:*HTML导航栏* (`<nav>`) 描绘一个含有多个超链接的区域，这个区域包含转到其他页面，或者页面内部其他部分的链接列表.



section:*HTML Section 元素* (`<section>`) 表示文档中的一个区域（或节），比如，内容中的一个专题组，一般来说会有包含一个标题（heading）。一般通过是否包含一个标题 ([``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h1)-[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h6) element) 作为子节点 来 辨识每一个<section>。



##文档内容：

```jvascript
使用 HTML 文本内容元素来组织在开标签 <body> 和闭标签 </body> 里的块或章节的内容。这些元素能标识内容的宗旨或结构，而这对于 accessibility 和 SEO 很重要。

```

blockqouote:**HTML <blockquote> 元素**（或者 HTML 块级引用元素），代表其中的文字是引用内容。通常在渲染时，这部分的内容会有一定的缩进（[注](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/blockquote#Notes) 中说明了如何更改）。若引文来源于网络，则可以将原内容的出处 URL 地址设置到 cite 特性上，若要以文本的形式告知读者引文的出处时，可以通过 cite 元素。



dd：**HTML <dd> 元素**（*HTML 描述元素*）用来指明一个描述列表  dl 元素中一个术语的描述。这个元素只能作为描述列表元素的子元素出现，并且必须跟着一个dt元素。



dir：*HTML 目录元素* (`<dir>`) 表示一个目录，也就是文件名称的集合。



div: HTML <div> 元素 (或 HTML 文档分区元素) 是一个通用型的流内容容器，它在语义上不代表任何特定类型的内容，它可以被用来对其它元素进行分组，一般用于样式化相关的需求（使用 class 或 id 特性) 或者对具有相同特性的一组元素进行分组 (比如 lang)，它应该在没有任何其它语义元素可用时才使用 (比如 <article> 或 <nav>) 。



dl:HTML <dl> 元素 （或 HTML 描述列表元素）是一个包含术语定义以及描述的列表，通常用于展示词汇表或者元数据 (键-值对列表)。



dt:HTML <dt> 元素 （或 HTML 术语定义元素）用于在一个定义列表中声明一个术语。该元素仅能作为 <dl> 的子元素出现。通常在该元素后面会跟着 <dd> 元素， 然而，多个连续出现的 <dt> 元素都将由出现在它们后面的第一个 <dd> 元素定义。



figcaption:HTML <figcaption> 元素 是与其相关联的图片的说明/标题，用?于描述其父节点 <figure> 元素里的其他数据。这意味着 <figcaption> 在<figure> 块里是第一个或最后一个。同时 HTML Figcaption 元素是可选的；如果没有该元素，这个父节点的图片只是会没有说明/标题。



figure :HTML <figure> 元素代表一段独立的内容, 经常与说明(caption) <figcaption> 配合使用, 并且作为一个独立的引用单元。当它属于主体(main flow)



hr :HTML <hr> 元素表示段落级元素之间的主题转换（例如，一个故事中的场景的改变，或一个章节的主题的改变）。在HTML的早期版本中，它是一个水平线。现在它仍能在可视化浏览器中表现为水平线，但目前被定义为语义上的，而不是表现层面上。



li:HTML <li> 元素 (或者 HTML 列表条目元素) 用于表示列表里的条目。它必须被包含在一个父元素里：一个有顺序的列表(<ol>)，一个无顺序的列表(<ul>)，或者一个菜单 (<menu>)。在菜单或者无顺序的列表里，列表条目通常用点排列显示。在有顺序的列表里，列表条目通常是在左边有按升序排列计数的显示，例如数字或者字母。



main: HTML <main>元素呈现了文档<body>或应用的主体部分。主体部分由与文档直接相关，或者扩展于文档的中心主题、应用的主要功能部分的内容组成。这部分内容在文档中应当是独一无二的，不包含任何在一系列文档中重复的内容，比如侧边栏，导航栏链接，版权信息，网站logo，搜索框（除非搜索框作为文档的主要功能）。



ol : HTML <ol> 元素 表示多个有序列表项，通常渲染为有带编号的列表。

p:HTML <p>元素（或者说 HTML 段落元素）表示文本的一个段落。该元素通常表现为一整块与相邻文本分离的文本，或以垂直的空白隔离或以首行缩进。另外，<p> 是块级元素。





pre:HTML <pre> 元素表示预定义格式文本。在该元素中的文本通常按照原文件中的编排，以等宽字体的形式展现出来，文本中的空白符（比如空格和换行符）都会显示出来。(紧跟在 <pre> 开始标签后的换行符也会被省略)



ul:The HTML <ul> 元素 ( 或 HTML 无序列表元素） 代表多项的无序列表，即无数值排序项的集合，且它们在列表中的顺序是没有意义的。通常情况下，无序列表项的头部可以是几种形式，如一个点，一个圆形或方形。头部的风格并不是在页面的HTML描述定义, 但在其相关的CSS 可以用 list-style-type 属性。



## 内联文本语义

使用 HTML 内联文本语义（Inline text semantics）定义一个单词、一行内容，或任意文字的语义、结构或样式。



a:HTML <a> 元素（或称锚元素）可以创建通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接。



abbr:HTML 缩写元素（<abbr>）用于展示缩写，并且可以通过可选的 title 属性提供完整的描述。



b:HTML提醒注意（Bring Attention To）元素（<b>）用于吸引读者的注意到该元素的内容上（如果没有另加特别强调）。这个元素过去被认为是粗体（Boldface）元素，并且大多数浏览器仍然将文字显示为粗体。尽管如此，你不应将 <b> 元素用于显示粗体文字；替代方案是使用 CSS font-weight 属性来创建粗体文字。



bdi:HTML <bdi> 元素 (双向隔离元素) 会隔离可能以不同方向进行格式化的外部文本。

bdo:<bdo> 元素 (HTML双向覆盖元素)用于覆盖当前文本的朝向，它使得字符按给定的方向排列。



br:HTML <br>元素在文本中生成一个换行（回车）符号。此元素在写诗和地址时很有用，这些地方的换行都非常重要。



cite:HTML引用（ Citation）标签 (<cite>) 表示一个作品的引用。它必须包含引用作品的符合简写格式的标题或者URL，它可能是一个根据添加引用元数据的约定的简写形式。



code:**HTML <code> 元素**呈现一段计算机代码. 默认情况下, 它以浏览器的默认等宽字体显示.

data:HTML <data> 元素 将一个指定内容和机器可读的翻译联系在一起。但如果内容是与 time 或者 date 相关的，一定要使用 <time>。

dfn:HTML 定义元素 (<dfn>) 表示术语的一个定义。



em:HTML 着重元素 (<em>) 标记出需要用户着重阅读的内容， <em> 元素是可以嵌套的，嵌套层次越深，则其包含的内容被认定为越需要着重阅读。



i:HTML元素 <i> 用于表现因某些原因需要区分普通文本的一系列文本。例如技术术语、外文短语或是小说中人物的思想活动等，它的内容通常以斜体显示。



kbd:HTML键盘输入元素(**<kbd>**) 用于表示用户输入，它将产生一个行内元素，以浏览器的默认monospace字体显示。



mark:这个 HTML mark 标签代表突出显示的文字,例如可以为了标记特定上下文中的文本而使用这个标签. 举个例子，它可以用来显示搜索引擎搜索后关键词。



q:HTML引用标签 (<q>)表示一个封闭的并且是短的行内引用的文本. 这个标签是用来引用短的文本，所以请不要引入换行符; 对于长的文本的引用请使用 <blockquote> 替代.



rp:HTML <rp> 元素用于为那些不能使用 <ruby> 元素展示 ruby 注解的浏览器，提供随后的圆括号。



rt:HTML Ruby 文本 (<rt>) 元素包含字符的发音，字符在 ruby 注解中出现，它用于描述东亚字符的发音。这个元素始终在 <ruby> 元素中使用。



rtc:HTML <rtc> 元素包含文字的语义注解，它们在 <rb> 元素中展示。<rb> 元素可以拥有发音 (<rt>) 和语义(<rtc>) 注解。



ruby:HTML <ruby> 元素 被用来展示东亚文字注音或字符注释。



s:HTML <s> 元素 使用删除线来渲染文本。使用 <s> 元素来表示不再相关，或者不再准确的事情。但是当表示文档编辑时，不提倡使用 <s> ；为此，提倡使用 <del> 和 <ins> 元素。



samp:<samp> 元素用于标识计算机程序输出，通常使用浏览器缺省的 monotype 字体（例如 Lucida Console）。



small:HTML 中的元素將使文本的字体变小一号。(例如从大变成中等，从中等变成小，从小变成超小)。在HTML5中，除了它的样式含义，这个元素被重新定义为表示边注释和附属细则，包括版权和法律文本。



span;HTML <span> 元素是短语内容的通用行内容器，并没有任何特殊语义。可以使用它来编组元素以达到某种样式意图（通过使用类或者Id属性），或者这些元素有着共同的属性，比如lang。应该在没有其他合适的语义元素时才使用它。<span> 与 <div> 元素很相似，但 <div> 是一个 块元素 而 <span> 则是 行内元素 .



strong:Strong 元素 (<strong>)表示文本十分重要，一般用粗体显示。



sub:HTML <sub> 元素定义了一个文本区域，出于排版的原因，与主要的文本相比，应该展示得更低并且更小。

sup:HTML <sup> 元素定义了一个文本区域，出于排版的原因，与主要的文本相比，应该展示得更高并且更小。



time:HTML time 标签(<time>) 用来表示24小时制时间或者公历日期，若表示日期则也可包含时间和时区。



tt:HTML 电报文本元素 (<tt>) 产生一个内联元素，使用浏览器内置的 monotype 字体展示。这个元素用于给文本排版，使其等宽展示，就像电报那样。使用 <code> 元素来展示等宽文本可能更加普遍。



u:HTML <u> 元素使文本在其内容的基线下的一行呈现下划线。在HTML5中, 此元素表示具有未标注的文本跨度，显示渲染，非文本注释，例如将文本标记为中文文本中的专有名称(一个正确的中文标记), 或 将文本标记为拼写错误。



var:<var> 标签表示变量的名称，或者由用户提供的值。



wbr：HTML <wbr>元素  — 一个文本中的位置，其中浏览器可以选择来换行，虽然它的换行规则可能不会在这里换行。



## 图片和多媒体

HTML 支持各种多媒体资源，例如图像，音频和视频。

area:HTML <area> 元素 在图片上定义一个热点区域，可以关联一个超链接。<area>元素仅在<map>元素内部使用。



audio:HTML <audio> 元素用于在文档中表示音频内容。 <audio> 元素可以包含多个音频资源， 这些音频资源可以使用 src 属性或者<source> 元素来进行描述； 浏览器将会选择最合适的一个来使用。对于不支持<audio>元素的浏览器，<audio>元素也可以作为浏览器不识别的内容加入到文档中。



img:HTML Image 元素（ <img> ）代表文档中的一个图像。



map:HTML <map> 属性 与 <area> 属性一起使用来定义一个图像映射(一个可点击的链接区域).



track:HTML <track> 元素 被当作媒体元素—<audio> 和 <video>的子元素来使用。它允许指定计时字幕（或者基于事件的数据），例如自动处理字幕。



video；HTML <video> 元素 用于在HTML或者XHTML文档中嵌入视频内容。



##内嵌内容

除了常规的多媒体内容，HTML 可以包括各种其他的内容，即使它并不容易交互。



applet:HTML中的Applet元素(<applet>) 标志着包含了Java的applet。



embed；HTML <embed> 元素将外部内容嵌入文档中的指定位置。此内容由外部应用程序或其他交互式内容源（如浏览器插件）提供。



iframe:HTML内联框架元素 <iframe> 表示嵌套的浏览上下文，有效地将另一个HTML页面嵌入到当前页面中。



noembed:<noembed> 元素是个废除的和不标准的方式，用于向不支持 <embed> ，或者不支持作者希望的 嵌入式内容 的浏览器提供替代（或者“后备”）内容。这个元素在 HTML 4.01 起废除，以支持后备



object:HTML <object> 元素（或者称作 HTML 嵌入对象元素）表示引入一个外部资源，这个资源可能是一张图片，一个嵌入的浏览上下文，亦或是一个插件所使用的资源。



param:HTML <param>元素为<object>元素定义参数



picture:HTML <picture> 元素是一个容器，用来为其内部特定的 <img> 元素提供多样的 <source> 元素。浏览器会根据当前页面（即图片所在的盒子的容器）的布局以及当前浏览的设备（比如普通的屏幕和高清屏幕）去从中选择最合适的资源。



source；HTML <source> 元素为 <picture>, <audio> 或者 <video> 元素指定多个媒体资源。这是一个空元素。它通常用于以不同浏览器支持的多种格式提供相同的媒体内容。 It is commonly used to serve the same media content in multiple formats supported by different browsers.



## 脚本

为了创建动态内容和 Web 应用程序，HTML 支持使用脚本语言，最突出的就是 JavaScript。某些元素支持此功能。

canvas:**<canvas>元素**可被用来通过脚本（通常是JavaScript）绘制图形。比如,它可以被用来绘制图形,制作图片集合,甚至用来实现动画效果。你可以(也应该)在元素标签内写入可提供替代的的代码内容，这些内容将会在在旧的、不支持<canvas>元素的浏览器或是禁用了JavaScript的浏览器内渲染并展现。

noscript:如果页面上的脚本类型不受支持或者当前在浏览器中关闭了脚本，则在HTML <noscript> 元素中定义脚本未被执行时的替代内容。</noscript>



script:HTML <script> 元素用于嵌入或引用可执行脚本。



## 编辑标识

这些元素能表示出某个文本被更改的部分

del:HTML的<del>标签表示一些被从文档中删除的文字内容。比如可以在需要显示修改记录或者源代码差异的情况使用这个标签。<ins>标签的作用恰恰于此相反：表示文档中添加的内容。

ins;HTML <ins> 元素定义已经被插入文档中的文本。



##表格内容：

这里的元素用于创建和处理表格数据

元素在一个元素中可以出现一个或者更多

caption:HTML <caption> 元素 (or HTML 表格标题元素) 展示一个表格的标题， 它常常作为 <table> 的第一个子元素出现，同时显示在表格内容的最前面，但是，它同样可以被CSS样式化，所以，它同样可以出现在任何一个一个相对于表格的做任意位置。



col:**HTML <col> 元素** 定义表格中的列，并用于定义所有公共单元格上的公共语义。它通常位于元素内。



colgroup:HTML 中的 表格列组（Column Group <colgroup>） 标签用来定义表中的一组列表。



table:**HTML**的 **table** 元素表示表格数据 — 即通过二维数据表表示的信息。



tbody:这个 HTML 标签 



td:The Table cell HTML element (<td>) defines a cell of a table that contains data. It participates in the table model.



tfoot:HTML 元素<tfoot>  定义了一组表格中各列的汇总行。



th:HTML <th> 元素 scope and headers 属性



thead:HTML的<thead>元素定义了一组定义表格的列头的行。



tr；HTML <tr> 元素定义表格中的行。 Those can be a mix of <td> and <th> elements.



## 表单

HTML 提供了许多可一起使用的元素，这些元素能用来创建一个用户可以填写并提交到网站或应用程序的表单。详情请参阅 HTML forms guide。

button:HTML <button> 元素表示一个可点击的按钮，可以用在表单或文档其它需要使用简单标准按钮的地方。

datalist:

fieldset:

form:HTML <form> 元素 表示了文档中的一个区域，这个区域包含有交互控制元件，用来向web服务器提交信息。



#### input；

HTML <input> 元素用于为基于Web的表单创建交互式控件，以便接受来自用户的数据; 可以使用各种类型的输入数据和控件小部件，具体取决于设备和user agent。

| [accept](http://www.runoob.com/tags/att-input-accept.html)   | audio/*  video/*  image/* *MIME_type*                        | 规定通过文件上传来提交的文件的类型。 (只针对type="file")     |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [align](http://www.runoob.com/tags/att-input-align.html)     | left  right  top  middle  bottom                             | HTML5已废弃，不赞成使用。规定图像输入的对齐方式。 (只针对type="image") |
| [alt](http://www.runoob.com/tags/att-input-alt.html)         | *text*                                                       | 定义图像输入的替代文本。 (只针对type="image")                |
| [autocomplete](http://www.runoob.com/tags/att-input-autocomplete.html)**New** | on  off                                                      | autocomplete 属性规定 <input> 元素输入字段是否应该启用自动完成功能。 |
| [autofocus](http://www.runoob.com/tags/att-input-autofocus.html)**New** | autofocus                                                    | 属性规定当页面加载时 <input>  元素应该自动获得焦点。         |
| [checked](http://www.runoob.com/tags/att-input-checked.html) | checked                                                      | checked 属性规定在页面加载时应该被预先选定的  <input> 元素。 (只针对 type="checkbox" 或者 type="radio") |
| [disabled](http://www.runoob.com/tags/att-input-disabled.html) | disabled                                                     | disabled 属性规定应该禁用的 <input> 元素。                   |
| [form](http://www.runoob.com/tags/att-input-form.html)**New** | *form_id*                                                    | form 属性规定 <input> 元素所属的一个或多个表单。             |
| [formaction](http://www.runoob.com/tags/att-input-formaction.html)**New** | *URL*                                                        | 属性规定当表单提交时处理输入控件的文件的 URL。(只针对 type="submit" 和 type="image") |
| [formenctype](http://www.runoob.com/tags/att-input-formenctype.html)**New** | application/x-www-form-urlencoded  multipart/form-data  text/plain | 属性规定当表单数据提交到服务器时如何编码(只适合 type="submit" 和 type="image")。 |
| [formmethod](http://www.runoob.com/tags/att-input-formmethod.html)**New** | get post                                                     | 定义发送表单数据到 action URL 的 HTTP 方法。 (只适合 type="submit" 和 type="image") |
| [formnovalidate](http://www.runoob.com/tags/att-input-formnovalidate.html)**New** | formnovalidate                                               | formnovalidate 属性覆盖 <form> 元素的 novalidate 属性。      |
| [formtarget](http://www.runoob.com/tags/att-input-formtarget.html)**New** | _blank  _self  _parent  _top *framename*                     | 规定表示提交表单后在哪里显示接收到响应的名称或关键词。(只适合 type="submit" 和 type="image") |
| [height](http://www.runoob.com/tags/att-input-height.html)**New** | *pixels*                                                     | 规定  <input>元素的高度。(只针对type="image")                |
| [list](http://www.runoob.com/tags/att-input-list.html)**New** | *datalist_id*                                                | 属性引用  <datalist> 元素，其中包含 <input> 元素的预定义选项。 |
| [max](http://www.runoob.com/tags/att-input-max.html)**New**  | *number  date*                                               | 属性规定 <input> 元素的最大值。                              |
| [maxlength](http://www.runoob.com/tags/att-input-maxlength.html) | *number*                                                     | 属性规定 <input> 元素中允许的最大字符数。                    |
| [min](http://www.runoob.com/tags/att-input-min.html)**New**  | *number  date*                                               | 属性规定 <input>元素的最小值。                               |
| [multiple](http://www.runoob.com/tags/att-input-multiple.html)**New** | multiple                                                     | 属性规定允许用户输入到 <input> 元素的多个值。                |
| [name](http://www.runoob.com/tags/att-input-name.html)       | *text*                                                       | name 属性规定 <input> 元素的名称。                           |
| [pattern](http://www.runoob.com/tags/att-input-pattern.html)**New** | *regexp*                                                     | pattern 属性规定用于验证 <input> 元素的值的正则表达式。      |
| [*placeholder](http://www.runoob.com/tags/att-input-placeholder.html)**New** | *text*  ================================                     | placeholder 属性规定可描述输入 <input> 字段预期值的简短的提示信息 。 |
| [readonly](http://www.runoob.com/tags/att-input-readonly.html) | readonly                                                     | readonly 属性规定输入字段是只读的。                          |
| [required](http://www.runoob.com/tags/att-input-required.html)**New** | required                                                     | 属性规定必需在提交表单之前填写输入字段。                     |
| [size](http://www.runoob.com/tags/att-input-size.html)       | *number*                                                     | size 属性规定以字符数计的  <input> 元素的可见宽度。          |
| [src](http://www.runoob.com/tags/att-input-src.html)         | *URL*                                                        | src 属性规定显示为提交按钮的图像的 URL。 (只针对 type="image") |
| [step](http://www.runoob.com/tags/att-input-step.html)**New** | *number*                                                     | step 属性规定 <input> 元素的合法数字间隔。                   |
| [type](http://www.runoob.com/tags/att-input-type.html)       | button   checkbox   color   date   datetime   datetime-local   email   file   hidden   image   month   number   password   radio   range   reset   search   submit   tel   text   time   url   week | type 属性规定要显示的  <input> 元素的类型。                  |
| [value](http://www.runoob.com/tags/att-input-value.html)     | *text*                                                       | 指定 <input> 元素 value 的值。                               |
| [width](http://www.runoob.com/tags/att-input-width.html)**New** | *pixels*                                                     | width 属性规定  <input> 元素的宽度。  (只针对type="image")   |



label：HTML 元素表示用户界面中项目的标题。



legend;HTML的<legend>元素（也称为HTML的域说明元素（or HMTL
 Legend Field Element））代表一个用于表示它的父元素<fieldset>的内容的标题。</legend>



meter；HTML <meter>元素用来显示已知范围的标量值或者分数值。



option:在一个web表单中, **HTML元素 <optgroup>** 会创建包含在一个 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/select) 元素中的一组选项



output:HTML <output> 标签表示计算或用户操作的结果。



progress：HTML中的progress (<progress>) 元素用来显示一项任务的完成进度.虽然规范中没有规定该元素具体如何显示,浏览器开发商可以自己决定,但通常情况下,该元素都显示为一个进度条形式.



select：HTML <select> 元素表示一个控件，提供一个选项菜单：



textarea:HTML <textarea> 元素表示一个多行纯文本编辑控件。



## 交互元素

HTML 提供了一系列有助于创建交互式用户界面对象的元素。

details

dialog；HTML <dialog> 元素表示一个对话框或其他交互式组件，例如一个检查员或窗口。

menu：HTML <menu> 元素 呈现了一组用户可执行或激活的命令。这既包含了可能出现在屏幕顶端的列表菜单，也包含了那些隐藏在按钮之下、当点击按钮后显示出来的文本菜单。

menuitem

summary:HTML <summary> 元素 用作 一个<details>元素的一个内容的摘要，标题或图例。



## web组件

Web 组件是一种与 HTML 相关联（HTML-related）的技术，简单来说，它允许创建自定义元素，并如同普通的 HTML 一样使用它们。此外，你甚至可以创建经过自定义的标准 HTML 元素。

content:HTML <content> 元素— Web 组件 的技术套件的废弃部分 — 用于 Shadow DOM 内部作为 insertion point，并且不可用于任何正常的 HTML，现在已被 <slot> 元素代替，它在 DOM 中创建一个位置，Shadow DOM 会插入这里。



element:<element>元素被定义在最新的 HTML DOM 元素中。</element>



shadow:HTML <shadow> 元素 — Web 组件技术套件的废弃部分 — 目的是用作 Shadow DOM insertion point。如果你在 shadow host 下面创建了多个 shadow root，你就可能已经使用了它。在正常的 HTML 没有任何用处。



slot:HTML <slot> element—是 Web Components 技术的一部分，是自定义web组件的占位符，目的是分离创建DOM树和DOM树的表现。



template:HTML内容模板（<template>）元素是一种用于保存客户端内容机制，该内容在加载页面时不会呈现，但随后可以在运行时使用JavaScript实例化。



##过时和弃用的元素：



acronym:



applet:



basefont:



bgsound:



big:



blink:



center:



command:



content:



dir



element:



font:



frame:



frameset:



image:



isindex:



keygen:



listing



marquee:



menuitem



multicol:



nextid



nobr



noembed



noframes



plaintext



shadow



spacer



strike



tt



xmp

























