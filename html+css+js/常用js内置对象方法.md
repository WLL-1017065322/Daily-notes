# js常用内置对象及方法		 

在js中万物皆对象；字符串，数组，数值，函数......

内置对象都有自己的属性和方法，访问方法如下：

对象名.属性名称；

对象名.方法名称



## 1.Array数组对象

##### unshift( )    数组开头增加

功能：给数组开头增加一个或多个

参数：一个或多个

返回值：数组的长度

原数组发生改变

 

##### shift( )        数组开头删除一项

功能：给数组开头删除一个

参数：无

返回值：被删除的内容

原数组发生改变

 

##### push( )       数组末尾增加

功能：给数组末尾增加一项或多项

参数：一个或多个

返回值：数组的长度

原数组发生改变

 

##### pop( )         数组末尾删除一项

功能：给数组末未删除一项

参数：无

返回值：被删除的内容

原数组发生改变

 

##### concat( )     数组的拼接

ary1.concat( ary2,ary3....)

使用concat可以实现数组的克隆，concat（）中不传参数

![img](https://images2017.cnblogs.com/blog/1173217/201708/1173217-20170801115400161-1410889865.png)

![img](https://images2017.cnblogs.com/blog/1173217/201708/1173217-20170801122839974-1316628368.png)

 

##### splice（index, *howmany, item1, ...itemx*）

splice 可以根据参数实现数组的删除，增加，替换

前两个参数 index 和 *howmany 是必需的参数，后面的参数可选参数*

 

splice（index,  0 ，item1， item2...)     增加

从索引 index 开始增加，增加的内容插入到索引 index 前面

 

splice(index, n)    删除

从索引 index 开始删除n个，如果只有一个参数splice（index），就是从索引  index  开始后面的内容全部删除

 

splice（index， n，item1，item2...）   替换

从索引 index开始替换 n 个，替换的内容为item1, item2....

 

##### slice（n，m）      截取

从索引 n 截取到索引 m 但不包括 m  ，原数组不发生改变

slice（0）或splice（）可以实现数组的克隆

 

**reverse（）     数组翻转**

返回值是翻转后的新数组，原数组发生改变

 

##### sort（）    数组排序

使用方法：sort（function （a，b）{return  a-b}）     从小到大排

​               sort（function （a，b）{return  b-a}）     从大到小排

 

##### toString( )   数组转字符串

把数组转成以逗号分隔的字符串

 

##### join（拼接形式）    拼接

把数组拼接成以其他形式分割的字符串，配合eval（）可以实现数学运算        eval（join（‘+’））

 

##### 数组常用但不兼容的方法：

##### indexOf（查找内容）   查找

ary.indexOf（查找内容）    查找数组中是否有某项，有的话返回该项的所引，没有话返回-1；

 

#####  

##### forEach（）  遍历

```
forEach接收两个参数，一个callback，thisArg
callback接收三个参数：1）item 2）index 3）input
thisArg用来改变callback中的this指向；
forEach 没有返回值，但是map有返回值
```

 

##### map（）   遍历

 

## 2.string字符串

##### **charAT（index）**      

通过索引找字符

 

##### **charCodeAt（index）**      

通过索引找到字符的 Unicode 编码。这个返回值是 0 - 65535 之间的整数。

 方法 charCodeAt() 与 charAt() 方法执行的操作相似，只不过前者返回的是位于指定位置的字符的编码，而后者返回的是字符子串。

 

##### **indexOf（）**      

从前往后找，找到返回内容的索引，找不到返回-1；

 

##### **lastIndexOf（）**     

 从后往前找，找到返回内容的索引，找不到返回-1；

 

##### **slice（n，m）**       

从索引n 查找到索引m  但不包括m，slice可以取负值

 

##### **substring（n，m）**      

从索引n 查找到索引m ，但不包括m， 不可以取负值

 

##### **substr（n，m）**      

从索引n开始截取m 个

 

##### **split（切割形式）**     

  把一个字符串分割成字符串数组。

 

##### **toUpperCase（）**      

转大写字母

 

##### **toLowerCase（）**      

 转小写字母

 

## 3.Math对象

**Math.floor（）**        向下取整

 

**Math.ceil（）**         向上取整

 

**Math.random（）**      取0-1之间的随机小数

 

**Math.round（）**     四舍五入

 

**Math.abs（）**      取绝对值

 

**Math.pow（x，y）**      x的y次幂  

 

**Math.sqrt（）**     开平方

 

**Math.max（）**      取最大值

 

**Math.min（）**      取最小值

 

## 4.Date日期对象

**new Date（）**      创建一个日期对象

 

**getFullYear（）**      返回年份

 

**getMonth（）**      返回月份数（0-11），想要得到几月，需要加一

 

**getDay（）**      返回一周的第几天（0-6），想要得到星期几，需要加一

 

**getDate（）**      返回日

 

**getHours（）**      返回时

 

**getMinutes（）**      返回分

 

**getSeconds（）**      返回秒

 

**getTime（）**      返回从1970年1月1日00：00到现在的毫秒数（格林尼治时间），也就是时间戳

 

**setYear(yearInt)**       设置年份.2位数或4位数 


**setFullYear(yearInt)**      设置年份.4位数 

 

**setMonth(monthInt)**       设置月份(0-11) 


**setDate(dateInt)**       设置日(1-31) 


**setHours(hourInt)**       设置小时数(0-23) 


**setMinutes(minInt)**       设置分钟数(0-59) 


**setSeconds(secInt)**       设置秒数(0-59) 


**setMilliseconds(milliInt)**       设置毫秒(0-999) 