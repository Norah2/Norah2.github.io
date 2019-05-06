---
layout: post
title: Windows下安装selenium以及chrome driver的安装步骤  
description: 本文主要写关于selenium的前期安装工作
tag: python
---

今天介绍一下关于selenium的安装方法：  

### 确定chrome版本  

首先需要知道chrome的版本号，不同的版本对应不同版本的driver，如果版本号没有对应上会报错。  

1. 打开chrome，找到帮助选项卡，下拉框中有一个关于chrome的选项。  

   ![][pt_01]

  
2. 打开后就可以看见自己电脑上的chrome版本号，我的chrome版本号是74.0.3729.131  

   ![][pt_02]
  
  
3. [打开链接][link_chromedriver], 在其中找到和自己chrome对应版本号的chromedriver。我选择的是74.0.3729.6/，点击。    

   ![][pt_03]
  
   **注：一般一个版本的driver能够对应相近几个版本的chrome，所以选择邻近版本的chrome一般也可以，如果你没有在链接里面找到自己chrome的版本号可以自己查一下能够被哪个版本的driver兼容**  
  

4. 进入到这个下载界面，我的系统是Windows，所以选了第三个，你可以根据自己的系统进行选择。  

   ![][pt_04]

   **注：Windows系统好像只有32的driver，反正我用着没有出bug。（我电脑是64位的）**  
  

5. 下载之后解压  

    ![][pt_05]
  

6. 将解压之后的chromedriver.exe复制到路径`C:\Program Files (x86)\Google\Chrome\Application`下（我的需要管理员权限）。

   ![][pt_06]

### 安装selenium第三方包  

打开cmd，输入`pip install selenium`或`pip3 install selenium`  

### 测试代码  

**重启你的python编辑器(spyder or pychram or IDLE ect.)**  

一定要记得重启一下！！！  

打开编辑器之后，输入以下代码：  

```python
from selenium import webdriver
driver = webdriver.Chrome()
```

如果出现以下界面即使成功：

![][pt_07]

转载请注明：[南梦婷的博客](https://norah2.github.io) » [点击阅读原文](https://norah2.github.io/2019/05/selenium_install/)   

<!--以下是本文用到的链接-->  

[pt_01]: /images/posts/selenium_install/01.png
[pt_02]: /images/posts/selenium_install/02.png
[pt_03]: /images/posts/selenium_install/03.png
[pt_04]: /images/posts/selenium_install/04.png
[pt_05]: /images/posts/selenium_install/05.png
[pt_06]: /images/posts/selenium_install/06.png
[pt_07]: /images/posts/selenium_install/07.png
[link_chromedriver]: http://npm.taobao.org/mirrors/chromedriver/
