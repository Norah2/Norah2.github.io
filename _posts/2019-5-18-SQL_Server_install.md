---
layout: post
title: SQL Server 安装教程  
date: 2019-05-18
description: sql server 的安装教程
categories: Install 
tags: Install SQLServer DataBase
author: NMt
mathjax: true
---

* content
{:toc}

这两天安装了个数据库，就顺便写个教程，数据库是SQL server。安装环境是Windows server 10。    


@@@@


{% raw %}
如果需要安装sql server全部功能则需要先安装jdk，jdk的安装教程请移步我的另一篇文章：[jdk安装教程](https://norah2.github.io/2019/05/jdk_install)  

在安装jdk的基础之上开始安装我们的数据库~  

1. 先将iso后缀的文件进行解压，打开解压后的文件夹点击setup：  
    
	[//]: # (![][pt_01])  
	[![W90NP1.png](https://z3.ax1x.com/2021/07/11/W90NP1.png)](https://imgtu.com/i/W90NP1)
	
2. 点击左边的安装选项卡，再点击“全新SQL Server独立安装或向现有安装添加功能”   
    
	[//]: # (![][pt_02])  
	[![W90Y5R.png](https://z3.ax1x.com/2021/07/11/W90Y5R.png)](https://imgtu.com/i/W90Y5R)
	
3. 填写产品密钥，点击下一步：  
    
	[//]: # (![][pt_03])  
	[![W90GVJ.png](https://z3.ax1x.com/2021/07/11/W90GVJ.png)](https://imgtu.com/i/W90GVJ)
	
4. 点击接受许可条款，点击下一步：
    
	[//]: # (![][pt_04])  
	[![W90a26.png](https://z3.ax1x.com/2021/07/11/W90a26.png)](https://imgtu.com/i/W90a26)
	
5. 点击下一步：
    
	[//]: # (![][pt_05])  
	[![W90Ja9.png](https://z3.ax1x.com/2021/07/11/W90Ja9.png)](https://imgtu.com/i/W90Ja9)  
	
6. 点击下一步：
    
	[//]: # (![][pt_06])  
	[![W90U8x.png](https://z3.ax1x.com/2021/07/11/W90U8x.png)](https://imgtu.com/i/W90U8x)
	
7. 点击下一步：  
    
	[//]: # (![][pt_07])  
	[![W900KO.png](https://z3.ax1x.com/2021/07/11/W900KO.png)](https://imgtu.com/i/W900KO)
	
8. 等待，点击下一步:  
    
	[//]: # (![][pt_08])  
	[![W90dxK.png](https://z3.ax1x.com/2021/07/11/W90dxK.png)](https://imgtu.com/i/W90dxK)
	
9. 点击下一步：  
    
	[//]: # (![][pt_09])  
	[![WP9xEt.png](https://z3.ax1x.com/2021/07/12/WP9xEt.png)](https://imgtu.com/i/WP9xEt)  
	
10. 点击全选，安装路径可以改成自己喜欢的，我直接改到了D盘，改好点击下一步：  
    
	[//]: # (![][pt_10])  
    [![WP9zUP.png](https://z3.ax1x.com/2021/07/12/WP9zUP.png)](https://imgtu.com/i/WP9zUP)  
	   
    但是我这一步出现了报错，PolyBase的检查不通过，点击查看原因如下： 
	
	[//]: # (![][pt_11])  
	[![WP9XDA.png](https://z3.ax1x.com/2021/07/12/WP9XDA.png)](https://imgtu.com/i/WP9XDA)  
	
    百度之后说是需要安装JRE 7，只能是7，装8也不行，下载地址：[http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)  
	
	[//]: # (![][pt_12])  
	[//]: # (![][pt_13])  
	[![WP9Oud.png](https://z3.ax1x.com/2021/07/12/WP9Oud.png)](https://imgtu.com/i/WP9Oud)  
	[![WP9jHI.png](https://z3.ax1x.com/2021/07/12/WP9jHI.png)](https://imgtu.com/i/WP9jHI)  
	
	我安装之后还是不行，可能是没装上吧，于是我就暴力解决，直接不安装这个功能，在上一步中取消勾选“针对外部数据的PolyBase查询服务”：  
	
	[//]: # (![][pt_14])  
	[![WPC9C8.png](https://z3.ax1x.com/2021/07/12/WPC9C8.png)](https://imgtu.com/i/WPC9C8)  
	
11. 点击下一步：  
    
	[//]: # (![][pt_15])  
	[![WPCS4f.png](https://z3.ax1x.com/2021/07/12/WPCS4f.png)](https://imgtu.com/i/WPCS4f)
	
12. 点击下一步：
    
	[//]: # (![][pt_16])  
	[![WPCC8S.png](https://z3.ax1x.com/2021/07/12/WPCC8S.png)](https://imgtu.com/i/WPCC8S)
	
13. 点击“添加当前用户”，再点击下一步：  
    
	[//]: # (![][pt_17])   
	[![WPCPgg.png](https://z3.ax1x.com/2021/07/12/WPCPgg.png)](https://imgtu.com/i/WPCPgg)
	
14. 点击“添加当前用户”，再点击下一步：  
    
	[//]: # (![][pt_18])  
	[![WPCivQ.png](https://z3.ax1x.com/2021/07/12/WPCivQ.png)](https://imgtu.com/i/WPCivQ)
	
15. 勾选第一个和第三个：  
    
	[//]: # (![][pt_19])  
	[![WPCADs.png](https://z3.ax1x.com/2021/07/12/WPCADs.png)](https://imgtu.com/i/WPCADs)
	
16. 点击“添加当前用户”，再点击下一步：  
    
	[//]: # (![][pt_20])  
	[![WPCkuj.png](https://z3.ax1x.com/2021/07/12/WPCkuj.png)](https://imgtu.com/i/WPCkuj)
	
17. 更改工作目录进和结果目录，可选择自己喜欢的文件夹。  
    
	[//]: # (![][pt_21])  
	[![WPCeU0.png](https://z3.ax1x.com/2021/07/12/WPCeU0.png)](https://imgtu.com/i/WPCeU0)
	
18. 点击“接受”，下一步:  
    
	[//]: # (![][pt_22])  
	[![WPCZEq.png](https://z3.ax1x.com/2021/07/12/WPCZEq.png)](https://imgtu.com/i/WPCZEq)
	
19. 出现以下界面，等待即可：  
    
	[//]: # (![][pt_23])  
	[![WPCEbn.png](https://z3.ax1x.com/2021/07/12/WPCEbn.png)](https://imgtu.com/i/WPCEbn)
	
20. 安装完成之后点击确定：  
    
	[//]: # (![][pt_24])  
	[![WPCK8U.png](https://z3.ax1x.com/2021/07/12/WPCK8U.png)](https://imgtu.com/i/WPCK8U)
	
21. 从开始界面点击“Reporting Services配置管理器”  
    
	[//]: # (![][pt_25])  
	[![WPCm5V.png](https://z3.ax1x.com/2021/07/12/WPCm5V.png)](https://imgtu.com/i/WPCm5V)
	
22. 点击连接：  
    
	[//]: # (![][pt_26])  
	[![WPCuCT.png](https://z3.ax1x.com/2021/07/12/WPCuCT.png)](https://imgtu.com/i/WPCuCT)
	
23. 这里的状态应该是启动状态，如果不是，则手动点击启动：  
    
	[//]: # (![][pt_27])  
	[![WPCM2F.png](https://z3.ax1x.com/2021/07/12/WPCM2F.png)](https://imgtu.com/i/WPCM2F)
	
24. 在开始里找到“SQL Server 2016 Data Quality Server”, 点击：  
    
	[//]: # (![][pt_28])  
	[![WPCQv4.png](https://z3.ax1x.com/2021/07/12/WPCQv4.png)](https://imgtu.com/i/WPCQv4)
	
25. 出现“是否要继续？[是/否]”，打一个“是”即可：  
    
	[//]: # (![][pt_29])  
	[![WPC1KJ.png](https://z3.ax1x.com/2021/07/12/WPC1KJ.png)](https://imgtu.com/i/WPC1KJ)
	
26. 接下来它会让你输出密码，密码长度至少8个字符，大小写字母、特殊字符、数字至少出现3种。确认一遍密码即可：  
    
	[//]: # (![][pt_30])  
	[![WPC8bR.png](https://z3.ax1x.com/2021/07/12/WPC8bR.png)](https://imgtu.com/i/WPC8bR)
	
26. 出现点击任意键继续，就随意按一下键盘就好了。  
    
	[//]: # (![][pt_31])  
	[![WPCJV1.png](https://z3.ax1x.com/2021/07/12/WPCJV1.png)](https://imgtu.com/i/WPCJV1)
	
27. 从开始点击“SQL Server 2016 Data Quality Cli...”  
    
	[//]: # (![][pt_33])  
	[![WPCYUx.png](https://z3.ax1x.com/2021/07/12/WPCYUx.png)](https://imgtu.com/i/WPCYUx)
	
28. 点击下拉箭头，选择“LOCAL”, 点击连接:  
    
	[//]: # (![][pt_35])  
    [//]: # (![][pt_32])  
	[![WPCUPK.png](https://z3.ax1x.com/2021/07/12/WPCUPK.png)](https://imgtu.com/i/WPCUPK)  
	[![WPC3r9.png](https://z3.ax1x.com/2021/07/12/WPC3r9.png)](https://imgtu.com/i/WPC3r9)  
	
29. 出现下述界面就是安装成功了：  
    
	[//]: # (![][pt_34])   
	[![WPCt56.png](https://z3.ax1x.com/2021/07/12/WPCt56.png)](https://imgtu.com/i/WPCt56)  



转载请注明：[南梦婷的博客](https://norah2.github.io) » [点击阅读原文](https://norah2.github.io/2019/05/SQL_Server_install/)   

<!--以下是本文用到的链接  

[pt_01]: /images/posts/SQL_Server_install/01.png
[pt_02]: /images/posts/SQL_Server_install/02.png
[pt_03]: /images/posts/SQL_Server_install/03.png
[pt_04]: /images/posts/SQL_Server_install/04.png
[pt_05]: /images/posts/SQL_Server_install/05.png
[pt_06]: /images/posts/SQL_Server_install/06.png
[pt_07]: /images/posts/SQL_Server_install/07.png
[pt_08]: /images/posts/SQL_Server_install/08.png
[pt_09]: /images/posts/SQL_Server_install/09.png
[pt_10]: /images/posts/SQL_Server_install/10.png
[pt_11]: /images/posts/SQL_Server_install/11.png
[pt_12]: /images/posts/SQL_Server_install/12.png
[pt_13]: /images/posts/SQL_Server_install/13.png
[pt_14]: /images/posts/SQL_Server_install/14.png
[pt_15]: /images/posts/SQL_Server_install/15.png
[pt_16]: /images/posts/SQL_Server_install/16.png
[pt_17]: /images/posts/SQL_Server_install/17.png
[pt_18]: /images/posts/SQL_Server_install/18.png
[pt_19]: /images/posts/SQL_Server_install/19.png
[pt_20]: /images/posts/SQL_Server_install/20.png
[pt_21]: /images/posts/SQL_Server_install/21.png
[pt_22]: /images/posts/SQL_Server_install/22.png
[pt_23]: /images/posts/SQL_Server_install/23.png
[pt_24]: /images/posts/SQL_Server_install/24.png
[pt_25]: /images/posts/SQL_Server_install/25.png
[pt_26]: /images/posts/SQL_Server_install/26.png
[pt_27]: /images/posts/SQL_Server_install/27.png
[pt_28]: /images/posts/SQL_Server_install/28.png
[pt_29]: /images/posts/SQL_Server_install/29.png
[pt_30]: /images/posts/SQL_Server_install/30.png
[pt_31]: /images/posts/SQL_Server_install/31.png
[pt_32]: /images/posts/SQL_Server_install/32.png
[pt_33]: /images/posts/SQL_Server_install/33.png
[pt_34]: /images/posts/SQL_Server_install/34.png
[pt_35]: /images/posts/SQL_Server_install/35.png
[![W90NP1.png](https://z3.ax1x.com/2021/07/11/W90NP1.png)](https://imgtu.com/i/W90NP1)
[![W90Y5R.png](https://z3.ax1x.com/2021/07/11/W90Y5R.png)](https://imgtu.com/i/W90Y5R)
[![W90GVJ.png](https://z3.ax1x.com/2021/07/11/W90GVJ.png)](https://imgtu.com/i/W90GVJ)
[![W90a26.png](https://z3.ax1x.com/2021/07/11/W90a26.png)](https://imgtu.com/i/W90a26)
[![W90Ja9.png](https://z3.ax1x.com/2021/07/11/W90Ja9.png)](https://imgtu.com/i/W90Ja9)
[![W90U8x.png](https://z3.ax1x.com/2021/07/11/W90U8x.png)](https://imgtu.com/i/W90U8x)
[![W900KO.png](https://z3.ax1x.com/2021/07/11/W900KO.png)](https://imgtu.com/i/W900KO)
[![W90dxK.png](https://z3.ax1x.com/2021/07/11/W90dxK.png)](https://imgtu.com/i/W90dxK)
[![WP9xEt.png](https://z3.ax1x.com/2021/07/12/WP9xEt.png)](https://imgtu.com/i/WP9xEt)
[![WP9zUP.png](https://z3.ax1x.com/2021/07/12/WP9zUP.png)](https://imgtu.com/i/WP9zUP)
[![WP9XDA.png](https://z3.ax1x.com/2021/07/12/WP9XDA.png)](https://imgtu.com/i/WP9XDA)
[![WP9Oud.png](https://z3.ax1x.com/2021/07/12/WP9Oud.png)](https://imgtu.com/i/WP9Oud)
[![WP9jHI.png](https://z3.ax1x.com/2021/07/12/WP9jHI.png)](https://imgtu.com/i/WP9jHI)
[![WPC9C8.png](https://z3.ax1x.com/2021/07/12/WPC9C8.png)](https://imgtu.com/i/WPC9C8)
[![WPCS4f.png](https://z3.ax1x.com/2021/07/12/WPCS4f.png)](https://imgtu.com/i/WPCS4f)
[![WPCC8S.png](https://z3.ax1x.com/2021/07/12/WPCC8S.png)](https://imgtu.com/i/WPCC8S)
[![WPCPgg.png](https://z3.ax1x.com/2021/07/12/WPCPgg.png)](https://imgtu.com/i/WPCPgg)
[![WPCivQ.png](https://z3.ax1x.com/2021/07/12/WPCivQ.png)](https://imgtu.com/i/WPCivQ)
[![WPCADs.png](https://z3.ax1x.com/2021/07/12/WPCADs.png)](https://imgtu.com/i/WPCADs)
[![WPCkuj.png](https://z3.ax1x.com/2021/07/12/WPCkuj.png)](https://imgtu.com/i/WPCkuj)
[![WPCeU0.png](https://z3.ax1x.com/2021/07/12/WPCeU0.png)](https://imgtu.com/i/WPCeU0)
[![WPCZEq.png](https://z3.ax1x.com/2021/07/12/WPCZEq.png)](https://imgtu.com/i/WPCZEq)
[![WPCEbn.png](https://z3.ax1x.com/2021/07/12/WPCEbn.png)](https://imgtu.com/i/WPCEbn)
[![WPCK8U.png](https://z3.ax1x.com/2021/07/12/WPCK8U.png)](https://imgtu.com/i/WPCK8U)
[![WPCm5V.png](https://z3.ax1x.com/2021/07/12/WPCm5V.png)](https://imgtu.com/i/WPCm5V)
[![WPCuCT.png](https://z3.ax1x.com/2021/07/12/WPCuCT.png)](https://imgtu.com/i/WPCuCT)
[![WPCM2F.png](https://z3.ax1x.com/2021/07/12/WPCM2F.png)](https://imgtu.com/i/WPCM2F)
[![WPCQv4.png](https://z3.ax1x.com/2021/07/12/WPCQv4.png)](https://imgtu.com/i/WPCQv4)
[![WPC1KJ.png](https://z3.ax1x.com/2021/07/12/WPC1KJ.png)](https://imgtu.com/i/WPC1KJ)
[![WPC8bR.png](https://z3.ax1x.com/2021/07/12/WPC8bR.png)](https://imgtu.com/i/WPC8bR)
[![WPCJV1.png](https://z3.ax1x.com/2021/07/12/WPCJV1.png)](https://imgtu.com/i/WPCJV1)
[![WPC3r9.png](https://z3.ax1x.com/2021/07/12/WPC3r9.png)](https://imgtu.com/i/WPC3r9)
[![WPCYUx.png](https://z3.ax1x.com/2021/07/12/WPCYUx.png)](https://imgtu.com/i/WPCYUx)
[![WPCt56.png](https://z3.ax1x.com/2021/07/12/WPCt56.png)](https://imgtu.com/i/WPCt56)
[![WPCUPK.png](https://z3.ax1x.com/2021/07/12/WPCUPK.png)](https://imgtu.com/i/WPCUPK)
-->

{% endraw %}
