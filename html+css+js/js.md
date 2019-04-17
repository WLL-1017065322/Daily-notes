# js对象



## Array 对象

Array 对象用于在变量中存储多个值:

 var cars = ["Saab", "Volvo", "BMW"];

第一个数组元素的索引值为 0，第二个索引值为 1，以此类推。

### 数组属性

| 属性                                                         | 描述                             |
| :----------------------------------------------------------- | :------------------------------- |
| [constructor](http://www.runoob.com/jsref/jsref-constructor-array.html) | 返回创建数组对象的原型函数。     |
| [length](http://www.runoob.com/jsref/jsref-length-array.html) | 设置或返回数组元素的个数。       |
| [prototype](http://www.runoob.com/jsref/jsref-prototype-array.html) | 允许你向数组对象添加属性或方法。 |

### Array 对象方法

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [concat()](http://www.runoob.com/jsref/jsref-concat-array.html) | 连接两个或更多的数组，并返回结果。                           |
| [copyWithin()](http://www.runoob.com/jsref/jsref-copywithin.html) | 从数组的指定位置拷贝元素到数组的另一个指定位置中。           |
| [entries()](http://www.runoob.com/jsref/jsref-entries.html)  | 返回数组的可迭代对象。                                       |
| [every()](http://www.runoob.com/jsref/jsref-every.html)      | 检测数值元素的每个元素是否都符合条件。                       |
| [fill()](http://www.runoob.com/jsref/jsref-fill.html)        | 使用一个固定值来填充数组。                                   |
| [filter()](http://www.runoob.com/jsref/jsref-filter.html)    | 检测数值元素，并返回符合条件所有元素的数组。                 |
| [ find()](http://www.runoob.com/jsref/jsref-find.html)       | 返回符合传入测试（函数）条件的数组元素。                     |
|                                                              |                                                              |
| [ findIndex()](http://www.runoob.com/jsref/jsref-findindex.html) | 返回符合传入测试（函数）条件的数组元素索引。                 |
|                                                              |                                                              |
| [ forEach()](http://www.runoob.com/jsref/jsref-foreach.html) | 数组每个元素都执行一次回调函数。                             |
| [ from()](http://www.runoob.com/jsref/jsref-from.html)       | 通过给定的对象中创建一个数组。                               |
|                                                              |                                                              |
| [includes()](http://www.runoob.com/jsref/jsref-includes.html) | 判断一个数组是否包含一个指定的值。                           |
| [indexOf()](http://www.runoob.com/jsref/jsref-indexof-array.html) | 搜索数组中的元素，并返回它所在的位置。                       |
| [isArray()](http://www.runoob.com/jsref/jsref-isarray.html)  | 判断对象是否为数组。                                         |
| [join()](http://www.runoob.com/jsref/jsref-join.html)        | 把数组的所有元素放入一个字符串。                             |
| [keys()](http://www.runoob.com/jsref/jsref-keys.html)        | 返回数组的可迭代对象，包含原始数组的键(key)。                |
| [lastIndexOf()](http://www.runoob.com/jsref/jsref-lastindexof-array.html) | 返回一个指定的字符串值最后出现的位置，在一个字符串中的指定位置从后向前搜索。 |
| [map()](http://www.runoob.com/jsref/jsref-map.html)          | 通过指定函数处理数组的每个元素，并返回处理后的数组。         |
| [pop()](http://www.runoob.com/jsref/jsref-pop.html)          | 删除数组的最后一个元素并返回删除的元素。                     |
| [push()](http://www.runoob.com/jsref/jsref-push.html)        | 向数组的末尾添加一个或更多元素，并返回新的长度。             |
|                                                              |                                                              |
| [reduce()](http://www.runoob.com/jsref/jsref-reduce.html)    | 将数组元素计算为一个值（从左到右）。                         |
|                                                              |                                                              |
| [reduceRight()](http://www.runoob.com/jsref/jsref-reduceright.html) | 将数组元素计算为一个值（从右到左）。                         |
| [reverse()](http://www.runoob.com/jsref/jsref-reverse.html)  | 反转数组的元素顺序。                                         |
| [shift()](http://www.runoob.com/jsref/jsref-shift.html)      | 删除并返回数组的第一个元素。                                 |
| [slice()](http://www.runoob.com/jsref/jsref-slice-array.html) | 选取数组的的一部分，并返回一个新数组。                       |
| [some()](http://www.runoob.com/jsref/jsref-some.html)        | 检测数组元素中是否有元素符合指定条件。                       |
| [sort()](http://www.runoob.com/jsref/jsref-sort.html)        | 对数组的元素进行排序。                                       |
| [splice()](http://www.runoob.com/jsref/jsref-splice.html)    | 从数组中添加或删除元素。                                     |
| [toString()](http://www.runoob.com/jsref/jsref-tostring-array.html) | 把数组转换为字符串，并返回结果。                             |
| [unshift()](http://www.runoob.com/jsref/jsref-unshift.html)  | 向数组的开头添加一个或更多元素，并返回新的长度。             |
| [valueOf()](http://www.runoob.com/jsref/jsref-valueof-array.html) | 返回数组对象的原始值。                                       |



## Boolean 对象

### Boolean 对象属性 

| 属性                                                         | 描述                                  |
| :----------------------------------------------------------- | :------------------------------------ |
| [constructor](http://www.runoob.com/jsref/jsref-constructor-boolean.html) | 返回对创建此对象的 Boolean 函数的引用 |
| [prototype](http://www.runoob.com/jsref/jsref-prototype-boolean.html) | 使您有能力向对象添加属性和方法。      |

 

### Boolean 对象方法

| 方法                                                         | 描述                               |
| :----------------------------------------------------------- | :--------------------------------- |
| [toString()](http://www.runoob.com/jsref/jsref-tostring-boolean.html) | 把布尔值转换为字符串，并返回结果。 |
| [valueOf()](http://www.runoob.com/jsref/jsref-valueof-boolean.html) | 返回 Boolean 对象的原始值。        |



## Date 对象 

Date 对象用于处理日期与时间。

创建 Date 对象： **new Date()**

以下四种方法同样可以创建 Date 对象：

```javascript
var d = new Date();
var d = new Date(milliseconds);
var d = new Date(dateString);
var d = new Date(year, month, day, hours, minutes, seconds, milliseconds);
```

### Date 对象属性

| 属性                                       | 描述                                 |
| ------------------------------------------ | ------------------------------------ |
| [constructor](jsref-constructor-date.html) | 返回对创建此对象的 Date 函数的引用。 |
| [prototype](jsref-prototype-date.html)     | 使您有能力向对象添加属性和方法。     |

### Date 对象方法

| 方法                                                  | 描述                                                         |
| ----------------------------------------------------- | ------------------------------------------------------------ |
| [getDate()](jsref-getdate.html)                       | 从 Date 对象返回一个月中的某一天 (1 ~ 31)。                  |
| [getDay()](jsref-getday.html)                         | 从 Date 对象返回一周中的某一天 (0 ~ 6)。                     |
| [getFullYear()](jsref-getfullyear.html)               | 从 Date 对象以四位数字返回年份。                             |
| [getHours()](jsref-gethours.html)                     | 返回 Date 对象的小时 (0 ~ 23)。                              |
| [getMilliseconds()](jsref-getmilliseconds.html)       | 返回 Date 对象的毫秒(0 ~ 999)。                              |
| [getMinutes()](jsref-getminutes.html)                 | 返回 Date 对象的分钟 (0 ~ 59)。                              |
| [getMonth()](jsref-getmonth.html)                     | 从 Date 对象返回月份 (0 ~ 11)。                              |
| [getSeconds()](jsref-getseconds.html)                 | 返回 Date 对象的秒数 (0 ~ 59)。                              |
| [getTime()](jsref-gettime.html)                       | 返回 1970 年 1 月 1 日至今的毫秒数。                         |
| [getTimezoneOffset()](jsref-gettimezoneoffset.html)   | 返回本地时间与格林威治标准时间 (GMT) 的分钟差。              |
| [getUTCDate()](jsref-getutcdate.html)                 | 根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。              |
| [getUTCDay()](jsref-getutcday.html)                   | 根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。               |
| [getUTCFullYear()](jsref-getutcfullyear.html)         | 根据世界时从 Date 对象返回四位数的年份。                     |
| [getUTCHours()](jsref-getutchours.html)               | 根据世界时返回 Date 对象的小时 (0 ~ 23)。                    |
| [getUTCMilliseconds()](jsref-getutcmilliseconds.html) | 根据世界时返回 Date 对象的毫秒(0 ~ 999)。                    |
| [getUTCMinutes()](jsref-getutcminutes.html)           | 根据世界时返回 Date 对象的分钟 (0 ~ 59)。                    |
| [getUTCMonth()](jsref-getutcmonth.html)               | 根据世界时从 Date 对象返回月份 (0 ~ 11)。                    |
| [getUTCSeconds()](jsref-getutcseconds.html)           | 根据世界时返回 Date 对象的秒钟 (0 ~ 59)。                    |
| getYear()                                             | 已废弃。 请使用 getFullYear() 方法代替。                     |
| [parse()](jsref-parse.html)                           | 返回1970年1月1日午夜到指定日期（字符串）的毫秒数。           |
| [setDate()](jsref-setdate.html)                       | 设置 Date 对象中月的某一天 (1 ~ 31)。                        |
| [setFullYear()](jsref-setfullyear.html)               | 设置 Date 对象中的年份（四位数字）。                         |
| [setHours()](jsref-sethours.html)                     | 设置 Date 对象中的小时 (0 ~ 23)。                            |
| [setMilliseconds()](jsref-setmilliseconds.html)       | 设置 Date 对象中的毫秒 (0 ~ 999)。                           |
| [setMinutes()](jsref-setminutes.html)                 | 设置 Date 对象中的分钟 (0 ~ 59)。                            |
| [setMonth()](jsref-setmonth.html)                     | 设置 Date 对象中月份 (0 ~ 11)。                              |
| [setSeconds()](jsref-setseconds.html)                 | 设置 Date 对象中的秒钟 (0 ~ 59)。                            |
| [setTime()](jsref-settime.html)                       | setTime() 方法以毫秒设置 Date 对象。                         |
| [setUTCDate()](jsref-setutcdate.html)                 | 根据世界时设置 Date 对象中月份的一天 (1 ~ 31)。              |
| [setUTCFullYear()](jsref-setutcfullyear.html)         | 根据世界时设置 Date 对象中的年份（四位数字）。               |
| [setUTCHours()](jsref-setutchours.html)               | 根据世界时设置 Date 对象中的小时 (0 ~ 23)。                  |
| [setUTCMilliseconds()](jsref-setutcmilliseconds.html) | 根据世界时设置 Date 对象中的毫秒 (0 ~ 999)。                 |
| [setUTCMinutes()](jsref-setutcminutes.html)           | 根据世界时设置 Date 对象中的分钟 (0 ~ 59)。                  |
| [setUTCMonth()](jsref-setutcmonth.html)               | 根据世界时设置 Date 对象中的月份 (0 ~ 11)。                  |
| [setUTCSeconds()](jsref-setutcseconds.html)           | setUTCSeconds() 方法用于根据世界时 (UTC) 设置指定时间的秒字段。 |
| setYear()                                             | 已废弃。请使用 setFullYear() 方法代替。                      |
| [toDateString()](jsref-todatestring.html)             | 把 Date 对象的日期部分转换为字符串。                         |
| toGMTString()                                         | 已废弃。请使用 toUTCString() 方法代替。                      |
| [toISOString()](jsref-toisostring.html)               | 使用 ISO 标准返回字符串的日期格式。                          |
| [toJSON()](jsref-tojson.html)                         | 以 JSON 数据格式返回日期字符串。                             |
| [toLocaleDateString()](jsref-tolocaledatestring.html) | 根据本地时间格式，把 Date 对象的日期部分转换为字符串。       |
| [toLocaleTimeString()](jsref-tolocaletimestring.html) | 根据本地时间格式，把 Date 对象的时间部分转换为字符串。       |
| [toLocaleString()](jsref-tolocalestring.html)         | 据本地时间格式，把 Date 对象转换为字符串。                   |
| [toString()](jsref-tostring-date.html)                | 把 Date 对象转换为字符串。                                   |
| [toTimeString()](jsref-totimestring.html)             | 把 Date 对象的时间部分转换为字符串。                         |
| [toUTCString()](jsref-toutcstring.html)               | 根据世界时，把 Date 对象转换为字符串。                       |
| [UTC()](jsref-utc.html)                               | 根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。        |
| [valueOf()](jsref-valueof-date.html)                  | 返回 Date 对象的原始值。                                     |







## Math 对象

Math 对象用于执行数学任务。

Math 对象并不像 Date 和 String 那样是对象的类，因此没有构造函数 Math()。

## 语法

```javascript
var x = Math.PI; // 返回PI
 var y = Math.sqrt(16); // 返回16的平方根
```

### Math 对象属性

 

| 属性                                                      | 描述                                                    |
| :-------------------------------------------------------- | :------------------------------------------------------ |
| [E](http://www.runoob.com/jsref/jsref-e.html)             | 返回算术常量 e，即自然对数的底数（约等于2.718）。       |
| [LN2](http://www.runoob.com/jsref/jsref-ln2.html)         | 返回 2 的自然对数（约等于0.693）。                      |
| [LN10](http://www.runoob.com/jsref/jsref-ln10.html)       | 返回 10 的自然对数（约等于2.302）。                     |
| [LOG2E](http://www.runoob.com/jsref/jsref-log2e.html)     | 返回以 2 为底的 e 的对数（约等于 1.4426950408889634）。 |
| [LOG10E](http://www.runoob.com/jsref/jsref-log10e.html)   | 返回以 10 为底的 e 的对数（约等于0.434）。              |
| [PI](http://www.runoob.com/jsref/jsref-pi.html)           | 返回圆周率（约等于3.14159）。                           |
| [SQRT1_2](http://www.runoob.com/jsref/jsref-sqrt1-2.html) | 返回 2 的平方根的倒数（约等于 0.707）。                 |
| [SQRT2](http://www.runoob.com/jsref/jsref-sqrt2.html)     | 返回 2 的平方根（约等于 1.414）。                       |

 

### Math 对象方法

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [abs(x)](http://www.runoob.com/jsref/jsref-abs.html)         | 返回 x 的绝对值。                                            |
| [acos(x)](http://www.runoob.com/jsref/jsref-acos.html)       | 返回 x 的反余弦值。                                          |
| [asin(x)](http://www.runoob.com/jsref/jsref-asin.html)       | 返回 x 的反正弦值。                                          |
| [atan(x)](http://www.runoob.com/jsref/jsref-atan.html)       | 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。     |
| [atan2(y,x)](http://www.runoob.com/jsref/jsref-atan2.html)   | 返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。 |
| [ceil(x)](http://www.runoob.com/jsref/jsref-ceil.html)       | 对数进行上舍入。                                             |
| [cos(x)](http://www.runoob.com/jsref/jsref-cos.html)         | 返回数的余弦。                                               |
| [exp(x)](http://www.runoob.com/jsref/jsref-exp.html)         | 返回  Ex 的指数。                                            |
| [floor(x)](http://www.runoob.com/jsref/jsref-floor.html)     | 对 x 进行下舍入。                                            |
| [log(x)](http://www.runoob.com/jsref/jsref-log.html)         | 返回数的自然对数（底为e）。                                  |
| [max(x,y,z,...,n)](http://www.runoob.com/jsref/jsref-max.html) | 返回 x,y,z,...,n 中的最高值。                                |
| [min(x,y,z,...,n)](http://www.runoob.com/jsref/jsref-min.html) | 返回 x,y,z,...,n中的最低值。                                 |
| [pow(x,y)](http://www.runoob.com/jsref/jsref-pow.html)       | 返回 x 的 y 次幂。                                           |
| [random()](http://www.runoob.com/jsref/jsref-random.html)    | 返回 0 ~ 1 之间的随机数。                                    |
| [round(x)](http://www.runoob.com/jsref/jsref-round.html)     | 四舍五入。                                                   |
| [sin(x)](http://www.runoob.com/jsref/jsref-sin.html)         | 返回数的正弦。                                               |
| [sqrt(x)](http://www.runoob.com/jsref/jsref-sqrt.html)       | 返回数的平方根。                                             |
| [tan(x)](http://www.runoob.com/jsref/jsref-tan.html)         | 返回角的正切。                                               |





## Number 对象

Number 对象是原始数值的包装对象。

Number 创建方式 new Number()。

### 语法

 var num = new Number(value);

**注意：** 如果一个参数值不能转换为一个数字将返回 NaN 
(非数字值)。

### Number 对象属性

 

| 属性                                                         | 描述                                   |
| :----------------------------------------------------------- | :------------------------------------- |
| [constructor](http://www.runoob.com/jsref/jsref-constructor-number.html) | 返回对创建此对象的 Number 函数的引用。 |
| [MAX_VALUE](http://www.runoob.com/jsref/jsref-max-value.html) | 可表示的最大的数。                     |
| [MIN_VALUE](http://www.runoob.com/jsref/jsref-min-value.html) | 可表示的最小的数。                     |
| [NEGATIVE_INFINITY](http://www.runoob.com/jsref/jsref-negative-infinity.html) | 负无穷大，溢出时返回该值。             |
| [NaN](http://www.runoob.com/jsref/jsref-number-nan.html)     | 非数字值。                             |
| [POSITIVE_INFINITY](http://www.runoob.com/jsref/jsref-positive-infinity.html) | 正无穷大，溢出时返回该值。             |
| [prototype](http://www.runoob.com/jsref/jsref-prototype-num.html) | 允许您可以向对象添加属性和方法。       |

 

### Number 对象方法

| 方法                                                         | 描述                                                 |
| :----------------------------------------------------------- | :--------------------------------------------------- |
| [ isFinite ](http://www.runoob.com/jsref/jsref-isfinite-number.html) | 检测指定参数是否为无穷大。                           |
|                                                              |                                                      |
| [toExponential(x)](http://www.runoob.com/jsref/jsref-toexponential.html) | 把对象的值转换为指数计数法。                         |
| [toFixed(x)](http://www.runoob.com/jsref/jsref-tofixed.html) | 把数字转换为字符串，结果的小数点后有指定位数的数字。 |
| [toPrecision(x)](http://www.runoob.com/jsref/jsref-toprecision.html) | 把数字格式化为指定的长度。                           |
| [toString()](http://www.runoob.com/jsref/jsref-tostring-number.html) | 把数字转换为字符串，使用指定的基数。                 |
| [valueOf()](http://www.runoob.com/jsref/jsref-valueof-number.html) | 返回一个 Number 对象的基本数字值。                   |

###  ES6 新增 Number 属性 

 ES 6 增加了以下三个 Number 对象的属性：

- EPSILON: 表示 1 和比最接近 1 且大于 1 的最小 Number 之间的差别
- MIN_SAFE_INTEGER: 表示在 JavaScript中最小的安全的 integer 型数字 (`-(2^53 - 1)`)。
- MAX_SAFE_INTEGER: 表示在 JavaScript 中最大的安全整数（`2^53 - 1`）。



### ES6 新增 Number 方法 

 

ES 6 增加了以下两个 Number 对象的方法：  

- Number.isInteger(): 用来判断给定的参数是否为整数。
- Number.isSafeInteger(): 判断传入的参数值是否是一个"安全整数"。

Number.isInteger() 在参数是整数时返回 true。

Number.isSafeInteger()判断传入的参数值是否是一个"安全整数"。

安全整数范围为 `-(2^53 - 1)到` `2^53 - 1 `之间的整数，包含 `-(2^53 - 1)和` `2^53 - 1`。

## String 对象

String 对象用于处理文本（字符串）。

String 对象创建方法： **new String()**。

  

### 语法

 ```javascript
var txt = new String("string");
或者更简单方式：
var txt = "string";
 ```



### String 对象属性

| 属性                                                         | 描述                       |
| :----------------------------------------------------------- | :------------------------- |
| [constructor](http://www.runoob.com/jsref/jsref-constructor-string.html) | 对创建该对象的函数的引用   |
| [length](http://www.runoob.com/jsref/jsref-length-string.html) | 字符串的长度               |
| [prototype](http://www.runoob.com/jsref/jsref-prototype-string.html) | 允许您向对象添加属性和方法 |

 

### String 对象方法

| 方法                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [charAt()](http://www.runoob.com/jsref/jsref-charat.html)    | 返回在指定位置的字符。                                       |
| [charCodeAt()](http://www.runoob.com/jsref/jsref-charcodeat.html) | 返回在指定的位置的字符的 Unicode 编码。                      |
| [concat()](http://www.runoob.com/jsref/jsref-concat-string.html) | 连接两个或更多字符串，并返回新的字符串。                     |
| [fromCharCode()](http://www.runoob.com/jsref/jsref-fromcharcode.html) | 将 Unicode 编码转为字符。                                    |
| [indexOf()](http://www.runoob.com/jsref/jsref-indexof.html)  | 返回某个指定的字符串值在字符串中首次出现的位置。             |
| [includes()](http://www.runoob.com/jsref/jsref-string-includes.html) | 查找字符串中是否包含指定的子字符串。                         |
| [lastIndexOf()](http://www.runoob.com/jsref/jsref-lastindexof.html) | 从后向前搜索字符串，并从起始位置（0）开始计算返回字符串最后出现的位置。 |
| [match()](http://www.runoob.com/jsref/jsref-match.html)      | 查找找到一个或多个正则表达式的匹配。                         |
| [ repeat()](http://www.runoob.com/jsref/jsref-repeat.html)   | 复制字符串指定次数，并将它们连接在一起返回。                 |
| [replace()](http://www.runoob.com/jsref/jsref-replace.html)  | 在字符串中查找匹配的子串， 并替换与正则表达式匹配的子串。    |
| [search()](http://www.runoob.com/jsref/jsref-search.html)    | 查找与正则表达式相匹配的值。                                 |
| [slice()](http://www.runoob.com/jsref/jsref-slice-string.html) | 提取字符串的片断，并在新的字符串中返回被提取的部分。         |
| [split()](http://www.runoob.com/jsref/jsref-split.html)      | 把字符串分割为字符串数组。                                   |
| [startsWith()](http://www.runoob.com/jsref/jsref-startswith.html) | 查看字符串是否以指定的子字符串开头。                         |
| [substr()](http://www.runoob.com/jsref/jsref-substr.html)    | 从起始索引号提取字符串中指定数目的字符。                     |
| [substring()](http://www.runoob.com/jsref/jsref-substring.html) | 提取字符串中两个指定的索引号之间的字符。                     |
| [toLowerCase()](http://www.runoob.com/jsref/jsref-tolowercase.html) | 把字符串转换为小写。                                         |
| [toUpperCase()](http://www.runoob.com/jsref/jsref-touppercase.html) | 把字符串转换为大写。                                         |
| [trim()](http://www.runoob.com/jsref/jsref-trim.html)        | 去除字符串两边的空白                                         |
| [ toLocaleLowerCase()](http://www.runoob.com/jsref/jsref-tolocalelowercase.html) | 根据本地主机的语言环境把字符串转换为小写。                   |
| [ toLocaleUpperCase()](http://www.runoob.com/jsref/jsref-tolocaleuppercase.html) | 根据本地主机的语言环境把字符串转换为大写。                   |
| [valueOf()](http://www.runoob.com/jsref/jsref-valueof-string.html) | 返回某个字符串对象的原始值。                                 |
| [ toString()](http://www.runoob.com/jsref/jsref-tostring.html) | 返回一个字符串。                                             |

 

### String HTML 包装方法

HTML 返回包含在相对应的 HTML 标签中的内容。

以下方法并非标准方法，所以可能在某些浏览器下不支持。

| 方法                                                         | 描述                         |
| :----------------------------------------------------------- | :--------------------------- |
| [anchor()](http://www.runoob.com/jsref/jsref-anchor.html)    | 创建 HTML 锚。               |
| [big()](http://www.runoob.com/jsref/jsref-big.html)          | 用大号字体显示字符串。       |
| [blink()](http://www.runoob.com/jsref/jsref-blink.html)      | 显示闪动字符串。             |
| [bold()](http://www.runoob.com/jsref/jsref-bold.html)        | 使用粗体显示字符串。         |
| [fixed()](http://www.runoob.com/jsref/jsref-fixed.html)      | 以打字机文本显示字符串。     |
| [fontcolor()](http://www.runoob.com/jsref/jsref-fontcolor.html) | 使用指定的颜色来显示字符串。 |
| [fontsize()](http://www.runoob.com/jsref/jsref-fontsize.html) | 使用指定的尺寸来显示字符串。 |
| [italics()](http://www.runoob.com/jsref/jsref-italics.html)  | 使用斜体显示字符串。         |
| [link()](http://www.runoob.com/jsref/jsref-link.html)        | 将字符串显示为链接。         |
| [small()](http://www.runoob.com/jsref/jsref-small.html)      | 使用小字号来显示字符串。     |
| [strike()](http://www.runoob.com/jsref/jsref-strike.html)    | 用于显示加删除线的字符串。   |
| [sub()](http://www.runoob.com/jsref/jsref-sub.html)          | 把字符串显示为下标。         |
| [sup()](http://www.runoob.com/jsref/jsref-sup.html)          | 把字符串显示为上标。         |





## RegExp 对象



正则表达式是描述字符模式的对象。

正则表达式用于对字符串模式匹配及检索替换，是对字符串执行模式匹配的强大工具。

语法

```javascript
var patt=new RegExp(pattern,modifiers);

或者更简单的方式:

var patt=/pattern/modifiers; 
```

- pattern（模式） 描述了表达式的模式
- modifiers(修饰符) 用于指定全局匹配、区分大小写的匹配和多行匹配

 

> **注意：**当使用构造函数创造正则对象时，需要常规的字符转义规则（在前面加反斜杠 \）。比如，以下是等价的： 

```javascript
var re = new RegExp("\\w+");
var re = /\w+/;
```

### 修饰符

修饰符用于执行区分大小写和全局匹配:

| 修饰符 | 描述                                                     |
| ------ | -------------------------------------------------------- |
| [i]()  | 执行对大小写不敏感的匹配。                               |
| [g]()  | 执行全局匹配（查找所有匹配而非在找到第一个匹配后停止）。 |
| m      | 执行多行匹配。                                           |

### 方括号

方括号用于查找某个范围内的字符：

| 表达式                                   | 描述                               |
| ---------------------------------------- | ---------------------------------- |
| [[abc\]](jsref-regexp-charset.html)      | 查找方括号之间的任何字符。         |
| [[^abc\]](jsref-regexp-charset-not.html) | 查找任何不在方括号之间的字符。     |
| [0-9]                                    | 查找任何从 0 至 9 的数字。         |
| [a-z]                                    | 查找任何从小写 a 到小写 z 的字符。 |
| [A-Z]                                    | 查找任何从大写 A 到大写 Z 的字符。 |
| [A-z]                                    | 查找任何从大写 A 到小写 z 的字符。 |
| [adgk]                                   | 查找给定集合内的任何字符。         |
| [^adgk]                                  | 查找给定集合外的任何字符。         |
| (red\|blue\|green)                       | 查找任何指定的选项。               |

### 元字符

元字符（Metacharacter）是拥有特殊含义的字符：

| 元字符                                  | 描述                                        |
| --------------------------------------- | ------------------------------------------- |
| [.](jsref-regexp-dot.html)              | 查找单个字符，除了换行和行结束符。          |
| [\w](jsref-regexp-wordchar.html)        | 查找单词字符。                              |
| [\W](jsref-regexp-wordchar-non.html)    | 查找非单词字符。                            |
| [\d](jsref-regexp-digit.html)           | 查找数字。                                  |
| [\D](jsref-regexp-digit-non.html)       | 查找非数字字符。                            |
| [\s](jsref-regexp-whitespace.html)      | 查找空白字符。                              |
| [\S](jsref-regexp-whitespace-non.html)  | 查找非空白字符。                            |
| [\b](jsref-regexp-begin.html)           | 匹配单词边界。                              |
| [\B](jsref-regexp-begin-not.html)       | 匹配非单词边界。                            |
| \0                                      | 查找 NULL 字符。                            |
| [\n](jsref-regexp-newline.html)         | 查找换行符。                                |
| \f                                      | 查找换页符。                                |
| \r                                      | 查找回车符。                                |
| \t                                      | 查找制表符。                                |
| \v                                      | 查找垂直制表符。                            |
| [\xxx](jsref-regexp-octal.html)         | 查找以八进制数 xxx 规定的字符。             |
| [\xdd](jsref-regexp-hex.html)           | 查找以十六进制数 dd 规定的字符。            |
| [\uxxxx](jsref-regexp-unicode-hex.html) | 查找以十六进制数 xxxx 规定的 Unicode 字符。 |

### 量词

| 量词                                 | 描述                                                         |
| ------------------------------------ | ------------------------------------------------------------ |
| [n+](jsref-regexp-onemore.html)      | 匹配任何包含至少一个 n 的字符串。例如，/a+/ 匹配 "candy" 中的 "a"，"caaaaaaandy" 中所有的 "a"。 |
| [n*](jsref-regexp-zeromore.html)     | 匹配任何包含零个或多个 n 的字符串。例如，/bo*/ 匹配 "A ghost booooed" 中的 "boooo"，"A bird warbled" 中的 "b"，但是不匹配 "A goat grunted"。 |
| [n?](jsref-regexp-zeroone.html)      | 匹配任何包含零个或一个 n 的字符串。例如，/e?le?/ 匹配 "angel" 中的 "el"，"angle" 中的 "le"。 |
| [n{X}](jsref-regexp-nx.html)         | 匹配包含 X 个 n 的序列的字符串。例如，/a{2}/ 不匹配 "candy," 中的 "a"，但是匹配 "caandy," 中的两个 "a"，且匹配 "caaandy." 中的前两个 "a"。 |
| [n{X,}]()                            | X 是一个正整数。前面的模式 n 连续出现至少 X 次时匹配。 例如，/a{2,}/ 不匹配 "candy" 中的 "a"，但是匹配 "caandy" 和 "caaaaaaandy." 中所有的 "a"。 |
| [n{X,Y}](jsref-regexp-nxy.html)      | X 和 Y 为正整数。前面的模式 n 连续出现至少 X 次，至多 Y 次时匹配。例如，/a{1,3}/ 不匹配 "cndy"，匹配 "candy," 中的 "a"，"caandy," 中的两个 "a"，匹配 "caaaaaaandy" 中的前面三个 "a"。注意，当匹配 "caaaaaaandy" 时，即使原始字符串拥有更多的 "a"，匹配项也是 "aaa"。 |
| [n$](jsref-regexp-ndollar.html)      | 匹配任何结尾为 n 的字符串。                                  |
| [^n](jsref-regexp-ncaret.html)       | 匹配任何开头为 n 的字符串。                                  |
| [?=n](jsref-regexp-nfollow.html)     | 匹配任何其后紧接指定字符串 n 的字符串。                      |
| [?!n](jsref-regexp-nfollow-not.html) | 匹配任何其后没有紧接指定字符串 n 的字符串。                  |

### RegExp 对象方法

| 方法                                 | 描述                                               |
| ------------------------------------ | -------------------------------------------------- |
| [compile](jsref-regexp-compile.html) | 在 1.5 版本中已废弃。 编译正则表达式。             |
| [exec](jsref-exec-regexp.html)       | 检索字符串中指定的值。返回找到的值，并确定其位置。 |
| [test](jsref-test-regexp.html)       | 检索字符串中指定的值。返回 true 或 false。         |
| [toString]()                         | 返回正则表达式的字符串。                           |

### 支持正则表达式的 String 对象的方法

| 方法        | 描述                             | FF   | IE   |
| ----------- | -------------------------------- | ---- | ---- |
| [search]()  | 检索与正则表达式相匹配的值。     | 1    | 4    |
| [match]()   | 找到一个或多个正则表达式的匹配。 | 1    | 4    |
| [replace]() | 替换与正则表达式匹配的子串。     | 1    | 4    |
| [split]()   | 把字符串分割为字符串数组。       | 1    | 4    |

------

### RegExp 对象属性 

| 属性                                         | 描述                                               |
| -------------------------------------------- | -------------------------------------------------- |
| [constructor](jsref-regexp-constructor.html) | 返回一个函数，该函数是一个创建 RegExp 对象的原型。 |
| [global](jsref-regexp-global.html)           | 判断是否设置了 "g" 修饰符                          |
| [ignoreCase](jsref-regexp-ignorecase.html)   | 判断是否设置了 "i" 修饰符                          |
| [lastIndex](jsref-lastindex-regexp.html)     | 用于规定下次匹配的起始位置                         |
| [multiline]()                                | 判断是否设置了 "m" 修饰符                          |
| [source](jsref-source-regexp.html)           | 返回正则表达式的匹配模式                           |

## 全局属性和函数

JavaScript 全局属性和方法可用于创建Javascript对象。

### JavaScript 全局属性

| 属性                                                         | 描述                     |
| :----------------------------------------------------------- | :----------------------- |
| [Infinity](http://www.runoob.com/jsref/jsref-infinity.html)  | 代表正的无穷大的数值。   |
| [NaN](http://www.runoob.com/jsref/jsref-nan.html)            | 指示某个值是不是数字值。 |
| [undefined](http://www.runoob.com/jsref/jsref-undefined.html) | 指示未定义的值。         |

### JavaScript 全局函数 

| 函数                                                         | 描述                                               |
| :----------------------------------------------------------- | :------------------------------------------------- |
| [decodeURI()](http://www.runoob.com/jsref/jsref-decodeuri.html) | 解码某个编码的 URI。                               |
| [decodeURIComponent()](http://www.runoob.com/jsref/jsref-decodeuricomponent.html) | 解码一个编码的 URI 组件。                          |
| [encodeURI()](http://www.runoob.com/jsref/jsref-encodeuri.html) | 把字符串编码为 URI。                               |
| [encodeURIComponent()](http://www.runoob.com/jsref/jsref-encodeuricomponent.html) | 把字符串编码为 URI 组件。                          |
| [escape()](http://www.runoob.com/jsref/jsref-escape.html)    | 对字符串进行编码。                                 |
| [eval()](http://www.runoob.com/jsref/jsref-eval.html)        | 计算 JavaScript 字符串，并把它作为脚本代码来执行。 |
| [isFinite()](http://www.runoob.com/jsref/jsref-isfinite.html) | 检查某个值是否为有穷大的数。                       |
| [isNaN()](http://www.runoob.com/jsref/jsref-isnan.html)      | 检查某个值是否是数字。                             |
| [Number()](http://www.runoob.com/jsref/jsref-number.html)    | 把对象的值转换为数字。                             |
| [parseFloat()](http://www.runoob.com/jsref/jsref-parsefloat.html) | 解析一个字符串并返回一个浮点数。                   |
| [parseInt()](http://www.runoob.com/jsref/jsref-parseint.html) | 解析一个字符串并返回一个整数。                     |
| [String()](http://www.runoob.com/jsref/jsref-string.html)    | 把对象的值转换为字符串。                           |
| [unescape()](http://www.runoob.com/jsref/jsref-unescape.html) | 对由 escape() 编码的字符串进行解码。               |



# browser对象



## Window 对象

## Navigator 对象

## Screen 对象

## History 对象

## Location 对象



#  html dom对象



## HTML Document

## HTML Element

## HTML Attributes

## HTML Events



# html dom元素对象



## Anchor 对象

## Area 对象

## Base 对象

## Body 对象

## Button 对象

## Form 对象

## Frame/IFrame 对象

## Frameset 对象

## Image 对象

## Input Button 对象

## Input Checkbox 对象

## Input File 对象

## Input Hidden 对象

## Input Password 对象

## Input Radio 对象

## Input Reset 对象

## Input Submit 对象

## Input Text 对象

## Link 对象

## Meta 对象

## Object 对象

## Option 对象

## Select 对象

## Style 对象

## Table 对象

## td / th 对象

## tr 对象

## Textarea 对象