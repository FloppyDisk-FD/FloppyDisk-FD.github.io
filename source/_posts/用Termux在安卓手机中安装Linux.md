---
title: 用Termux在安卓手机中安装Linux
date: 2020-07-27 21:00:00
---
# 前言
Termux是一款安卓手机可用的终端，可以模拟一部分Linux操作，但并不是完整的Linux系统，所以我们今天来用Termux安装完整版的Linux发行版系统
# 准备工作

> 会打字
会粘贴复制
会用脑子


# 开始安装

PS:由于本人文笔有限，所以下面内容会出现一些别的博主的内容
Termux下载:[下载链接](https://f-droid.org/zh_Hans/packages/com.termux/ "下载链接")
Anlinux下载:[下载链接](https://f-droid.org/zh_Hans/packages/exa.lnx.a/ "下载链接")
1. 授予Termux文件访问权限，运行以下命令
    `termux-setup-storage`
2. 换源，一键命令
打开你的Termux
<img src="https://s1.ax1x.com/2020/06/28/Ngw86P.jpg" alt="Termux" border="0">

```
sed -i 's@^\(deb.*stable main\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/termux-packages-24 stable main@' $PREFIX/etc/apt/sources.list
    
sed -i 's@^\(deb.*games stable\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/game-packages-24 games stable@' $PREFIX/etc/apt/sources.list.d/game.list
    
sed -i 's@^\(deb.*science stable\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/science-packages-24 science stable@' $PREFIX/etc/apt/sources.list.d/science.list
    
pkg update
```

等待几秒就好了
3. 开始安装Linux
还记得Anlinux吗？对，我们接下来要用他来安装
首先你进来是这样的
<img src="https://s1.ax1x.com/2020/06/28/Ng0dHO.jpg" alt="Anlinux" border="0">
点击选择，选你想要的系统
这里我选择的是Ubuntu
<img src="https://s1.ax1x.com/2020/06/28/Ng02KP.jpg" alt="Ubuntu" border="0">
复制他给你的命令到Termux运行，安装过程略
安装好之后，该如何运行呢？
以Ubuntu为例
输入以下命令到Termux
`./start-ubuntu.sh`
<img src="https://s1.ax1x.com/2020/06/28/Ng0qK0.jpg" alt="Start Ubutnu" border="0">

------------


# 完成
