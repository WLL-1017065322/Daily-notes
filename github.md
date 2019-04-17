怎么传文件：

自从使用github以来，一直都是在[github网站](https://link.jianshu.com?t=https://github.com/)在线上传文件到仓库中，但是有时因为网络或者电脑的原因上传失败。最重要的原因是我习惯本地编辑，完成以后再一起上传github。看过了几个教程，总结出最适合自己的比较简单的方法。



两种方法上传本地文件到github

#### 1. github在线上传文件夹

在线上传也可以上传完整的文件夹结构，直接拖拽到上传文件页面的框中即可。

##### 1.1点击上传文件



![img](https:////upload-images.jianshu.io/upload_images/3067059-3dc3ff655f5826e9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/985)

点击上传

##### 1.2 直接拖拽

直接拖拽即可上传文件夹及文件夹里面的文件。如果点击* choose your files *就只能上传单个文件。



![img](https:////upload-images.jianshu.io/upload_images/3067059-1433fee4d699a53e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/981)

直接拖拽





#### 2. 通过git工具上传本地文件夹（本地项目）

##### 2.1 下载[git工具](https://link.jianshu.com?t=https://git-scm.com/downloads) 



![img](https:////upload-images.jianshu.io/upload_images/3067059-0ff2c754d4888bb4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/989)

选择对应版本下载

##### 2.2 下载完成后安装完成，注意在安装过程中可以选择创建桌面快捷方式



![img](https:////upload-images.jianshu.io/upload_images/3067059-fa7d131432a1232e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/503)

桌面快捷方式

##### 2.3 绑定用户

打开git-bash.exe（直接在桌面上点击右键，或者点击开始按钮找到Git Bash）



![img](https:////upload-images.jianshu.io/upload_images/3067059-a232cbd6d250296e.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/592)

运行gitBash.gif

在打开的GIt Bash中输入以下命令（用户和邮箱为你github注册的账号和邮箱）

```
$ git config --global user.name "hanyuntao"
$ git config --global user.email "hanyuntaocn@163.com"
```



![img](https:////upload-images.jianshu.io/upload_images/3067059-f2c6c88dca3cb4f1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/514)

Paste_Image.png

##### 2.4 设置SSH key（[git中sshkey有何作用？](https://link.jianshu.com?t=https://segmentfault.com/q/1010000000118744)）

###### 2.4.1 生成ssh key

首先检查是否已生成密钥`cd ~/.ssh`，如果返回的`ls`有3个文件,则密钥已经生成。



![img](https:////upload-images.jianshu.io/upload_images/3067059-18adb5b6ca265756.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/274)

密钥生成

如果没有密钥，则通过

```
$ ssh-keygen -t rsa -C "hanyuntaocn@163.com"
```

生成，生成过程中一路按3次回车键就好了。（默认路径，默认没有密码登录）
 生成成功后，去对应目录C:\Users\hyt.ssh里（hyt为电脑用户名，每个人不同）用记事本打开id_rsa.pub，得到ssh key公钥。



![img](https:////upload-images.jianshu.io/upload_images/3067059-ef6cb51d5ad31445.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/569)

ssh key公钥

###### 2.4.2 为github账号配置ssh key

切换到github，展开个人头像的小三角，点击settings，然后打开SSH keys菜单， 点击Add SSH key新增密钥，填上标题（最好跟本地仓库保持一致）。



![img](https:////upload-images.jianshu.io/upload_images/3067059-1aba5aba10165470.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000)

设置sshkey.gif

接着将id_rsa.pub文件中key粘贴到此，最后Add key生成密钥吧。\

#### 2.5 上传本地项目到github

##### 2.5.1 创建一个本地项目

这是我自己创建的几个文件夹及文件。



![img](https:////upload-images.jianshu.io/upload_images/3067059-2a5f6b6ff4ae9c95.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/558)

本地项目

##### 2.5.2 建立本地仓库

1.首先进入text文件夹

```
cd d:text
```



![img](https:////upload-images.jianshu.io/upload_images/3067059-2b398f0122f722cb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/257)

首先进入text文件夹

2.执行指令：`git init`



![img](https:////upload-images.jianshu.io/upload_images/3067059-71817641532ad828.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/352)

执行git init

初始化成功后你会发现项目里多了一个隐藏文件夹.git



![img](https:////upload-images.jianshu.io/upload_images/3067059-ac953ff8977c72db.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/738)

隐藏的文件夹

3.执行指令：`git add .`
 将所有文件添加到仓库



![img](https:////upload-images.jianshu.io/upload_images/3067059-fd5b779ebc45f4ba.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/318)

执行git add .

4.执行指令：`git commit -m "提交文件"`
 双引号内是提交注释。



![img](https:////upload-images.jianshu.io/upload_images/3067059-b4be356b146b06ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/312)

提交文件

##### 2.5.3 关联github仓库

1.到github text仓库复制仓库地址





![img](https:////upload-images.jianshu.io/upload_images/3067059-29c5089e9fd4b637.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000)

复制仓库地址

 2.执行指令：

```
git remote add origin https://github.com/hanyuntao/text.git
```





![img](https:////upload-images.jianshu.io/upload_images/3067059-eeaf4b58df1f142f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/455)

执行指令

##### 2.5.4 上传本地代码

执行指令：`git push -u origin master`



![img](https:////upload-images.jianshu.io/upload_images/3067059-22f6fe754c8e3267.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/437)

执行指令

##### 2.5.5完成了

可以看到我们的本地项目已经上传到了github上了。



![img](https:////upload-images.jianshu.io/upload_images/3067059-2b4264842851800a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000)

完成了

** 注意：git是不能管理空的文件夹的，文件夹里必须有文件才能上传。 **

参考资料：[git中sshkey有何作用？](https://link.jianshu.com?t=https://segmentfault.com/q/1010000000118744)

作者：hanyuntao

链接：https://www.jianshu.com/p/c70ca3a02087

来源：简书

简书著作权归作者所有，任何形式的转载都请联系作者获得授权并注明出处。













问题：