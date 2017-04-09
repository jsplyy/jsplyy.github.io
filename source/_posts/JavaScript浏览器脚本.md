---
title: JavaScript浏览器脚本
date: 2013-06-09 22:06:44
tags:
---

#### 把网页转换成编辑模式

```
javascript:document.body.contentEditable='true'; document.designMode='on'; void(0);
```


#### 旋转网页
```
javascript:window.i=1;setInterval(function(){i++;document.body.style.cssText+="-webkit-transform: rotate(-"+i+"deg);-moz-transform: rotate(-"+i+"deg)";},100);void(0);
```

#### 不显示图片
```
jannick='';for%20(i7M1bQz=0;i7M1bQz<document.images.length;i7M1bQz++){jannick+='<img%20src='+document.images[i7M1bQz].src+'><br>'};if(jannick!=''){document.write('<center>'+jannick+'</center>');void(document.close())}else{alert('No%20images!')}
```

#### 显示网页中非图片元素
```
for(jannick=0;jannick<document.images.length;jannick++){void(document.images[jannick].style.visibility='hidden')}
```


#### 解除复制限制
```
with(document.body){oncontextmenu='';ondragstart='';onselectstart='';onselect='';oncopy='';onbeforecopy='';onmouseup='';}void(0);
```

#### 解除网页中的一些禁止功能 如复制/粘贴，右键等
```
javascript<img src="static/image/smiley/default/sad.gif" border="0" smilieid="2" alt=":(">function(e,f,w,d,b,i){for(i=0;i<e.length;)(t=e,w=d=b=f);})(['onmousedown','onmouseup','onmousemove','ondblclick','onclick','oncontextmenu','onmousewheel','onselectstart','oncopy','onkeydown','onkeypress','onkeyup'],new Function,window,document,document.body);
```

#### 密码框密文变明文--无效--待修改
```
(function(){var s,F,j,f,i;s="";F=document.forms;for(j=0;j<F.length;++j){f=F;for(i=0;i<f.length;++i){if(f.type.toLowerCase()=="password")s+=f.value+"\n";}}if(s)alert("Passwords in forms on this page:\n\n"+s);else alert("There are no passwords in forms on this page.");})();
```


#### 查看网站更新时间
```
javascript:alert(document.lastModified)
```
