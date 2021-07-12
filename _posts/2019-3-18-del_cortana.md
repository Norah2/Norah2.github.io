---
layout: post
title: 分开小娜和搜索功能  
date: 2019-03-18
description: win10将小娜和搜索功能合并了，导致很多不必要的麻烦。本文就是解决这个问题的。 
categories: Windows  
tags: Windows Setting
author: NMt
mathjax: true
---

* content
{:toc}

从最初接触win10就不喜欢小娜这个功能，但是一直因为里面有个搜索功能甚得我心，小娜就一直安安稳稳待在我的任务栏上。直到这一天，想找个快捷键打开搜索功能结果阴差阳错get到小娜的快捷键，我就实在忍无可忍想干掉它（一按就开始放语音严重影响我听歌），事实证明我成功了。  

@@@@


{% raw %}
1. `win+R`打开运行，输入`gpedit.msc`，按回车。  
   [![W9AC6g.png](https://z3.ax1x.com/2021/07/11/W9AC6g.png)](https://imgtu.com/i/W9AC6g)
   
   [//]: # (![][pt_01])  
   
   **注：win10家庭版没有这里的`gpedit.msc`功能。若想要继续则参考：[win10升级专业版][win10]**  
   
2. 点击 ‘管理模板’->'Windows组件'->搜索  
   [![W9APXQ.png](https://z3.ax1x.com/2021/07/11/W9APXQ.png)](https://imgtu.com/i/W9APXQ)
   
   [//]: # (![][pt_02])  
   
3. 在搜索里找到'允许使用Cortana'  
   [![W9AFmj.png](https://z3.ax1x.com/2021/07/11/W9AFmj.png)](https://imgtu.com/i/W9AFmj)
   
   [//]: # (![][pt_03])  
   
4. 双击后弹出新窗口，将选项改为'已禁用'，点确定即可。  
   [![W9A91S.png](https://z3.ax1x.com/2021/07/11/W9A91S.png)](https://imgtu.com/i/W9A91S)
   
   [//]: # (![][pt_04])  


参考文献：  
http://www.windows10zj.com/win10school/5291.html  

转载请注明：[南梦婷的博客](https://norah2.github.io) » [点击阅读原文](https://norah2.github.io/2019/03/del_cortana/)   

<!--本文中用到的链接  
[pt_01]: /images/posts/del_cortana/01.png
[pt_02]: /images/posts/del_cortana/02.png
[pt_03]: /images/posts/del_cortana/03.png
[pt_04]: /images/posts/del_cortana/04.png
[![W9AC6g.png](https://z3.ax1x.com/2021/07/11/W9AC6g.png)](https://imgtu.com/i/W9AC6g)
[![W9APXQ.png](https://z3.ax1x.com/2021/07/11/W9APXQ.png)](https://imgtu.com/i/W9APXQ)
[![W9AFmj.png](https://z3.ax1x.com/2021/07/11/W9AFmj.png)](https://imgtu.com/i/W9AFmj)
[![W9A91S.png](https://z3.ax1x.com/2021/07/11/W9A91S.png)](https://imgtu.com/i/W9A91S)
-->

[win10]: https://norah2.github.io/2019/03/win10_upgrate/

{% endraw %}