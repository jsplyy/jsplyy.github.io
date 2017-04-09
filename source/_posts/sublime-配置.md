---
title: sublime 配置
date: 2017-04-09 22:13:21
tags:
---
### 添加ctags快捷键
ctags -R -f .tags  
Preferences -> Key Bindings -> Users  

```
[  
    {"command": "navigate_to_definition","keys": ["f12"]}, 
    {"command": "jump_prev","keys": ["f8"]}
]
```



### 修改TAB键为缩进为四个空格
Preferences -> Settings -> Users
```
{
    // 注意只有一个大括号，如果之前有属性，如在之前的属性前确保有 ，(逗号)
    "tab_size": 4,
    "translate_tabs_to_spaces": true, 
    //若要在保存时自动把tab 转换成空格，请把下面一行设置成 true，如不需要: 设置成 false
    "expand_tabs_on_save": true
}
```
