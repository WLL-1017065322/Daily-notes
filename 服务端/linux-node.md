1 官网下载包:

linux x64

2 上传到linux 解压tar,xz 文件

$xz -d ***.**tar.xz**

$tar -xvf  ***.tar

3 环境配置

/home/admin  /root 里的.bashrc 添加 PATH=$PATH:/usr/local/node/bin

4 测试版本  node -v

5 安装cnpm

```
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
```

　　安装完之后，安装模块的命令就变为：

```
$ cnpm install [name]
```

　　同步模块命令为：

```
$ cnpm sync connect
```

