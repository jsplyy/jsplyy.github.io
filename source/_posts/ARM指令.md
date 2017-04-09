---
title: ARM指令
date: 2017-04-09 22:15:18
tags:
---
#### __WFI

```

```
#### [MSR MRS指令详解](http://blog.csdn.net/wavemcu/article/details/6737302)

```
MSR = Move to Register from State register
MSR     PSP,R0
MRS     R0,PSP
```
#### PenSV

```

```
#### CPSID CPISE

#### CPS指令

```
CPSID   I   ;PRIMASK=1;关中断 
CPSIE   I   ;PRIMASK=0;开中断
CPSID   F   ;FAULTMASK=1;关异常
CPSIE   F   ;FAULTMASK=0;开异常
```


