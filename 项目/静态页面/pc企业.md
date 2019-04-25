# fullpage.js的使用

​	fullPage.js 是一个基于 jQuery 的插件，它能够很方便、很轻松的制作出全屏网站。如今我们经常能见到全屏网站，尤其是国外网站。这些网站用几幅很大的图片或色块做背景，再添加一些简单的内容，显得格外的高端大气上档次。如果你也希望你的网站能设计成全屏的，显得更上档次，你可以试试 fullPage.js。

​	fullPage.js的主要功能有：支持鼠标滚动、支持前进后退和键盘控制、多个回调函数、支持手机、平板触摸事件、支持 CSS3 动画、支持窗口缩放、窗口缩放时自动调整、可设置滚动宽度、背景颜色、滚动速度、循环选项、回调、文本对齐方式等等

## 使用说明

## 1、引入插件文件

 

这个插件依赖于jQuery，所以你还需要下载jQuery，并且在Fullpage插件之前引入。

 

```
<link rel="stylesheet" type="text/css" href="/fullpage/jquery.fullPage.css" />
<script src="/fullpage/jquery.min.js"></script>
<script type="text/javascript" src="/fullpage/jquery.fullPage.js"></script>
```

 

如果你需要自定义页面滚动的效果，你需要引入jquery.easings.min.js文件。

 

```
<script src="/fullpage/jquery.easings.min.js"></script>
```

 

对于内容比较多的页面，可以设置右侧的滚动条，但是默认情况下无法滚动，你需要jquery.slimscroll.min.js文件来自定义滑条滚动效果。

 

```
<script type="text/javascript" src="/fullpage/jquery.slimscroll.min.js"></script>
```

 

最后，如果你不想下载到项目中，您可以使用开源项目CDN服务，Fullpage在CDNJS的地址：https://cdnjs.com/libraries/fullPage.js

 

## 2、编写HTML代码

 

默认情况下，每一屏幕的代码都需要有DIV包裹，并且设置DIV的类名为section，默认情况下，第一个setion将作为首页显示在页面上。

 

```js
<div id="fullpage'">
<div class="section">Some section</div>
<div class="section">Some section</div>
<div class="section">Some section</div>
<div class="section">Some section</div>
</div>
```

 

假如你需要让某一个section作为首页的第一屏展示，你只需要给这个section添加一个active的类，Fullpage会自动优先展示这个屏幕，例如定义下面的代码：

 

```
<div class="section active">Some section</div>
```

 

Fullpage自带左右滑动的幻灯片，只需要在section中添加DIV元素，并且给DIV元素添加slide类，FUllpage会自动生成幻灯片特效，例如下面的代码：

 

```
<div class="section">
<div class="slide"> Slide 1 </div>
<div class="slide"> Slide 2 </div>
<div class="slide"> Slide 3 </div>
<div class="slide"> Slide 4 </div>
</div>
```

 

## 3、初始化Fullpage

 

使用jQuery的文档加载完毕以后执行函数，初始化Fullpage插件。

 

```
$(document).ready(function() {
$('#fullpage').fullpage();
});
```

 

所有的选项设置更复杂的初始化可能看起来像这样：

 

```
$(document).ready(function() {
	$('#fullpage').fullpage({
		//Navigation
		menu: false,//绑定菜单，设定的相关属性与anchors的值对应后，菜单可以控制滚动，默认为false。
		anchors:['firstPage', 'secondPage'],//anchors定义锚链接，默认为[]
		lockAnchors: false,//是否锁定锚链接，默认为false,设为true后链接地址不会改变
		navigation: false,//是否显示导航，默认为false
		navigationPosition: 'right',//导航小圆点的位置
		navigationTooltips: ['firstSlide', 'secondSlide'],//导航小圆点的提示
		showActiveTooltip: false,//是否显示当前页面的tooltip信息
		slidesNavigation: true,//是否显示横向幻灯片的导航，默认为false
		slidesNavPosition: 'bottom',//横向导航的位置，默认为bottom，可以设置为top或bottom
		 
		//Scrolling
		css3: true,//是否使用CSS3 transforms来实现滚动效果，默认为true
		scrollingSpeed: 700,//设置滚动速度，单位毫秒，默认700
		autoScrolling: true,//是否使用插件的滚动方式，默认为true,若为false则会出现浏览器自带滚动条
		fitToSection: true,//设置是否自适应整个窗口的空间，默认值：true
		scrollBar: false,//是否包含滚动条，默认为false,若为true浏览器自带滚动条出现
		easing: 'easeInOutCubic',//定义页面section滚动的动画方式，若修改此项需引入jquery.easing插件
		easingcss3: 'ease',//定义页面section滚动的过渡效果，若修改此项需引入第三方插件
		loopBottom: false,//滚动到最低部后是否连续滚动到顶部，默认为false
		loopTop: false,//滚动到最顶部后是否连续滚动到底部，默认为false
		loopHorizontal: true,//横向slide幻灯片是否循环滚动，默认为true
		continuousVertical: false,//是否循环滚动，不兼容loopTop和loopBottom选项
		normalScrollElements: '#element1, .element2',//避免自动滚动，滚动时的一些元素，例如百度地图
		scrollOverflow: false,//内容超过满屏后是否显示滚动条，true则显示滚动条，若需滚动查看内容还需要jquery.slimscroll插件的配合
		touchSensitivity: 15,//在移动设备中滑动页面的敏感性，默认为5最高100，越大越难滑动
		normalScrollElementTouchThreshold: 5,
		 
		//Accessibility
		keyboardScrolling: true,//是否可以使用键盘方向键导航，默认为true
		animateAnchor: true,//锚链接是否可以控制滚动动画，默认为true,若为false则锚链接定位失效
		recordHistory: true,//是否记录历史，默认为true,浏览器的前进后退可导航。若autoScrolling:false,那么这个属性将被关闭
		 
		//Design
		controlArrows: true,//定义是否通过箭头来控制slide,默认true
		verticalCentered: true,//定义每一页的内容是否垂直居中，默认true
		resize : false,//字体是否随窗口缩放而缩放，默认false
		sectionsColor : ['#ccc', '#fff'],//为每个section设置background-color属性
		paddingTop: '3em',设置每一个section顶部的padding,默认为0
		paddingBottom: '10px',设置每一个section底部的padding,默认为0
		fixedElements: '#header, .footer',固定元素，默认为null,需要配置一个jquery选择器，在页面滚动时，fixElements设置的元素不滚动
		responsiveWidth: 0,
		responsiveHeight: 0,
		 
		//Custom selectors
		sectionSelector: '.section',//section选择器。默认为.section
		slideSelector: '.slide',//slide选择器，默认为.slide
		 
		//events
		onLeave: function(index, nextIndex, direction){},
		afterLoad: function(anchorLink, index){},
		afterRender: function(){},
		afterResize: function(){},
		afterSlideLoad: function(anchorLink, index, slideAnchor, slideIndex){},
		onSlideLeave: function(anchorLink, index, slideIndex, direction, nextSlideIndex){}
	});
});
```









如今我们经常能见到全屏网站，尤其是国外网站。这些网站用几幅很大的图片或色块做背景，再添加一些简单的内容，显得格外的高端大气上档次。比如 iPhone 5C 的介绍页面（查看），QQ浏览器的官网站。如果你也希望你的网站能设计成全屏的，显得更上档次，你可以试试 fullPage.js。

主要功能有：

支持鼠标滚动

支持前进后退和键盘控制

多个回调函数

支持手机、平板触摸事件

支持 CSS3 动画

支持窗口缩放

窗口缩放时自动调整

可设置滚动宽度、背景颜色、滚动速度、循环选项、回调、文本对齐方式等等



## 使用方法 

### 1、引入文件

[?](#)

```
`<``link` `rel``=``"stylesheet"` `href``=``"css/jquery.fullPage.css"``>``<``script` `src``=``"js/jquery.min.js"``></``script``>` `<!-- jquery.easings.min.js 是必须的，用于 easing 参数，也可以使用完整的 jQuery UI 代替 -->``<``script` `src``=``"js/jquery.easings.min.js"``></``script``>` `<!-- 如果 scrollOverflow 设置为 true，则需要引入 jquery.slimscroll.min.js，一般情况下不需要 -->``<``script` `src``=``"js/jquery.slimscroll.min.js"``></``script``>` `<``script` `src``=``"js/jquery.fullPage.js"``></``script``>`
```

### 2、HTML

[?](#)

```
`<``div` `id``=``"fullpage"``>``    ``<``div` `class``=``"section"``>第一屏</``div``>``    ``<``div` `class``=``"section"``>第二屏</``div``>``    ``<``div` `class``=``"section"``>``        ``<``div` `class``=``"slide"``>第三屏的第一屏</``div``>``        ``<``div` `class``=``"slide"``>第三屏的第二屏</``div``>``        ``<``div` `class``=``"slide"``>第三屏的第三屏</``div``>``        ``<``div` `class``=``"slide"``>第三屏的第四屏</``div``>``    ``</``div``>``    ``<``div` `class``=``"section"``>第四屏</``div``>``</``div``>`
```

### 3、JavaScript

[?](#)

```
`$(``function``(){``    ``$(``'#fullpage'``).fullpage();``});`
```

## 配置

### 1、选项

| verticalCentered                  | 字符串 | true        | 内容是否垂直居中                                             |
| --------------------------------- | ------ | ----------- | ------------------------------------------------------------ |
| resize                            | 布尔值 | false       | 字体是否随着窗口缩放而缩放                                   |
| slidesColor                       | 函数   | 无          | 设置背景颜色                                                 |
| anchors                           | 数组   | 无          | 定义锚链接                                                   |
| scrollingSpeed                    | 整数   | 700         | 滚动速度，单位为毫秒                                         |
| easing                            | 字符串 | easeInQuart | 滚动动画方式                                                 |
| menu                              | 布尔值 | false       | 绑定菜单，设定的相关属性与 anchors 的值对应后，菜单可以控制滚动 |
| navigation                        | 布尔值 | false       | 是否显示项目导航                                             |
| navigationPosition                | 字符串 | right       | 项目导航的位置，可选 left 或 right                           |
| navigationColor                   | 字符串 | #000        | 项目导航的颜色                                               |
| navigationTooltips                | 数组   | 空          | 项目导航的 tip                                               |
| slidesNavigation                  | 布尔值 | false       | 是否显示左右滑块的项目导航                                   |
| slidesNavPosition                 | 字符串 | bottom      | 左右滑块的项目导航的位置，可选 top 或 bottom                 |
| controlArrowColor                 | 字符串 | #fff        | 左右滑块的箭头的背景颜色                                     |
| loopBottom                        | 布尔值 | false       | 滚动到最底部后是否滚回顶部                                   |
| loopTop                           | 布尔值 | false       | 滚动到最顶部后是否滚底部                                     |
| loopHorizontal                    | 布尔值 | true        | 左右滑块是否循环滑动                                         |
| autoScrolling                     | 布尔值 | true        | 是否使用插件的滚动方式，如果选择 false，则会出现浏览器自带的滚动条 |
| scrollOverflow                    | 布尔值 | false       | 内容超过满屏后是否显示滚动条                                 |
| css3                              | 布尔值 | false       | 是否使用 CSS3 transforms 滚动                                |
| paddingTop                        | 字符串 | 0           | 与顶部的距离                                                 |
| paddingBottom                     | 字符串 | 0           | 与底部距离                                                   |
| fixedElements                     | 字符串 | 无          |                                                              |
| normalScrollElements              |        | 无          |                                                              |
| keyboardScrolling                 | 布尔值 | true        | 是否使用键盘方向键导航                                       |
| touchSensitivity                  | 整数   | 5           |                                                              |
| continuousVertical                | 布尔值 | false       | 是否循环滚动，与 loopTop 及 loopBottom 不兼容                |
| animateAnchor                     | 布尔值 | true        |                                                              |
| normalScrollElementTouchThreshold | 整数   | 5           |                                                              |

### 2、方法

| moveSectionUp()        | 向上滚动                                 |
| ---------------------- | ---------------------------------------- |
| moveSectionDown()      | 向下滚动                                 |
| moveTo(section, slide) | 滚动到                                   |
| moveSlideRight()       | slide 向右滚动                           |
| moveSlideLeft()        | slide 向左滚动                           |
| setAutoScrolling()     | 设置页面滚动方式，设置为 true 时自动滚动 |
| setAllowScrolling()    | 添加或删除鼠标滚轮/触控板控制            |
| setKeyboardScrolling() | 添加或删除键盘方向键控制                 |
| setScrollingSpeed()    | 定义以毫秒为单位的滚动速度               |

### 3、回调函数

| afterLoad      | 滚动到某一屏后的回调函数，接收 anchorLink 和 index 两个参数，anchorLink 是锚链接的名称，index 是序号，从1开始计算 |
| -------------- | ------------------------------------------------------------ |
| onLeave        | 滚动前的回调函数，接收 index、nextIndex 和 direction 3个参数：index 是离开的“页面”的序号，从1开始计算；nextIndex 是滚动到的“页面”的序号，从1开始计算；direction 判断往上滚动还是往下滚动，值是 up 或 down。 |
| afterRender    | 页面结构生成后的回调函数，或者说页面初始化完成后的回调函数   |
| afterSlideLoad | 滚动到某一水平滑块后的回调函数，与 afterLoad 类似，接收 anchorLink、index、slideIndex、direction 4个参数 |
| onSlideLeave   | 某一水平滑块滚动前的回调函数，与 onLeave 类似，接收 anchorLink、index、slideIndex、direction 4个参数 |





# 总结





## 问题总结

放大页面排版错乱；给页面加一个大盒子



第三页，不停鼠标滑动01bug，多一块

fadeIn（）j

前加stop



最后一页图片：播放不全？

```js
background: url('../images/fifth_tit.png')no-repeat center;
```

播放完会回到中间，解决

```js
 background: url('../images/fifth_table.png') no-repeat top;
```





animationClass

.section.animation  .bg





权重问题;

伪类选择器：

浏览器权重在上面