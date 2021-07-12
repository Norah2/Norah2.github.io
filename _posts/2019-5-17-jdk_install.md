---
layout: post
title: jdk 安装教程  
date: 2019-05-17
description: jdk 安装教程
categories: Install
tags: Install Java SQLServer Jdk
author: NMt
mathjax: true
---
* content
{:toc}

有很多软件的适用于运行都需要基于Java的环境，这两天安装了SQL Server数据库就需要基于Java的环境，下面是安装教程：  


@@@@

{% raw %}
1. 打开装着jdk安装包的文件夹，双击：  
   [![W9lt61.png](https://z3.ax1x.com/2021/07/11/W9lt61.png)](https://imgtu.com/i/W9lt61)  
   
   [//]: # (![][pt_01])  
   
2. 出现安装向导界面，点击下一步：  
   [![W9lwTO.png](https://z3.ax1x.com/2021/07/11/W9lwTO.png)](https://imgtu.com/i/W9lwTO)  
   
   [//]: # (![][pt_02])  
   
3. 更改文件夹的路径，我选择安装在D盘：  
   [![W9lNOx.png](https://z3.ax1x.com/2021/07/11/W9lNOx.png)](https://imgtu.com/i/W9lNOx)
   
   [//]: # (![][pt_03])  
   
4. 更改之后的样子如下，点击下一步：  
   [![W9lam6.png](https://z3.ax1x.com/2021/07/11/W9lam6.png)](https://imgtu.com/i/W9lam6)
   
   [//]: # (![][pt_04])  
   
   **注：记下这个路径，后面需要配置系统环境。D:\Java\jdk1.8.0_131\\(我的是这个路径，你们记下你们安装的路径)**
5. 等待安装：  
   [![W9lYlR.png](https://z3.ax1x.com/2021/07/11/W9lYlR.png)](https://imgtu.com/i/W9lYlR)
   
   [//]: # (![][pt_05])  
   
6. 在刚安装目录的同一级新建一个jre1.8的文件夹：  
   [![W9ld0K.png](https://z3.ax1x.com/2021/07/11/W9ld0K.png)](https://imgtu.com/i/W9ld0K)
   
   [//]: # (![][pt_06])  
   
7. 将目标文件夹更改到刚刚新建的文件夹，如下所示：  
   [![W9lDte.png](https://z3.ax1x.com/2021/07/11/W9lDte.png)](https://imgtu.com/i/W9lDte)  
   [![W9lBkD.png](https://z3.ax1x.com/2021/07/11/W9lBkD.png)](https://imgtu.com/i/W9lBkD)  
   
   [//]: # (![][pt_07])  
   
   [//]: # (![][pt_08])  
   
8. 接下来点击下一步安装即可。
9. 现在开始配置环境，首先进入高级系统设置：  
   [![W9lrfH.png](https://z3.ax1x.com/2021/07/11/W9lrfH.png)](https://imgtu.com/i/W9lrfH)  
   
   [//]: # (![][pt_09])   
   
10. 点击环境变量：  
   [![W9lypd.png](https://z3.ax1x.com/2021/07/11/W9lypd.png)](https://imgtu.com/i/W9lypd)  
   
   [//]: # (![][pt_10])  
   
11. 点击新建：  
   [![W9l61A.png](https://z3.ax1x.com/2021/07/11/W9l61A.png)](https://imgtu.com/i/W9l61A)  
   
   [//]: # (![][pt_11])  
   
12. 变量名处写`JAVA_HOME`，变量值写第一次复制的安装路径，我的是`D:\Java\jdk1.8.0_131\`，点击确定。  
   [![W9lc6I.png](https://z3.ax1x.com/2021/07/11/W9lc6I.png)](https://imgtu.com/i/W9lc6I)  
   
   [//]: # (![][pt_12])  
   
13. 继续点击新建，变量名处写`CLASSPATH`，变量值写`%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;`  
   [![W9lgXt.png](https://z3.ax1x.com/2021/07/11/W9lgXt.png)](https://imgtu.com/i/W9lgXt)  
   
   [//]: # (![][pt_13])  
   
14. 在系统变量找到Path，双击进入，点击编辑文本：
   [![W9lf78.png](https://z3.ax1x.com/2021/07/11/W9lf78.png)](https://imgtu.com/i/W9lf78)  
   
   [//]: # (![][pt_14])   
   
15. 在变量值后面添加`%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;`  
   [![W9lRnP.png](https://z3.ax1x.com/2021/07/11/W9lRnP.png)](https://imgtu.com/i/W9lRnP)  
   
   [//]: # (![][pt_15])  
   
16. 完成之后全部都点击确定，否则它不会保存你的更改。打开cmd检查是否安装成功(win+R打开运行，输入cmd回车即可)：  
   [![W9l4AS.png](https://z3.ax1x.com/2021/07/11/W9l4AS.png)](https://imgtu.com/i/W9l4AS)   
   
   [//]: # (![][pt_16])  
   
17. 打开之后分别输入：`java -version`、`java`、`javac`，出现下述情况即是安装成功：  
   [![W9l5tg.png](https://z3.ax1x.com/2021/07/11/W9l5tg.png)](https://imgtu.com/i/W9l5tg)  
   [![W9lIhQ.png](https://z3.ax1x.com/2021/07/11/W9lIhQ.png)](https://imgtu.com/i/W9lIhQ)  
   [![W9lTpj.png](https://z3.ax1x.com/2021/07/11/W9lTpj.png)](https://imgtu.com/i/W9lTpj)  
   
   [//]: # (![][pt_17])  
   
   [//]: # (![][pt_18])
   
   [//]: # (![][pt_19])

转载请注明：[南梦婷的博客](https://norah2.github.io) » [点击阅读原文](https://norah2.github.io/2019/05/jdk_install/)   

<!--以下是本文用到的链接  

[pt_01]: /images/posts/jdk_install/01.png  
[pt_02]: /images/posts/jdk_install/02.png
[pt_03]: /images/posts/jdk_install/03.png
[pt_04]: /images/posts/jdk_install/04.png
[pt_05]: /images/posts/jdk_install/05.png
[pt_06]: /images/posts/jdk_install/06.png
[pt_07]: /images/posts/jdk_install/07.png
[pt_08]: /images/posts/jdk_install/08.png
[pt_09]: /images/posts/jdk_install/09.png
[pt_10]: /images/posts/jdk_install/10.png
[pt_11]: /images/posts/jdk_install/11.png  
[pt_12]: /images/posts/jdk_install/12.png
[pt_13]: /images/posts/jdk_install/13.png
[pt_14]: /images/posts/jdk_install/14.png
[pt_15]: /images/posts/jdk_install/15.png
[pt_16]: /images/posts/jdk_install/16.png
[pt_17]: /images/posts/jdk_install/17.png
[pt_18]: /images/posts/jdk_install/18.png
[pt_19]: /images/posts/jdk_install/19.png
[![W9lt61.png](https://z3.ax1x.com/2021/07/11/W9lt61.png)](https://imgtu.com/i/W9lt61)
[![W9lwTO.png](https://z3.ax1x.com/2021/07/11/W9lwTO.png)](https://imgtu.com/i/W9lwTO)
[![W9lNOx.png](https://z3.ax1x.com/2021/07/11/W9lNOx.png)](https://imgtu.com/i/W9lNOx)
[![W9lam6.png](https://z3.ax1x.com/2021/07/11/W9lam6.png)](https://imgtu.com/i/W9lam6)
[![W9lYlR.png](https://z3.ax1x.com/2021/07/11/W9lYlR.png)](https://imgtu.com/i/W9lYlR)
[![W9ld0K.png](https://z3.ax1x.com/2021/07/11/W9ld0K.png)](https://imgtu.com/i/W9ld0K)
[![W9lDte.png](https://z3.ax1x.com/2021/07/11/W9lDte.png)](https://imgtu.com/i/W9lDte)
[![W9lBkD.png](https://z3.ax1x.com/2021/07/11/W9lBkD.png)](https://imgtu.com/i/W9lBkD)
[![W9lrfH.png](https://z3.ax1x.com/2021/07/11/W9lrfH.png)](https://imgtu.com/i/W9lrfH)
[![W9lypd.png](https://z3.ax1x.com/2021/07/11/W9lypd.png)](https://imgtu.com/i/W9lypd)
[![W9l61A.png](https://z3.ax1x.com/2021/07/11/W9l61A.png)](https://imgtu.com/i/W9l61A)
[![W9lc6I.png](https://z3.ax1x.com/2021/07/11/W9lc6I.png)](https://imgtu.com/i/W9lc6I)
[![W9lgXt.png](https://z3.ax1x.com/2021/07/11/W9lgXt.png)](https://imgtu.com/i/W9lgXt)
[![W9lf78.png](https://z3.ax1x.com/2021/07/11/W9lf78.png)](https://imgtu.com/i/W9lf78)
[![W9lRnP.png](https://z3.ax1x.com/2021/07/11/W9lRnP.png)](https://imgtu.com/i/W9lRnP)
[![W9l4AS.png](https://z3.ax1x.com/2021/07/11/W9l4AS.png)](https://imgtu.com/i/W9l4AS)
[![W9l5tg.png](https://z3.ax1x.com/2021/07/11/W9l5tg.png)](https://imgtu.com/i/W9l5tg)
[![W9lIhQ.png](https://z3.ax1x.com/2021/07/11/W9lIhQ.png)](https://imgtu.com/i/W9lIhQ)
[![W9lTpj.png](https://z3.ax1x.com/2021/07/11/W9lTpj.png)](https://imgtu.com/i/W9lTpj)
-->

{% endraw %}