---
title: 镜像文件vmdk和cdi格式相互转化
date: 2017-07-03 21:54:51
tags:
    - 虚拟机
---
#### vmdk转vdi
```
vBoxManage.exe clonehd MachinesUbuntuUbuntu.vmdkUbuntu.vdi --format VDI
```
#### vdi转vmdk
```
vBoxVBoxManage.exe clonehd Ubuntu.vmdk Ubuntu.vdi --format VDI
```