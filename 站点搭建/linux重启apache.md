# [linux 如何重启apache](https://www.cnblogs.com/hunchun/p/6116296.html)

```
查看apache2的命令 httpd -V
其中HTTPD_ROOT和SERVER_CONFIG_FILE  就可以确定httpd.conf的路径了

假设当前Linux用户的apahce安装目录为/usr/local/apache2，那么在命令行终端中使用以下命令启动，停止和重启apache。
1. 启动apahce的命令：
/usr/local/apache2/bin/apachectl start apache
2.  停止apache的命令：
/usr/local/apache2/bin/apachectl stop  
3.  重启apache的命令：
/usr/local/apache2/bin/apachectl restart 
要在重启 Apache 服务器时不中断当前的连接，则应运行：
/usr/local/sbin/apachectl graceful

如果当前用户的apache已经安装为linux的服务的话，可以使用以下命令进行以上操作。
1. 启动apache
service httpd start 
2. 停止服务apache
service httpd stop 
3. 重新启动apache
service httpd restart

Linux系统为Ubuntu
一、Start Apache 2 Server /启动apache服务
# /etc/init.d/apache2 start
or
$ sudo /etc/init.d/apache2 start
二、 Restart Apache 2 Server /重启apache服务
# /etc/init.d/apache2 restart
or
$ sudo /etc/init.d/apache2 restart
三、Stop Apache 2 Server /停止apache服务
# /etc/init.d/apache2 stop
or
$ sudo /etc/init.d/apache2 stop
```