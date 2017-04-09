---
title: Nginx配置SSL实现Https访问
date: 2014-07-09 22:11:23
tags:
---
#### 生成根密钥
```
openssl genrsa -out ca.key 2048
/
openssl genrsa -out cakey.pem 2048
```
#### 生成根证书



```
openssl req -new -x509 -key ca.key -out ca.cert
/
openssl req -new -x509 -key cakey.pem -out cacert.pem
```



#### 生成服务器密钥

```
openssl genrsa -out server.key 2048
/
openssl genrsa -out server.pem 2048
```



#### 生成服务器请求

```
openssl req -new -key server.key -out server.csr
/
openssl req -new -key server.pem -out server.pem

执行上述命令后，需要输入信息。输入的信息中最重要的为 Common Name，这里输入的域名即为我们要使用https访问的域名。

127.0.0.1
/
localhost
/
iotcent.org
```


#### 私有CA根据请求来签署证书

```
# 默认openssl配置
openssl ca -in server.csr -out server.crt
/
openssl x509 -req -in server.csr -CA ca.crt -CAkey ca.key -CAcreateserial -out server.crt

```

#### Linux添加根证书

```

```
#### nginx配置

```
必选：
listen 127.0.0.1:443;
ssl on;
ssl_certificate ../ssl_crt/server.crt;
ssl_certificate_key ../ssl_crt/server.key;



可选：
#客户端能够重复使用存储在缓存中的会话参数时间 
ssl_session_timeout 5m; 
#指定使用的ssl协议  
ssl_protocols SSLv3 TLSv1;  
#指定许可的密码描述 
ssl_ciphers ALL:!ADH:!EXPORT56:RC4+RSA:+HIGH:+MEDIUM:+LOW:+SSLv2:+EXP;  
#SSLv3和TLSv1协议的服务器密码需求优先级高于客户端密码 
ssl_prefer_server_ciphers  on;
```


---
#### 内容参考：  
[基于OpenSSL自建CA和颁发SSL证书](https://segmentfault.com/a/1190000002569859)  
[Windows下Nginx配置SSL实现Https访问](http://www.cnblogs.com/developer-ios/p/6074665.html)  
