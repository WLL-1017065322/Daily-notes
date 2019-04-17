## H5 新特性

1. 语义化标签：header、footer、section、nav、aside、article
2. 增强型表单：input 的多个 type
3. 新增表单元素：datalist、keygen、output
4. 新增表单属性：placehoder、required、min 和 max
5. 音频视频：audio、video
6. canvas
7. 地理定位
8. 拖拽
9. 本地存储：localStorage - 没有时间限制的数据存储；sessionStorage - 针对一个 session 的数据存储，当用户关闭浏览器窗口后，数据会被删除
10. 新事件：onresize、ondrag、onscroll、onmousewheel、onerror、onplay、onpause
11. WebSocket：单个 TCP 连接上进行全双工通讯的协议







### 语义化标签

| 标签     | 描述                             |
| -------- | -------------------------------- |
| header   | 定义了文档的头部区域             |
| footer   | 定义了文档的尾部区域             |
| nav      | 定义文档的导航                   |
| section  | 定义文档中的节（section、区段）  |
| article  | 定义页面独立的内容区域           |
| aside    | 定义页面的侧边栏内容             |
| detailes | 用于描述文档或文档某个部分的细节 |
| summary  | 标签包含 details 元素的标题      |
| dialog   | 定义对话框，比如提示框           |

### 增强型表单

HTML5 拥有多个新的表单 Input 输入类型。这些新特性提供了更好的输入控制和验证

| input 的 type | 描述                         |
| ------------- | ---------------------------- |
| color         | 主要用于选取颜色             |
| date          | 从一个日期选择器选择一个日期 |
| datetime      | 选择一个日期（UTC 时间）     |
| email         | 包含 e-mail 地址的输入域     |
| month         | 选择一个月份                 |
| number        | 数值的输入域                 |
| range         | 一定范围内数字值的输入域     |
| search        | 用于搜索域                   |
| tel           | 定义输入电话号码字段         |
| time          | 选择一个时间                 |
| url           | URL 地址的输入域             |
| week          | 选择周和年                   |

### html5 也新增以下表单元素

| 表单元素 | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| datalist | 元素规定输入域的选项列表，使用 input 元素的 list 属性与 datalist 元素的 id 绑定 |
| keygen   | 提供一种验证用户的可靠方法，标签规定用于表单的密钥对生成器字段 |
| output   | 用于不同类型的输出，比如计算或脚本输出                       |

### html5 新增的表单属性

| 表单属性        | 描述                                                         |
| --------------- | ------------------------------------------------------------ |
| placehoder      | 简短的提示在用户输入值前会显示在输入域上。即我们常见的输入框默认提示，在用户输入后消失 |
| required        | 是一个 boolean 属性。要求填写的输入域不能为空                |
| pattern         | 描述了一个正则表达式用于验证 input 元素的值                  |
| min 和 max      | 设置元素最小值与最大值                                       |
| step            | 为输入域规定合法的数字间隔                                   |
| height 和 width | 用于 image 类型的 input 标签的图像高度和宽度                 |
| autofocus       | 是一个 boolean 属性。规定在页面加载时，域自动地获得焦点      |
| multiple        | 是一个 boolean 属性。规定 input 元素中可选择多个值           |

### html5 新事件

| 事件         | 描述                                 |
| ------------ | ------------------------------------ |
| onresize     | 当调整窗口大小时运行脚本             |
| ondrag       | 当拖动元素时运行脚本                 |
| onscroll     | 当滚动元素滚动元素的滚动条时运行脚本 |
| onmousewheel | 当转动鼠标滚轮时运行脚本             |
| onerror      | 当错误发生时运行脚本                 |
| onplay       | 当媒介数据将要开始播放时运行脚本     |
| onpause      | 当媒介数据暂停时运行脚本             |

- 块级元素
  div、p、h1~h6、ul、ol、dl、li、dd、table、hr、blockquote、address、table、menu、pre，HTML5 新增的 header、section、aside、footer 等
- 行内元素
  pan、img、a、lable、input、abbr（缩写）、em（强调）、big、cite（引用）、i（斜体）、q（短引用）、textarea、select、small、sub、sup，strong、u（下划线）、button







## CSS3 新特性

1. 选择器
2. 背景和边框
3. 文本效果
4. 2D/3D 转换
5. 动画、过渡
6. 多列布局
7. 用户界面







### 选择器

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
:last-child /* 选择元素最后一个孩子 */
:first-child /* 选择元素第一个孩子 */
:nth-child(1) /* 按照第几个孩子给它设置样式 */
:nth-child(even) /* 按照偶数 */
:nth-child(odd)  /* 按照奇数 */
:disabled /* 选择每个禁用的E元素 */
:checked /* 选择每个被选中的E元素 */
:not(selector) /* 选择非 selector 元素的每个元素 */
::selection /* 选择被用户选取的元素部分 */
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```css

```

伪类和伪元素：

> 根本区别在于它们是否创造了新的元素（抽象）

- 伪类：用于向某些选择器添加特殊的效果（没有创建新元素）

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
:last-child /* 选择元素最后一个孩子 */
:first-child /* 选择元素第一个孩子 */
:nth-child(1) /* 按照第几个孩子给它设置样式 */
a:link {color: #FF0000} /* 未访问的链接 */
a:visited {color: #00FF00} /* 已访问的链接 */
a:hover {color: #FF00FF} /* 鼠标移动到链接上 */
a:active {color: #0000FF} /* 选定的链接 */
```

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```css

```

- 伪元素：创建了 html 中不存在的元素，用于将特殊的效果添加到某些选择器

```
::before {} /* 选择器在被选元素的前面插入内容和定义css，使用 content 属性来指定要插入的内容。 */
::after {} /* 选择器在被选元素的后面插入内容和定义css，使用 content 属性来指定要插入的内容。 */
:first-letter /* 选择该元素内容的首字母 */
:first-line /* 选择该元素内容的首行 */
::selection /* 选择被用户选取的元素部分 */

```

### 背景和边框

- 背景：
  background-size：规定背景图片的尺寸（cover：填充；100% 100%：拉伸）
  background-origin：规定背景图片的定位区域
  对于 background-origin 属性，有如下属性
  背景图片可以放置于 content-box、padding-box 或 border-box 区域

![img](https://raw.githubusercontent.com/Krryxa/WORK-LEARNING/master/images/25.jpg)

- 边框：
  border-radius：圆角
  box-shadow / text-shadow：阴影
  border-image：边框图片

### 文本效果

| 属性            | 描述                                                         |
| --------------- | ------------------------------------------------------------ |
| text-shadow     | 向文本添加阴影                                               |
| text-justify    | 规定当 text-align 设置为 “justify” 时所使用的对齐方法        |
| text-emphasis   | 向元素的文本应用重点标记以及重点标记的前景色                 |
| text-outline    | 规定文本的轮廓                                               |
| text-overflow   | 规定当文本溢出包含元素时发生的事情                           |
| text-wrap       | 规定文本的换行规则                                           |
| word-break      | 规定非中日韩文本的换行规则                                   |
| word-wrap       | 允许对长的不可分割的单词进行分割并换行到下一行               |
| text-decoration | 文本修饰符：overline、line-through、underline 分别是上划线、中划线、下划线 |

- @font-face 自定义字体
- 渐变，CSS3新增了渐变效果，包括 linear-gradient(线性渐变)和 radial-gradient(径向渐变)
  详看：<https://www.ainyi.com/krry_project>

### 2D/3D 转换

- 2D 转换（transform）

1. translate()：元素从其当前位置移动，根据给定的 left（x 坐标） 和 top（y 坐标） 位置参数。 transform: translate(50px, 100px);
2. rotate()：元素顺时针旋转给定的角度。若为负值，元素将逆时针旋转。transform: rotate(30deg);
3. scale()：元素的尺寸会增加或减少，根据给定的宽度（X 轴）和高度（Y 轴）参数，也可以一个值（宽高）。transform: scale(2,4);
4. skew()：元素翻转给定的角度，根据给定的水平线（X 轴）和垂直线（Y 轴）参数。transform: skew(30deg, 20deg);
5. matrix()： 把所有 2D 转换方法组合在一起，需要六个参数，包含数学函数，允许您：旋转、缩放、移动以及倾斜元素。transform:matrix(0.866,0.5,-0.5,0.866,0,0);

 

- 3D 转换

1. rotateX()：元素围绕其 X 轴以给定的度数进行旋转。transform: rotateX(120deg);
2. rotateY()：元素围绕其 Y 轴以给定的度数进行旋转。transform: rotateY(130deg);
3. perspective：规定 3D 元素的透视效果

### 动画、过渡

- 过渡效果（transition），使页面变化更平滑，以下参数可直接写在 transition 后面

1. transition-property ：执行动画对应的属性，例如 color，background 等，可以使用 all 来指定所有的属性。
2. transition-duration：过渡动画的一个持续时间。
3. transition-timing-function：在延续时间段，动画变化的速率，常见的有：ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier
4. transition-delay：延迟多久后开始动画

 

- 动画（animation）
  先定义 @keyframes 规则（0%，100% | from，to）
  然后定义 animation，以下参数可直接写在 animation 后面

1. animation-name: 定义动画名称
2. animation-duration: 指定元素播放动画所持续的时间长
3. animation-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(, , , )： 指元素根据时间的推进来改变属性值的变换速率，即动画的播放方式
4. animation-delay: 指定元素动画开始时间
5. animation-iteration-count: infinite | number：指定元素播放动画的循环次数
6. animation-direction: normal | alternate： 指定元素动画播放的方向，其只有两个值，默认值为normal，如果设置为 normal 时，动画的每次循环都是向前播放；另一个值是 alternate，规定动画在下一周期逆向地播放（来去播放）
7. animation-play-state: running | paused ：控制元素动画的播放状态

### 多列布局

通过CSS3，能够创建多个列来对文本进行布局

1. column-count: 规定元素应该被分隔的列数
2. column-gap: 规定列之间的间隔
3. column-rule: 设置列之间的宽度、样式和颜色规则

### 用户界面

CSS3中，新的用户界面特性包括重设元素尺寸、盒尺寸以及轮廓等

1. resize
2. box-sizing
3. outline-offset

resize 属性规定是否可由用户调整元素尺寸。如果希望此属性生效，需要设置元素的 overflow 属性，值可以是 auto、hidden 或 scroll

```
div {
  resize: both; /* none|both|horizontal|vertical; */
  overflow: auto;
}

```

box-sizing 属性可设置的值有 content-box、border-box 和 inherit
content-box 是W3C的标准盒模型，元素宽度 = 内容宽度 + padding + border：意思是 padding 和 border 会增加元素的宽度，以至于实际上的 width 大于原始设定的 width
border-box 是ie的怪异盒模型，元素宽度 = 设定的宽度，已经将 padding 和 border 包括进去了，比如有时候在元素基础上添加内距 padding 或 border 会将布局撑破，但是使用 border-box 就可以轻松完成
inherit：规定应从父元素继承 box-sizing 属性的值

outline-offset 属性对轮廓进行偏移，并在超出边框边缘的位置绘制轮廓

## CSS 兼容内核

-moz-：代表FireFox浏览器私有属性
-ms-：代表IE浏览器私有属性
-webkit-：代表safari、chrome浏览器私有属性
-o-：代表opera浏览器私有属性

 













