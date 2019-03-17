---
layout: post
title: 查看电脑的密钥
description: 升级时做个备份，以防万一。
tag: Windows
---

1. `win+R`打开运行，输入`regedit`用以打开注册表  
   ![][pt_01]

2. 依次展开：HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> Windows NT -> CurrentVersion：  
   ![][pt_02]

3. 单击SoftwareProtectionPlatform，右侧找到BackupProductKeyDefault双击则可看到激活密钥：  
   ![][pt_03]

参考文献：  
https://jingyan.baidu.com/article/f3e34a12f361f9f5ea653574.html  

转载请注明：[南梦婷的博客](https://norah2.github.io) » [点击阅读原文](https://norah2.github.io/2019/03/view_keys/) 

<!--本文用到的链接-->
[pt_01]: /images/posts/view_keys/01.png  
[pt_02]: /images/posts/view_keys/02.png  
[pt_03]: /images/posts/view_keys/03.png  


