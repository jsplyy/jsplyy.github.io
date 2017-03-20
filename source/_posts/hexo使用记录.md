---
title: hexo配置记录
---

``` 
被酒莫惊春睡重，赌书消得泼茶香，当时只道是寻常
```
<!-- more -->

### deploy

```
type: git #注意,这边是git不是github,hexo 3.0以后就要求使用git,不然会出现deploy失败情况.  
repo: git@github.com:Helloxyw/Helloxyw.github.io.git  
branch: master

npm install hexo-deployer-git --save  
```

### 换maupassant主题
```
$ git clone https://github.com/tufu9441/maupassant-hexo.git themes/maupassant

$ npm install hexo-renderer-jade --save
$ npm install hexo-renderer-sass --save
```

### 命令
```
hexo clean
hexo generate
hexo d/deploy

hexo d -g

hexo s/server
```

### 安装hexo
```
安装node.js

设置npm镜像--
npm config set registry "https://registry.npm.taobao.org"

配置git
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub注册邮箱"
ssh-keygen -t rsa -C "你的GitHub注册邮箱"

安装hexo
npm install hexo / npm install hexo-cli g
hexo init blog
cd blog
hexo generate
```


### git同时push到多个仓库 oschina github coding
```
$ git remote add <主机名> <网址>
$ git pull <远程主机名> <远程分支名>:<本地分支名>
$ git push <远程主机名> <本地分支名>:<远程分支名>

```