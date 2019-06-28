CSS基本功：布局、盒子模型、选择器优先级、css3 flexbox

选择器 
过度（transiton）
动画（animation）
形状转换 transform:适用于2D或3D转换的元素 transform-origin：转换元素的位置（围绕那个点进行转换）。默认(x,y,z)：(50%,50%,0)）

阴影（box-shadow）
边框（box-border） border-radius（边框圆角）border-image（边框图片）

反射 
倒影（reflect）
颜色（提供了rgba和hsla的方法来显示颜色）
渐变
滤镜（filter）
布局 
flex弹性布局
grid栅格化布局
column-count多列布局
盒模型
媒体查询（一般用来做自适应布局，与rem布局结合使用可以有巧妙地效果）
用户界面

文本效果：
字体
图片：
按钮
分页：
框大小



**1 、css盒模型****



**2、字体font-family**

------

##### 3、可能用到的meta标签

##### 4、消除 transition 闪屏

**5.CSS 重排和重绘之间有什么区别？**



**6. 什么是 CSS 选择器权重以及它如何工作？**



**7.CSS 中的 pixel 与硬件/物理中的 pixel 有何不同？**



**8.什么是 sectioning 算法？**



**9.如果你用过 CSS Flex / CSS Grid（网格）布局，请说明你为什么要使用它？它为你解决了什么问题？**



**10.什么时候应该使用 CSS animations 而不是 CSS transitions ？你做出这个决定标准是什么？**

**11.如果你正在 Review CSS 代码，那么你在代码中经常遇到的问题是什么？**

**12 启动硬件加速**

------

##### 13、android 4.x bug

------

##### 14、JS 判断设备来源

------

##### 15、audio元素和video元素在ios和andriod中无法自动播放

##### 16、css实现单行文本溢出显示 ...

##### 17、实现多行文本溢出显示...

效果：

![img](https:////www.runoob.com/wp-content/uploads/2018/03/3820353650-5a8f7bb98a123_articlex.png)



##### 18、让图文不可复制

**19、盒子垂直水平居中**

##### 20、改变 placeholder 的字体颜色大小

##### 21 CSS Sprite是什么，谈谈这个技术的优缺点？

##### 22 以CSS3标准定义一个webkit内核浏览器识别的圆角（尺寸随意）

##### 23 行内元素有哪些？块级元素有哪些？CSS的盒模型？

##### 24 CSS display:none和visibility:hidden的区别

















**1 、css盒模型**

css盒模型，可能会要求手写一个布局，这个布局基本上用到的css是margin的负值，boxing-sizing：border-box，布局尽量往这方面想。浏览器布局的基本元素是盒，在w3c的标准模式下，width=width，但是在怪异模式下，width=border*2+padding*2+width;其中后代元素的width：100%；参照的是右边的那个width，

CSS盒模型原理

- 1、W3C 盒子模型的范围包括 margin、border、padding、content，并且 content 部分不包含其他部分。

- 2、IE 盒子模型的范围也包括 margin、border、padding、content，和标准 W3C 盒子模型不同的是：IE 盒子模型的 content 部分包含了 border 和 pading。 

  

  



**2、字体font-family**

```
@ 宋体      SimSun
@ 黑体      SimHei
@ 微软雅黑   Microsoft Yahei
@ 微软正黑体 Microsoft JhengHei
@ 新宋体    NSimSun
@ 新细明体  MingLiU
@ 细明体    MingLiU
@ 标楷体    DFKai-SB
@ 仿宋     FangSong
@ 楷体     KaiTi
@ 仿宋_GB2312  FangSong_GB2312
@ 楷体_GB2312  KaiTi_GB2312  
@
@ 说明：中文字体多数使用宋体、雅黑，英文用Helvetica

body { font-family: Microsoft Yahei,SimSun,Helvetica; }
```

------

##### 3、可能用到的meta标签

```
<!-- 设置缩放 -->
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no, minimal-ui" />
<!-- 可隐藏地址栏，仅针对IOS的Safari（注：IOS7.0版本以后，safari上已看不到效果） -->
<meta name="apple-mobile-web-app-capable" content="yes" />
<!-- 仅针对IOS的Safari顶端状态条的样式（可选default/black/black-translucent ） -->
<meta name="apple-mobile-web-app-status-bar-style" content="black" />
<!-- IOS中禁用将数字识别为电话号码/忽略Android平台中对邮箱地址的识别 -->
<meta name="format-detection"content="telephone=no, email=no" />
```

其他meta标签

```
<!-- 启用360浏览器的极速模式(webkit) -->
<meta name="renderer" content="webkit">
<!-- 避免IE使用兼容模式 -->
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<!-- 针对手持设备优化，主要是针对一些老的不识别viewport的浏览器，比如黑莓 -->
<meta name="HandheldFriendly" content="true">
<!-- 微软的老式浏览器 -->
<meta name="MobileOptimized" content="320">
<!-- uc强制竖屏 -->
<meta name="screen-orientation" content="portrait">
<!-- QQ强制竖屏 -->
<meta name="x5-orientation" content="portrait">
<!-- UC强制全屏 -->
<meta name="full-screen" content="yes">
<!-- QQ强制全屏 -->
<meta name="x5-fullscreen" content="true">
<!-- UC应用模式 -->
<meta name="browsermode" content="application">
<!-- QQ应用模式 -->
<meta name="x5-page-mode" content="app">
<!-- windows phone 点击无高光 -->
<meta name="msapplication-tap-highlight" content="no">
```

------

##### 4、消除 transition 闪屏

```
.css {
    -webkit-transform-style: preserve-3d;
    -webkit-backface-visibility: hidden;
    -webkit-perspective: 1000;
}
```

过渡动画（在没有启动硬件加速的情况下）会出现抖动的现象， 以上的解决方案只是改变视角来启动硬件加速的一种方式；启动硬件加速的另外一种方式： 

```
.css {
    -webkit-transform: translate3d(0,0,0);
    -moz-transform: translate3d(0,0,0);
    -ms-transform: translate3d(0,0,0);
    transform: translate3d(0,0,0);
}
```



**5.CSS 重排和重绘之间有什么区别？**

哪些 CSS 属性会导致重排及重绘？

**6. 什么是 CSS 选择器权重以及它如何工作？**

说说计算 CSS 选择器权重的算法。

**7.CSS 中的 pixel 与硬件/物理中的 pixel 有何不同？**

提示：像素不是像素不是像素 – ppk。

**8.什么是 sectioning 算法？**

提示：它也被称为 HTML5 大纲算法。特别是在构建具有语义结构的网站时非常重要。

**9.如果你用过 CSS Flex / CSS Grid（网格）布局，请说明你为什么要使用它？它为你解决了什么问题？**

- 使用 CSS Grid，百分比％和 fr 单位有何不同？
- 使用 CSS flexbox，有时 flex-items/children 会不考虑 flex 容器设置的宽度/高度？为什么会这样？
- 可以使用 CSS Grid 创建 Masonry layout（瀑布流布局）吗？如果可以，怎么做？
- 解释 CSS Grid 和 CSS flexbox 术语？
- 浮动元素（`float: left | right;`）如何在 CSS Grid 和 flexbox 中渲染？

提示：等高的列，垂直居中，复杂网格等。

**10.什么时候应该使用 CSS animations 而不是 CSS transitions ？你做出这个决定标准是什么？**

**11.如果你正在 Review CSS 代码，那么你在代码中经常遇到的问题是什么？**

示例：使用魔性数字，如 `width: 67px;` 或使用 `em` 代替 `rem` 单位，在通用代码之前编写 media queries（媒体查询），滥用 ID 和类等。





**12 启动硬件加速**

最常用的方式：translate3d、translateZ、transform

opacity 属性/过渡动画（需要动画执行的过程中才会创建合成层，动画没有开始或结束后元素还会回到之前的状态）

will-chang 属性（这个比较偏僻），一般配合opacity与translate使用（而且经测试，除了上述可以引发硬件加速的属性外，其它属性并不会变成复合层）。

弊端：硬件加速会导致 CPU 性能占用量过大，电池电量消耗加大 ；因此尽量避免泛滥使用硬件加速。

------

##### 13、android 4.x bug

- 1.三星 Galaxy S4中自带浏览器不支持border-radius缩写
- 2.同时设置border-radius和背景色的时候，背景色会溢出到圆角以外部分
- 3.部分手机(如三星)，a链接支持鼠标:visited事件，也就是说链接访问后文字变为紫色
- 4.android无法同时播放多音频audio
- 5.oppo 的border-radius 会失效

------

##### 14、JS 判断设备来源

```
// 判断移动端设备
function deviceType(){
    var ua = navigator.userAgent;
    var agent = ["Android", "iPhone", "SymbianOS", "Windows Phone", "iPad", "iPod"];    
    for(var i=0; i<len,len = agent.length; i++){
        if(ua.indexOf(agent[i])>0){         
            break;
        }
    }
}
deviceType();
window.addEventListener('resize', function(){
    deviceType();
})


// 判断微信浏览器
function isWeixin(){
    var ua = navigator.userAgent.toLowerCase();
    if(ua.match(/MicroMessenger/i)=='micromessenger'){
        return true;
    }else{
        return false;
    }
}
```

------

##### 15、audio元素和video元素在ios和andriod中无法自动播放

**原因：**因为各大浏览器都为了节省流量，做出了优化，在用户没有行为动作时（交互）不予许自动播放；

```
//音频，写法一
<audio src="music/bg.mp3" autoplay loop controls>你的浏览器还不支持哦</audio>

//音频，写法二
<audio controls="controls"> 
    <source src="music/bg.ogg" type="audio/ogg"></source>
    <source src="music/bg.mp3" type="audio/mpeg"></source>
    优先播放音乐bg.ogg，不支持在播放bg.mp3
</audio>

//JS绑定自动播放（操作window时，播放音乐）
$(window).one('touchstart', function(){
    music.play();
})

//微信下兼容处理
document.addEventListener("WeixinJSBridgeReady", function () {
    music.play();
}, false);

//小结
//1.audio元素的autoplay属性在IOS及Android上无法使用，在PC端正常；
//2.audio元素没有设置controls时，在IOS及Android会占据空间大小，而在PC端Chrome是不会占据任何空间；
//3.注意不要遗漏微信的兼容处理需要引用微信JS；
```

------

##### 16、css实现单行文本溢出显示 ...

直接上效果：相对于多行文本溢出做处理， 单行要简单多，且更容易理解。

![img](https:////www.runoob.com/wp-content/uploads/2018/03/3313696839-5a8f7bb9864cc_articlex.png)

实现方法:

```
overflow: hidden;
text-overflow:ellipsis;
white-space: nowrap;
```

当然还需要加宽度width属来兼容部分浏览。

------

##### 17、实现多行文本溢出显示...

效果：

![img](https:////www.runoob.com/wp-content/uploads/2018/03/3820353650-5a8f7bb98a123_articlex.png)

实现方法：

```
display: -webkit-box;
-webkit-box-orient: vertical;
-webkit-line-clamp: 3;
overflow: hidden;
```

适用范围：

因使用了WebKit的CSS扩展属性，该方法适用于WebKit浏览器及移动端；

注：

1、-webkit-line-clamp 用来限制在一个块元素显示的文本的行数。 为了实现该效果，它需要组合其他的WebKit属性。常见结合属性：

2、display: -webkit-box; 必须结合的属性，将对象作为弹性伸缩盒子模型显示 。

3、-webkit-box-orient 必须结合的属性，设置或检索伸缩盒对象的子元素的排列方式 。

如果你觉着这样还不够美观， 那么就接着往下看效果：

![img](https:////www.runoob.com/wp-content/uploads/2018/03/2039871283-5a8f7bb9883e8_articlex.png)

**这样 是不是你想要的呢？**

实现方法：

```
div {
    position: relative;
    line-height: 20px;
    max-height: 40px;
    overflow: hidden;
}

div:after {
    content: "..."; position: absolute; bottom: 0; right: 0; padding-left: 40px;
    background: -webkit-linear-gradient(left, transparent, #fff 55%);
    background: -o-linear-gradient(right, transparent, #fff 55%);
    background: -moz-linear-gradient(right, transparent, #fff 55%);
    background: linear-gradient(to right, transparent, #fff 55%);
}
```

不要只顾着吃，要注意胃口，此方法有个弊端 那就是 【未超出行的情况下也会出现省略号】 ，这样会不会很挫！！！ 没办法，只能结合JS 进行优化该方法了。

注：

- 1、将height设置为line-height的整数倍，防止超出的文字露出。
- 2、给p::after添加渐变背景可避免文字只显示一半。
- 3、由于ie6-7不显示content内容，所以要添加标签兼容ie6-7（如：…）；兼容ie8需要将::after替换成:after。

------

##### 18、让图文不可复制

这点应该大家 都很熟悉了， 某些时候【你懂的】为了快捷搜索答案，可是打死也不让你复制:

```
-webkit-user-select: none; 
-ms-user-select: none;
-moz-user-select: none;
-khtml-user-select: none;
user-select: none;
```

------

##### 19、盒子垂直水平居中

这个问题好像面试必问的吔！反正我是必问的，哈哈！！！ 其实无关多少种实现思路，只要你能实现就可以！

提供4种方法:

- 1、定位 盒子宽高已知， position: absolute; left: 50%; top: 50%; margin-left:-自身一半宽度; margin-top: -自身一半高度;

- 2、table-cell布局 父级 display: table-cell; vertical-align: middle;  子级 margin: 0 auto;

- 3、定位 + transform ; 适用于 子盒子 宽高不定时； （这里是本人常用方法）

  ```
  position: relative / absolute;
  /*top和left偏移各为50%*/
     top: 50%;
     left: 50%;
  /*translate(-50%,-50%) 偏移自身的宽和高的-50%*/
  transform: translate(-50%, -50%); 注意这里启动了3D硬件加速哦 会增加耗电量的 （至于何是3D加速 请看浏览器进程与线程篇）
  ```

- 4、flex 布局

  ```
  父级： 
  /*flex 布局*/
  display: flex;
  /*实现垂直居中*/
  align-items: center;
  /*实现水平居中*/
  justify-content: center;
  ```

再加一种水平方向上居中 ：margin-left : 50% ; transform: translateX(-50%);

那有些网页为了尊重原创，复制的文本 都会被加上一段来源说明，是如何做到的呢？问的好！ 等的就是你这个问题 -_- 。

大致思路：

- 1、答案区域监听copy事件，并阻止这个事件的默认行为。
- 2、获取选中的内容（window.getSelection()）加上版权信息，然后设置到剪切板（clipboarddata.setData()）。

------

##### 20、改变 placeholder 的字体颜色大小

其实这个方法也就在 PC 端可以，真机上屁用都没有，当时我就哭了。 但还是贴出来吧

```
input::-webkit-input-placeholder { 
    /* WebKit browsers */ 
    font-size:14px;
    color: #333;
} 
input::-moz-placeholder { 
    /* Mozilla Firefox 19+ */ 
    font-size:14px;
    color: #333;
} 
input:-ms-input-placeholder { 
    /* Internet Explorer 10+ */ 
    font-size:14px;
    color: #333;
}
```

------

##### 













##### 21 CSS Sprite是什么，谈谈这个技术的优缺点？

CSS sprites在国内很多人叫css精灵，是一种网页图片应用处理方式。它允许你将一个页面涉及到的所有零星图片都包含到 中去，减少对服务器的请求次数，提高访问速度。

1、优点：

- （1）利用CSS Sprites能很好地减少了网页的http请求，从而大大的提高了页面的性能，这也是CSS Sprite的优点，也是其被广泛传播和应用的主要原因。
- （2）解决了网页设计师在图片命名上的困扰，只需对一张集合的图片上命名就可以了，不需要对每一个小元素命名，从而提高了网页的制作效率。
- （3）换风格方便，只需要在一张或少张图片上修改图片的颜色或样式，整个网页的风格就可以改变。维护起来也很方便。

2、缺点：

- （1）在图片合并的时候，你要把多张图片有序的合理的合并成一张图片，还要留好足够的空间，防止板块内显示不必要的背景。这些还好，最痛苦的是在宽屏，高分辨率的屏幕下的自适应页面，你的图片如果不够宽，很容易将背景断裂。
- （2）CSS Sprites在开发的时候比较麻烦，你要通过photoshop或其他工具测量计算每一个背景单元的精确位是针线活，没什么难度，但是很繁琐。
- （3）CSS Sprites在维护的时候比较麻烦，如果页面背景有少许改动，一般就要改这张合并的图片，无需改的好不要动，这样避免改动更多的css，如果在原来的地方放不下，又只能（最好）往下加图片，这样图片的字加了，还要改动css。

##### 22 以CSS3标准定义一个webkit内核浏览器识别的圆角（尺寸随意）

```
-moz-border-radius: 10px; -webkit-border-radius: 10px; border-radius:10px;
```

##### 23 行内元素有哪些？块级元素有哪些？CSS的盒模型？

- 行内元素有：a b span I em img input select strong
- 级元素有：div ul ol li dl dt dd h1 h2 h3 h4 p
- 盒模型：margin border padding width

##### 24 CSS display:none和visibility:hidden的区别

- visibility:hidden隐藏，但在浏览时保留位置 
- display:none视为不存在，且不加载













## CSS

- 介绍一下标准的CSS的盒子模型？低版本IE的盒子模型有什么不同的？

  ```
  （1）有两种， IE 盒子模型、W3C 盒子模型；
  （2）盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border)；
  （3）区  别： IE的content部分把 border 和 padding计算了进去;
  ```

- CSS选择符有哪些？哪些属性可以继承？

  ```
  *   1.id选择器（ # myid）
      2.类选择器（.myclassname）
      3.标签选择器（div, h1, p）
      4.相邻选择器（h1 + p）
      5.子选择器（ul > li）
      6.后代选择器（li a）
      7.通配符选择器（ * ）
      8.属性选择器（a[rel = "external"]）
      9.伪类选择器（a:hover, li:nth-child）
  
  *   可继承的样式： font-size font-family color, UL LI DL DD DT;
  
  *   不可继承的样式：border padding margin width height ;
  ```

- CSS优先级算法如何计算？

  ```
  *   优先级就近原则，同权重情况下样式定义最近者为准;
  
  *   载入样式以最后载入的定位为准;
  
  优先级为:
     !important >  id > class > tag
      important 比 内联优先级高
  ```

  

- CSS3新增伪类有那些？

  ```
  举例：
      p:first-of-type 选择属于其父元素的首个 <p> 元素的每个 <p> 元素。
      p:last-of-type  选择属于其父元素的最后 <p> 元素的每个 <p> 元素。
      p:only-of-type  选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。
      p:only-child        选择属于其父元素的唯一子元素的每个 <p> 元素。
      p:nth-child(2)  选择属于其父元素的第二个子元素的每个 <p> 元素。
  
      :after          在元素之前添加内容,也可以用来做清除浮动。
      :before         在元素之后添加内容
      :enabled        
      :disabled       控制表单控件的禁用状态。
      :checked        单选框或复选框被选中。
  ```

- 如何居中div？如何居中一个浮动元素？如何让绝对定位的div居中？

  - 给div设置一个宽度，然后添加margin:0 auto属性

    ```
    div{
        width:200px;
        margin:0 auto;
     }
    ```

  - 居中一个浮动元素

    ```
      确定容器的宽高 宽500 高 300 的层
      设置层的外边距
    
     .div {
          width:500px ; height:300px;//高度可以不设
          margin: -150px 0 0 -250px;
          position:relative;         //相对定位
          background-color:pink;     //方便看效果
          left:50%;
          top:50%;
     }
    ```

  - 让绝对定位的div居中

    ```
      position: absolute;
      width: 1200px;
      background: none;
      margin: 0 auto;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
    ```

- display有哪些值？说明他们的作用。

  ```
    block         像块类型元素一样显示。
    none          此元素不会被显示。
    inline-block  像行内元素一样显示，但其内容像块类型元素一样显示。
    list-item     像块类型元素一样显示，并添加样式列表标记。
    table         此元素会作为块级表格来显示
    inherit       规定应该从父元素继承 display 属性的值
  ```

- position的值relative和absolute定位原点是？

  ```
    absolute
      生成绝对定位的元素，相对于值不为 static的第一个父元素进行定位。
    fixed （老IE不支持）
      生成绝对定位的元素，相对于浏览器窗口进行定位。
    relative
      生成相对定位的元素，相对于其正常位置进行定位。
    static
      默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right z-index 声明）。
    inherit
      规定从父元素继承 position 属性的值。
  ```

- CSS3有哪些新特性？

  ```
    新增各种CSS选择器  （: not(.input)：所有 class 不是“input”的节点）
    圆角           （border-radius:8px）
    多列布局        （multi-column layout）
    阴影和反射        （Shadow\Reflect）
    文字特效      （text-shadow、）
    文字渲染      （Text-decoration）
    线性渐变      （gradient）
    旋转          （transform）
    增加了旋转,缩放,定位,倾斜,动画，多背景
    transform:\scale(0.85,0.90)\ translate(0px,-30px)\ skew(-9deg,0deg)\Animation:
  ```

- 请解释一下CSS3的Flexbox（弹性盒布局模型）,以及适用场景？

  ```
   .
  ```

- 用纯CSS创建一个三角形的原理是什么？

  ```
  把上、左、右三条边隐藏掉（颜色设为 transparent）
  #demo {
    width: 0;
    height: 0;
    border-width: 20px;
    border-style: solid;
    border-color: transparent transparent red transparent;
  }
  ```

- 一个满屏 品 字布局 如何设计?

  ```
  简单的方式：
      上面的div宽100%，
      下面的两个div分别宽50%，
      然后用float或者inline使其不换行即可
  ```

- 经常遇到的浏览器的兼容性有哪些？原因，解决方法是什么，常用hack的技巧 ？

  

  ```
  * png24位的图片在iE6浏览器上出现背景，解决方案是做成PNG8.
  
  * 浏览器默认的margin和padding不同。解决方案是加一个全局的*{margin:0;padding:0;}来统一。
  
  * IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。
  
    浮动ie产生的双倍距离 #box{ float:left; width:10px; margin:0 0 0 100px;}
  
    这种情况之下IE会产生20px的距离，解决方案是在float的标签样式控制中加入 ——_display:inline;将其转化为行内属性。(_这个符号只有ie6会识别)
  
    渐进识别的方式，从总体中逐渐排除局部。
  
    首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。
    接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。
  
    css
        .bb{
            background-color:#f1ee18;/*所有识别*/
            .background-color:#00deff\9; /*IE6、7、8识别*/
            +background-color:#a200ff;/*IE6、7识别*/
            _background-color:#1e0bd1;/*IE6识别*/
        }
  
  
  *  IE下,even对象有x,y属性,但是没有pageX,pageY属性;
     Firefox下,event对象有pageX,pageY属性,但是没有x,y属性。
  
  *  解决方法：（条件注释）缺点是在IE浏览器下可能会增加额外的HTTP请求数。
  
  *  Chrome 中文界面下默认会将小于 12px 的文本强制按照 12px 显示,
     可通过加入 CSS 属性 -webkit-text-size-adjust: none; 解决。
  
  超链接访问过后hover样式就不出现了 被点击访问过的超链接样式不在具有hover和active了解决方法是改变CSS属性的排列顺序:
  L-V-H-A :  a:link {} a:visited {} a:hover {} a:active {}
  
  兼容性：
  
      1、IE6对PNG图片格式支持不好。gif和png这两种图片的不同，gif支持图像透明，体积很小，网上很多小动画都是gif格式，保存出来的图片相对png图片会有明显的齿缘，视觉效果不太好，png图片相对gif占用内存小，但是png图片在IE6下背景是不透明的，针对IE6下图片背景不透明，可以专门写css hack语句。或者在PS中保存为PNG8格式的图片，有或者引入一段脚本处理。
     
      5、IE下可以通过常规方法获取属性值，也可以通过getAttribute()方法获取属性。在火狐下只能用getAtrribute()方法。解决办法：统一用getAttribute()。
      6、Chorme下会默认将文本字体小于12px的强制换为12px。解决办法：加上-webkit-text-size-adjust: none ;
      
      8、上下margin会重合的问题。margin-left和margin-right不会重合，但是margin-top和margin-bottom会重合。解决办法：养成良好的书写习惯，同时书写margin-top或者同时书写margin-bottm。
      9、怪异模式问题，如果漏写DTD声明，火狐还是会正常解析，但是IE会触发怪异模式。加上<!DOCTYPE html>即可
      10,3像素问题  使用float引起的  使用  dispaly:inline
      11,IE  z-index问题  给父级添加position:relative
      12,min-height 最小高度  !important 
      13,IE5-8不支持opacity    .opacity{        opacity:0.4,        filter:alpha(opacity=60);        -ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=60)"}
      14、IE6不支持PNG透明管背景色，IE6下使用gif图片,png24的图片在ie6浏览器上显示背景色，做成png8的
      15、IE下even对象只有x,y属性，但是没有pagex和pagey属性，火狐只有pagex pagey属性。
      16、谷歌下默认会将小于12px的文本设置按照12px显示，可是通过加入-webkit-text-size-adjust:none;解决。
      17 、ie6中，父级元素浮动以后，内部元素内容撑不开宽度
      解决方法：元素内部的块级元素也设置浮动
      代码如下：
      html：
      <div class="box"><div class="left"><h3>左侧</h3></div><div class="right"><h3>右侧</h3></div></div>
      css：
      .box {width:400px;}.left {background: red;float:left;}.right{background: yellow;float:right;}h3{margin:0;float:left;/*此处设置浮动，如果不设置，内容撑不来宽度*/}
      
      18、在IE6下不支持1px的dotted边框样式
      解决方法：可以采取切背景平铺的方法
      19、两个块级元素，父元素设置了overflow:auto；子元素设置了position:relative ;且高度大于父元素，在IE6、IE7会被隐藏而不是溢出；
      解决方案：父级元素设置position:relative
      
      20、边距重叠问题；当相邻两个元素都设置了margin 边距时，margin 将取最大值，舍弃最小值；
      解决方案：为了不让边重叠，可以给子元素增加一个父级元素，并设置父级元素为overflow:hidden；
  
  
  ```

- https://blog.csdn.net/gj1949/article/details/53885384

  

  hack:

  ```
  1、什么是CSS hack?
  CSS hack是通过在CSS样式中加入一些特殊的符号，让不同的浏览器识别不同的符号（什么样的浏览器识别什么样的符号是有标准的，CSS hack就是让你记住这个标准），以达到应用不同的CSS样式的目的，比如.kwstu{width:300px;_width:200px;}，一般浏览器会先给元素使用width:300px;的样式，紧接着后面还有个_width:200px;由于下划线_width只有IE6可以识别，所以此样式在IE6中实际设置对象的宽度为200px，后面的把前面的给覆盖了，而其他浏览器不识别_width不会执行_width:200px;这句样式，所以在其他浏览器中设置对象的宽度就是300px;
  以下是引自百度文库的定义
  简单地讲，css hack指各版本及各品牌浏览器之间对CSS解释后出现网页内容的误差(比如我们常说错位)的处理。由于各浏览器的内核不同，所以会造成一些误差就像JS一样，一个JS网页特效，在微软IE6、IE7、IE8浏览器有效果，但可能在火狐（Mozilla Firefox）谷歌浏览器无效，这样就叫做JS hack ，所以我们对于CSS来说他们来解决各浏览器对CSS解释不同所采取的区别不同浏览器制作不同的CSS样式的设置来解决这些问题就叫作CSS Hack。
  注意：我们通常主要考虑的浏览器有IE6、IE7、IE8、谷歌浏览器（chrome）、火狐（Mozilla Firefox）即可，至于我们常用的傲游、QQ的TT浏览器是用你计算机中装的系统自带浏览器的内核，所以只需要兼容以上浏览器即可兼容TT\傲游浏览器。
  2、CSS hack解决问题
  CSS hack用来解决有些css属性在不同浏览器中显示的效果不一样的问题，如margin属性在ie6中显示的距离会比其他浏览器中显示的距离宽2倍，也就是说margin-left:20px;在ie6中距左侧对象的实际显示距离是40px，而在非ie6中显示的距左侧对象的距离是设置的值20px;所以要想设置一个对象距离左侧对象的距离在所有浏览器中都显示是20px的宽度的样式应为：.kwstu{margin-left:20px;_margin-left:20px;}。
  3、浏览器识别字符标准对应表
  
  从上图可以分析出以下几种情况：
  1.大部分特殊字符IE浏览器支持，其他主流浏览器firefox，chrome，opera，safari不支持 (opera可识别除外)。
  2.\9    ：所有IE浏览器都支持
  3._和-  ：仅IE6支持
  4.*     ：IE6、E7支持
  5.\0    ：IE8、IE9支持，opera部分支持
  6.\9\0  ：IE8部分支持、IE9支持
  7.\0\9  ：IE8、IE9支持
  4、各种CSS hack情况介绍 
  1.区别IE和非IE浏览器
  #tip{ 
  background:blue;/*非IE背景蓝色  因为所有浏览器都能解释*/ 
  background:red\9;/*IE6、IE7、IE8、IE9背景紅色 因为\9在IE6.7.8.9中可以识别，覆盖上面样式 IE10跟11应该不识别，IE11测试确定*/ 
  } 
  2.区别IE6,IE7,IE8,FF
  【区别符号】：“\9”、“*”、“_”
  #tip{ 
  background:blue;/*Firefox背景变蓝色 所有浏览器都支持*/ 
  background:red\9;/*IE8背景变红色 IE6、7、8、9支持覆盖上面样式*/ 
  *background:black;/*IE7背景变黑色 IE6、7支持又一次覆盖上面样式*/ 
  _background:orange;/*IE6背景变橘色 紧IE6支持又一次覆盖上面样式*/ 
  }  
  【说明】：因为IE系列浏览器可读「\9」，而IE6和IE7可读「*」(米字号)，另外IE6可辨识「_」(底线)，因此可以依照顺序写下来，就会让浏览器正确的读取到自己看得懂得CSS语法，所以就可以有效区分IE各版本和非IE浏览器(像是Firefox、Opera、GoogleChrome、Safari等)。
  3.区别IE6、IE7、Firefox(方法1)
  【区别符号】：“*”、“_”
  #tip{  
  background:blue;/*Firefox背景变蓝色*/  
  *background:black;/*IE7背景变黑色*/  
  _background:orange;/*IE6背景变橘色*/  
  } 
  【说明】：IE7和IE6可读「*」(米字号)，IE6又可以读「_」(底线)，但是IE7却无法读取「_」，至于Firefox(非IE浏览器)则完全无法辨识「*」和「_」，因此就可以透过这样的差异性来区分IE6、IE7、Firefox
  4.区别IE6、IE7、Firefox(方法2)
  【区别符号】：“*”、“!important”
  #tip{  
  background:blue;/*Firefox背景变蓝色*/  
  *background:green!important;/*IE7背景变绿色*/  
  *background:orange;/*IE6背景变橘色*/  
  } 
  【说明】：IE7可以辨识「*」和「!important」，但是IE6只可以辨识「*」，却无法辨识「!important」，至于Firefox可以读取「!important」但不能辨识「*」因此可以透过这样的差异来有效区隔IE6、IE7、Firefox。 
  5.区别IE7、Firefox
  【区别符号】：“*”、“!important”
  #tip{  
  background:blue;/*Firefox背景变蓝色*/  
  *background:green!important;/*IE7背景变绿色*/  
  } 
  【说明】：因为Firefox可以辨识「!important」但却无法辨识「*」，而IE7则可以同时看懂「*」、「!important」，因此可以两个辨识符号来区隔IE7和Firefox。
  6.区别IE6、IE7(方法1)
  【区别符号】：“*”、“_”
  #tip{  
  *background:black;/*IE7背景变黑色*/  
  _background:orange;/*IE6背景变橘色*/  
  } 
  【说明】：IE7和IE6都可以辨识「*」(米字号)，但IE6可以辨识「_」(底线)，IE7却无法辨识，透过IE7无法读取「_」的特性就能轻鬆区隔IE6和IE7之间的差异。
  7.区别IE6、IE7(方法2)
  【区别符号】：“!important”
  #tip{  
  background:black!important;/*IE7背景变黑色*/  
  background:orange;/*IE6背景变橘色*/  
  } 
  【说明】：因为IE7可读取「!important;」但IE6却不行，而CSS的读取步骤是从上到下，因此IE6读取时因无法辨识「!important」而直接跳到下一行读取CSS，所以背景色会呈现橘色。
  8.区别IE6、Firefox
  【区别符号】：“_”
  #tip{  
  background:black;/*Firefox背景变黑色*/  
  _background:orange;/*IE6背景变橘色*/  
  } 
  【说明】：因为IE6可以辨识「_」(底线)，但是Firefox却不行，因此可以透过这样的差异来区隔Firefox和IE6，有效达成CSShack。
  5、IE浏览器下hack总结
  element{
  color：#666\9； //IE8 IE9
  * color：#999；   //IE7
  _color:#EBEBEB； //IE6
  }
  可以看出，利用字符识别无法区分IE8和IE9，我们可以从伪类的识别来区分
  element{
  color：#666\9；      //IE8
  * color：#999；        //IE7
  _color:#EBEBEB；      //IE6
  }
  :root element{color：#666\9;}//IE9
  【说明】：“:root”伪类IE系列只有IE9支持，其他主流浏览器均支持，利用这一点来区分IE8和IE9。另外考虑到opera部分支持，完全支持:root,所以不使用。
  6、其他主流浏览器css hack总结
  1.Firefox浏览器：mozilla私有属性
  @-moz-document url-prefix(){ .element{color:#f1f1f1;}} //Firefox
  2.Webkit和Opera:
  @media all and (min-width: 0px){ .element{color:#777;} }
  //Webkit
  @media screen and (-webkit-min-device-pixel-ratio:0)
  {
  .element{color:#444;}
  }
  //Opera
  @media all and (-webkit-min-device-pixel-ratio:10000), not all and (-webkit-min-device-pixel-ratio:0) {
  .element{color:#336699;}
  }
  7、兼容各大主流浏览器(最新版本)css hack汇总如下（最全的）：
  .element{
  color:#000;             /*w3c标准*/
  [;color:#f00;];         /*Webkit(chrome和safari)*/
  color:#666\9;           /*IE8*/
  *color:#999;            /*IE7*/
  _color:#333;            /*IE6*/
  }
  :root .element{color:#0f0\9;}  /*IE9*/
  @media all and (-webkit-min-device-pixel-ratio:10000), not all and (
  -webkit-min-device-pixel-ratio:0) { .element{color:#336699;}}  /*opera*/
  @-moz-document url-prefix(){ .element{color:#f1f1f1;}} /*Firefox*/
  8、建议：实际开发先如果不是很清楚可以先写布局代码，写一个阶段用浏览器测试工具（常用工具推荐IETEST）测试一个各个版本浏览器的布局效果，如有问题针对有问题的浏览器单独调试。
  ```

  

- li与li之间有看不见的空白间隔是什么原因引起的？有什么解决办法？

  ```
  行框的排列会受到中间空白（回车\空格）等的影响，因为空格也属于字符,这些空白也会被应用样式，占据空间，所以会有间隔，把字符大小设为0，就没有空格了。
  ```

- 为什么要初始化CSS样式。

  ```
  - 因为浏览器的兼容问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面显示差异。
  
  - 当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。
  
  最简单的初始化方法： * {padding: 0; margin: 0;} （强烈不建议）
  
  淘宝的样式初始化代码：
  body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin:0; padding:0; }
  body, button, input, select, textarea { font:12px/1.5tahoma, arial, \5b8b\4f53; }
  h1, h2, h3, h4, h5, h6{ font-size:100%; }
  address, cite, dfn, em, var { font-style:normal; }
  code, kbd, pre, samp { font-family:couriernew, courier, monospace; }
  small{ font-size:12px; }
  ul, ol { list-style:none; }
  a { text-decoration:none; }
  a:hover { text-decoration:underline; }
  sup { vertical-align:text-top; }
  sub{ vertical-align:text-bottom; }
  legend { color:#000; }
  fieldset, img { border:0; }
  button, input, select, textarea { font-size:100%; }
  table { border-collapse:collapse; border-spacing:0; }
  ```

- absolute的containing block(容器块)计算方式跟正常流有什么不同？

  ```
  无论属于哪种，都要先找到其祖先元素中最近的 position 值不为 static 的元素，然后再判断：
  1、若此元素为 inline 元素，则 containing block 为能够包含这个元素生成的第一个和最后一个 inline box 的 padding box (除 margin, border 外的区域) 的最小矩形；
  2、否则,则由这个祖先元素的 padding box 构成。
  如果都找不到，则为 initial containing block。
  
  补充：
  1. static(默认的)/relative：简单说就是它的父元素的内容框（即去掉padding的部分）
  2. absolute: 向上找最近的定位为absolute/relative的元素
  3. fixed: 它的containing block一律为根元素(html/body)，根元素也是initial containing block
  ```

- CSS里的visibility属性有个collapse属性值是干嘛用的？在不同浏览器下以后什么区别？

- position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？

- 对BFC规范(块级格式化上下文：block formatting context)的理解？

  ```
  （W3C CSS 2.1 规范中的一个概念,它是一个独立容器，决定了元素如何对其内容进行定位,以及与其他元素的关系和相互作用。）
   一个页面是由很多个 Box 组成的,元素的类型和 display 属性,决定了这个 Box 的类型。
   不同类型的 Box,会参与不同的 Formatting Context（决定如何渲染文档的容器）,因此Box内的元素会以不同的方式渲染,也就是说BFC内部的元素和外部的元素不会互相影响。
  ```

- css定义的权重

  ```
  以下是权重的规则：标签的权重为1，class的权重为10，id的权重为100，以下例子是演示各种定义的权重值：
  
  /*权重为1*/
  div{
  }
  /*权重为10*/
  .class1{
  }
  /*权重为100*/
  #id1{
  }
  /*权重为100+1=101*/
  #id1 div{
  }
  /*权重为10+1=11*/
  .class1 div{
  }
  /*权重为10+10+1=21*/
  .class1 .class2 div{
  }
  
  如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现
  ```

- 请解释一下为什么会出现浮动和什么时候需要清除浮动？清除浮动的方式

- 移动端的布局用过媒体查询吗？

- 使用 CSS 预处理器吗？喜欢那个？

  ```
  SASS (SASS、LESS没有本质区别，只因为团队前端都是用的SASS)
  ```

- CSS优化、提高性能的方法有哪些？

- 浏览器是怎样解析CSS选择器的？

- 在网页中的应该使用奇数还是偶数的字体？为什么呢？

- margin和padding分别适合什么场景使用？

- 抽离样式模块怎么写，说出思路，有无实践经验？[阿里航旅的面试题]

- 元素竖向的百分比设定是相对于容器的高度吗？

- 全屏滚动的原理是什么？用到了CSS的那些属性？

- 什么是响应式设计？响应式设计的基本原理是什么？如何兼容低版本的IE？

- 视差滚动效果，如何给每页做不同的动画？（回到顶部，向下滑动要再次出现，和只出现一次分别怎么做？）

- ::before 和 :after中双冒号和单冒号 有什么区别？解释一下这2个伪元素的作用。

- 如何修改chrome记住密码后自动填充表单的黄色背景 ？

- 你对line-height是如何理解的？

- 设置元素浮动后，该元素的display值是多少？（自动变成display:block）

- 怎么让Chrome支持小于12px 的文字？

- 让页面里的字体变清晰，变细用CSS怎么做？（-webkit-font-smoothing: antialiased;）

- font-style属性可以让它赋值为"oblique" oblique是什么意思？

- position:fixed;在android下无效怎么处理？

- 如果需要手动写动画，你认为最小时间间隔是多久，为什么？（阿里）

  ```
  多数显示器默认频率是60Hz，即1秒刷新60次，所以理论上最小间隔为1/60＊1000ms ＝ 16.7ms
  ```

- display:inline-block 什么时候会显示间隙？(携程)

  ```
  移除空格、使用margin负值、使用font-size:0、letter-spacing、word-spacing
  ```

- overflow: scroll时不能平滑滚动的问题怎么处理？

- 有一个高度自适应的div，里面有两个div，一个高度100px，希望另一个填满剩下的高度。

- png、jpg、gif 这些图片格式解释一下，分别什么时候用。有没有了解过webp？

- 什么是Cookie 隔离？（或者说：请求资源的时候不要让它带cookie怎么做）

  ```
  如果静态文件都放在主域名下，那静态文件请求的时候都带有的cookie的数据提交给server的，非常浪费流量，
  所以不如隔离开。
  
  因为cookie有域的限制，因此不能跨域提交请求，故使用非主要域名的时候，请求头中就不会带有cookie数据，
  这样可以降低请求头的大小，降低请求时间，从而达到降低整体请求延时的目的。
  
  同时这种方式不会将cookie传入Web Server，也减少了Web Server对cookie的处理分析环节，
  提高了webserver的http请求的解析速度。
  ```

- style标签写在body后与body前有什么区别？

- 什么是CSS 预处理器 / 后处理器？

  ```
  - 预处理器例如：LESS、Sass、Stylus，用来预编译Sass或less，增强了css代码的复用性，
    还有层级、mixin、变量、循环、函数等，具有很方便的UI组件模块化开发能力，极大的提高工作效率。
  
  - 后处理器例如：PostCSS，通常被视为在完成的样式表中根据CSS规范处理CSS，让其更有效；目前最常做的
    是给CSS属性添加浏览器私有前缀，实现跨浏览器兼容性的问题。
  ```

#

