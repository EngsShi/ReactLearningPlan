# Nginx安装

## 安装

1. 安装程序

```
brew install nginx
```



2. 配置命令行

创建或修改 ~/.bash_profile，底部添加一行配置文件（需要根据安装的版本号修改地址）

```
export PATH=$PATH:/usr/local/Cellar/nginx/${此处是版本号}/bin/:
```

3. 执行并测试安装是否成功

```
nginx
```

打开网页 http://127.0.0.1:8080 测试服务是否正常启动



## 修改配置项

配置文件默认存储路径 `/usr/local/etc/nginx/nginx.conf`



1. 端口修改

```
listen       8080;
```

2. 反向代理

```
location /fs {
  proxy_pass  http://t.dh.yuexunedu.cn/fs;
}
```

3. 本地文件夹转发

```
location /file {
  alias    /Users/engs/Desktop/;
  autoindex   on; # 开启文件列表预览功能
}
```



## 常用命令

1. 测试配置文件是否正确

```
nginx -t
```

2. 重启服务

```
nginx -s reload
```

3. 关闭服务

```
nginx -s stop
```



## 日志

```
/usr/local/var/log/nginx/
```



