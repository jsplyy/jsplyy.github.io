---
title: IAR配置
date: 2017-04-09 22:14:53
tags:
---
#### 汇编包含头文件
```
option->assembler->Preprocessor
```
#### Run to main

```
project->options->debugger->setup 中勾选 run to main 选项
```
#### icf文件

```

```
#### map文件

```

```

#### [ARM中PC和LR的关系 ](http://blog.sina.com.cn/s/blog_932ba3b90101mlh8.html)

```
LR = PC -4
```

#### SWI中断

```

```

#### ARM工作模式

```
用户模式，FIQ模式，IRQ模式，系统模式，终止模式，数据访问终止模式，未定义模式
```

#### IAR call_graph

```

```

#### objdump反汇编

```
objdump -f test  显示test的文件头信息

objdump -d test  反汇编test中的需要执行指令的那些section

objdump -D test  与-d类似，但反汇编test中的所有section

objdump -h test  显示test的Section Header信息

objdump -x test  显示test的全部Header信息

objdump -s test  除了显示test的全部Header信息，还显示他们对应的十六进制文件代码
```
#### SVC指令

```

```
#### 输出汇编文件

```
Option->C/C++ Compile->List->Output assemble file
```
#### 生成call graph log file

```
Option->Linker->Extra Options->Command line options:
--log call_graph
--log_file log.txt
```

#### entry symbol
```
Option->Linker->Library->override default program entry->entry symbol
```
