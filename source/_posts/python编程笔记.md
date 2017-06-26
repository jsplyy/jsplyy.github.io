---
title: python编程笔记
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
####日期
```
datetime.datetime.now().strftime('__%Y_%m_%d__%H_%M_%S')
```
####glob
```
*,?,[]这三个通配符，*代表0个或多个字符，?代表一个字符，[]匹配指定范围内的字符，如[0-9]匹配数字
>>> import glob
>>> glob.glob('./[0-9].*')
['./1.gif', './2.txt']
>>> glob.glob('*.gif')
['1.gif', 'card.gif']
>>> glob.glob('?.gif')
['1.gif']
glob.glob('*.back')
```
####os.path
```
os.path.split(os.path.realpath(__file__))[0]
```