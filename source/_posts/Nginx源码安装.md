---
title: Nginx源码安装
date: 2014-06-09 22:09:20
tags:
	- nginx
---
## nginx 源码安装

#### configure参数
```

./configure --user=nginx --group=nginx --prefix=/usr/local/nginx --with-http_ssl_module --add-module=../ngx_cache_purge-2.3 --with-pcre=/home/ubuntu/nginx_source/pcre-8.40 --with-zlib=/home/ubuntu/nginx_source/zlib-1.2.11 --with-http_stub_status_module --with-threads --with-http_sub_module --with-http_flv_module --with-http_gzip_static_module
```
#### 编译安装
```
sudo make && sudo make install

```
## nginx常用命令

#### 启动nginx
```
./nginx                          :正常启动

nginx -c /path/to/nginx.conf     ：指定配置文件

kill -HUP 主进程号               ：平滑重启
```

#### 关闭nginx
```
nginx -s stop  :快速停止nginx
         quit  ：完整有序的停止nginx

ps -ef | grep nginx

kill -QUIT 主进程号     ：从容停止Nginx
kill -TERM 主进程号     ：快速停止Nginx
pkill -9 nginx          ：强制停止Nginx
```


#### 查看nginx配置文件路径
```
sudo ./nginx -t
```

#### 查看nginx版本信息
```
sudo ./nginx -V
```
#### 修改配置后重新加载生效
```
nginx -s reload
```

## nginx 配置

#### 重定向缓存
```
rewrite 重定向，浏览器会缓存301永久重定向
```
#### [nginx配置location总结及rewrite规则写法](https://segmentfault.com/a/1190000002797606)
#### 反向代理配置 代理百度谷歌

```
proxy_pass
```

```
ngx_http_google_filter_module
```
