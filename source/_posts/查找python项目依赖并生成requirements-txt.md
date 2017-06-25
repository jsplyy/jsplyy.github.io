---
title: 查找python项目依赖并生成requirements.txt
date: 2017-06-25 15:49:36
tags:
    - python
---
####使用pip freeze
```
pip freeze > requirements.txt
```
这种方式配合virtualenv 才好使，否则把整个环境中的包都列出来了。

####使用 pipreqs
```
pipreqs ./
```
这个工具的好处是可以通过对项目目录的扫描，自动发现使用了那些类库，自动生成依赖清单。
缺点是可能会有些偏差，需要检查并自己调整下。