---
layout: post
title: Git 安装教程
date: 2019-03-02
categories: blog
tags: Git Install Software SSH Configure
---

* content
{:toc}

Git + SHH配置流程

{% raw %}

由于篇幅问题，这里又新写了一篇博客用作补充的，这里专门讲如何安装 Git ，外加配置 SSH。

## Git安装教程

由于我现在只在win10的操作系统上用过这个，就先只写windows上安装Git的详细过程。

1、先进入Git官网下载对应版本的Git安装包，跳过agree协议和修改安装路径的步骤。

2、选择安装组件，推荐全选

[//]: # ![](/images/posts/Git_install/01.png)
[![WS16ED.png](https://z3.ax1x.com/2021/07/10/WS16ED.png)](https://imgtu.com/i/WS16ED)

在我自己安装的时候底下会多出一个复选框，可能和我找到的这个教程版本不相同的原因，那个我没有勾。

[//]: # ![](/images/posts/Git_install/02.png)
[![WS1rDK.png](https://z3.ax1x.com/2021/07/10/WS1rDK.png)](https://imgtu.com/i/WS1rDK)

3、菜单文件夹 -- 默认

[//]: # ![](/images/posts/Git_install/03.png)
[![WS1Du6.png](https://z3.ax1x.com/2021/07/10/WS1Du6.png)](https://imgtu.com/i/WS1Du6)

4、修改系统的环境变量--建议选择上面两个。我选择的第一个

[//]: # ![](/images/posts/Git_install/04.png)
[![WS1sHO.png](https://z3.ax1x.com/2021/07/10/WS1sHO.png)](https://imgtu.com/i/WS1sHO)

5、SSH的证书的选择--我选的第一个

[//]: # ![](/images/posts/Git_install/05.png)
[![WS10jx.png](https://z3.ax1x.com/2021/07/10/WS10jx.png)](https://imgtu.com/i/WS10jx)

6、配置行尾结束符--我选的第三个

[//]: # ![](/images/posts/Git_install/06.png)
[![WS1g4H.png](https://z3.ax1x.com/2021/07/10/WS1g4H.png)](https://imgtu.com/i/WS1g4H)

说实话，我不太懂行尾结束符有什么用，但是我就这么配置了

[//]: # ![](/images/posts/Git_install/07.png)
[![WS1cUe.png](https://z3.ax1x.com/2021/07/10/WS1cUe.png)](https://imgtu.com/i/WS1cUe)

7、配置终端仿真

[//]: # ![](/images/posts/Git_install/08.png)
[![WS1hvt.png](https://z3.ax1x.com/2021/07/10/WS1hvt.png)](https://imgtu.com/i/WS1hvt)

*大多数其他Cygwin/MSYS终端一样，MinTTY也是基于pseudo终端("pty")设备的。但是MinTTY并不能完全替代windows的命令提示符。windows上自带简单的文本输出的原生态的命令提示符通常可以很好的工作，但交互性更好的诸如MinTTY这样的应用程序却可能出现故障——虽然通常都有应对方案。这就是为什么MinTTY不能完全替代windows自带的命令提示符。

8、其他的配置--默认

[//]: # ![](/images/posts/Git_install/09.png)
[![WS15KP.png](https://z3.ax1x.com/2021/07/10/WS15KP.png)](https://imgtu.com/i/WS15KP)

9、使用测试界面

[//]: # ![](/images/posts/Git_install/10.png)
[![WS1W8A.png](https://z3.ax1x.com/2021/07/10/WS1W8A.png)](https://imgtu.com/i/WS1W8A)

10、使用过程问题解决汇总--我没有出现这种问题

[//]: # ![](/images/posts/Git_install/11.png)
[![WS17VS.png](https://z3.ax1x.com/2021/07/10/WS17VS.png)](https://imgtu.com/i/WS17VS)

安装教程结束
------


## 配置SSH

1. 首先设置一下git的邮箱和用户名
输入以下两行命令：
```
git config --global user.email "your email"
git config --global user.name "your name"
```
**注：引号里面的请填写自己的邮箱和用户名**
2. 创建 SSH key

删除.ssh文件下的 known_hosts

git 输入命令：
```
$ ssh-keygen -t rsa -C "your@email.com"（请填你设置的邮箱地址）
```

接着出现：
```
Generating public/private rsa key pair.

Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):
```
请直接按下回车

然后系统会自动在.ssh文件夹下生成两个文件，id_rsa和id_rsa.pub，用记事本打开id_rsa.pub

windows 在 `C:\Users\username\.ssh\`  路径下有 `id_rsa` 和 `id_rsa.pub` 两个文件，`id_rsa.pub`文件中存储着 SSH 公钥。`id_rsa` 存储着私钥。

以上两个步骤整体流程如下图：
[//]: # ![](/images/posts/Git_install/14.jpg)
[![WS1ob8.jpg](https://z3.ax1x.com/2021/07/10/WS1ob8.jpg)](https://imgtu.com/i/WS1ob8)

3.登陆Github，打开“Accounting setting”，“SSH Keys”页面：

[//]: # ![](/images/posts/Git_install/12.png)
[![WS1fgI.png](https://z3.ax1x.com/2021/07/10/WS1fgI.png)](https://imgtu.com/i/WS1fgI)

点“Add Key”，你就应该看到已经添加的Key：

[//]: # ![](/images/posts/Git_install/13.png)
[![WS1IDf.png](https://z3.ax1x.com/2021/07/10/WS1IDf.png)](https://imgtu.com/i/WS1IDf)

------
由于 Git 是在很久之前配置的，因此图片大部分不是自己的，用的别人的，但是过程是自己的。如有错误，欢迎与我联系并指正~

转载请注明：[南梦婷的博客](https://norah2.github.io) » [点击阅读原文](https://norah2.github.io/2019/02/blog_github/) 

{% endraw %}