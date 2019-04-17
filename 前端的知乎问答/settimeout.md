# 使用setTimeout，为什么下面这样写，都是大概每隔1s打印一个结果呢？

代码如下：



```text
for (let i = 0; i < 5; i++) {
    setTimeout(function() {
        console.log(i);
    }, i * 1000);
}
```

打印结果：

![img](https://pic1.zhimg.com/v2-4f07cdddd9b4e85be3c945ad435dd544_b.jpg)

提问：为什么这里动态设置setTimeout的延迟时间，效果确实大概1s打印出一个结果？如果想实现每隔0s,1s,2s,3s,4s打印一个结果，该如何修改代码呢？





先学好数学，你只需要知道三角数列的通项公式是 ![\frac{n\times(n+1)}{2}](https://www.zhihu.com/equation?tex=%5Cfrac%7Bn%5Ctimes%28n%2B1%29%7D%7B2%7D)

所以：

```js
for (let i = 0; i < 5; i++) {
    setTimeout(function() {
        console.log(i);
    }, (i * (i + 1) / 2) * 1000);
}
```

作者：紫云飞

链接：https://www.zhihu.com/question/277686094/answer/395059322

来源：知乎

著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。







其实这是个数学问题，相当于越往后需要等待的时间越长，下面是推导过程

A0 = 0

A1 = 1

A2 = A1+ 2

...

An-1 = An-2 + (n-1)

An = An-1 + n



左侧加起来 = 右侧加起来

去掉相同项

最后

An = 0 + 1+ 2 + ... + （n-1）+ n

​     = n(n+1)/2

作者：彭扬

链接：https://www.zhihu.com/question/277686094/answer/404286910

来源：知乎

著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。