https://jingyan.baidu.com/article/90bc8fc85aa780f653640cb9.html

电脑蓝屏后重启后，我们首先应该去查一下“事件查看器”看看电脑故障，非正常关机的事件日志。如图点击此电脑右键-管理-进入计算机管理。

在计算机管理中点击系统工具下面的事件查看器。

在Windows日志中，查看系统日志，以时间为准，找到刚刚蓝屏重启那一刻所出现的错误日志。

若查看所有错误日志没有发现是非系统，其它软件造成的原因，那么我们还可以对Windows蓝屏时会自动生成一个转储DMP文件，这个文件一般都是默认保存在系统Windows目录下面。

我们可以直接搜索这个文件名MEMORY.DMP，但这个DMP文件在使用系统软件是无法打开的，需要使用到微软的Debugging Tools的分析工具来打开。

可以在百度中搜索Debugging Tools下载安装，需要注意的是：在执行Debugging Tools的Windbg.exe文件时需要以管理员身份执行。

打开Debugging Tools后，点击File-Open Crash Dump，选择Windows下面的MEMORY.DMP文件打开。

在故障检验分析Bugcheck Analysis中,出现ERROR错误，Module load completed but symbols could not be loaded for NETwew00.sys，NETwew00.sys文件不能被加载。可以判断是加载这个文件的时候导致蓝屏的。

这时我们可以将这个NETwew00.sys在百度中搜索一下相关资料，这是一个显卡的驱动的部件，那么可以试着找到解决这个Windows蓝屏的方法，当然这个过程很有可能不顺利，最终有可能还没有解决蓝屏问题，因为导致蓝屏的原因多种多样的。但至少在这个过程中也是一种学习。