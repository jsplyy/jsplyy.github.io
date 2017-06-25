---
title: python trick
date: 2017-06-25 17:02:18
tags:
    - python
---
####if简写
'''
c = a if a>b else b
c = [b,a][a>b]
c = (a>b and [a] or [b])[0]
'''

####删除目录
```
shutil.rmtree(dir_name)
```
####字典访问
```
for key in dic:
for (k,v) in dic.items():
for k,v in dic.iteritems():
```