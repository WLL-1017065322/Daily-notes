阿里云搭建FTP服务器

要安装vsftp软件之前必须更新yum源。阿里云的帮助里写的比较烂，给了个链接地址，进去后可以下载一个软件，但是我下载了后不会用。每次执行yum install vsftpd -y都提示错误。

2
经过百度搜索，还是解决了，度娘还是很给力的。

yum check-update  检查可更新的所有软件包

我执行完这个命令后显示了一大片。我也看不懂，o(∩_∩)o 哈哈。

yum update  下载更新系统已经安装的软件包

执行后连续回答两个 y 就OK了

再执行yum install vsftpd -y 居然成功了

![阿里云搭建FTP服务器（非常适合新手）](https://imgsa.baidu.com/exp/w=500/sign=8b0847619f16fdfad86cc6ee848e8cea/4034970a304e251fb92d58b2a586c9177e3e53a5.jpg)]

配置Vsftpd

使用命令vi /etc/vsftpd/vsftpd.conf

这时候打开了该文件

第一次接触的时候注意光标

按INSERT键可以更改，左下角变成-- INSERT --

刚打开的时候并未显示完全，控制光标多往下走一段

需要修改的有几点

anonymous_enable=YES  禁止匿名访问

降YES改成NO

\#ascii_upload_enable 允许使用ascii码上传

\#ascii_download_enable 允许使用ascii码下载

去掉前面的“#”号

按ESC建，再输入“：”，发现左下角可以输入了

输入wq后按回车，配置完成。

修改shell配置，其实新的版本已经修改好了，无需再修改。

启动vsftpd： service vsftpd start

[![阿里云搭建FTP服务器（非常适合新手）](https://imgsa.baidu.com/exp/w=500/sign=8dd6ccdddb33c895a67e987be1127397/4bed2e738bd4b31c05f32ff185d6277f9f2ff8a9.jpg)](http://jingyan.baidu.com/album/afd8f4de4d6ea434e286e914.html?picindex=2)

[![阿里云搭建FTP服务器（非常适合新手）](https://imgsa.baidu.com/exp/w=500/sign=cf3bf264d01b0ef46ce8985eedc551a1/78310a55b319ebc4dcbcccd38026cffc1f1716b7.jpg)](http://jingyan.baidu.com/album/afd8f4de4d6ea434e286e914.html?picindex=3)

添加账户：useradd -p /alidata/www/wwwroot -s /sbin/nologin pwftp

然后修改密码：passwd pwftp

在输入密码的时候，不显示输入的内容，两次确认密码一致就可以了

这时候的vsftpd还得手动启动。

开机自动启动：chkconfig vsftpd on

重启阿里云，检查FTP是否正常。





Linux下添加FTP账号和服务器、增加密码和用户，更改FTP目录

1、 启动VSFTP服务器
A:cenos下运行:yum  install  vsftpd
B. 登录Linux主机后，运行命令：”service vsftpd start”
C. 要让FTP每次开机自动启动，运行命令:  “chkconfig --level 35 vsftpd on”

 

2、设置FTP权限
A. 编辑VSFTP配置文件，运行命令：”vi /etc/vsftpd/vsftpd.conf “
B. 将配置文件中”anonymous_enable=YES “改为 “anonymous_enable=NO”
C. 保存修改，按ESC键，运行命令：“：wq”

这样关闭了匿名登录功能。

 

3、添加FTP账号
A. 登录Linux主机后，运行命令：”useradd ftpadmin -s /sbin/nologin “。该账户路径默认指向/home/ftpadmin目录；如果需要将用户指向其他目录，请运行命令：useradd ftpadmin -s /sbin/nologin –d /www(其他目录)
B. 设置ftpadmin用户密码，运行命令：”passwd ftpadmin” ; 输入两次密码，匹配成功后，就设置好了ftpadmin用户的密码了。
C.测试连接，您可以在“我的电脑”地址栏中输入 ftp://IP 来连接FTP服务器，根据提示输入账户密码。

 

4、FTP数据传输注意事项?
A. 尽量把文件打包后上传。Linux无法识别RAR压缩包，可以使用ZIP压缩。
B.上传数据时请选择二进制编码，如果选择其他编码，可能会导致上传的压缩包无法打开。