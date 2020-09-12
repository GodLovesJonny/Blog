---
title: "BLWL[2] Manjaro Xfce桌面背景替换"
date: 2020-01-23T22:24:58+08:00
categories: ["Better Life With Linux"]
tags: ["Manjaro", "Linux"]
draft: false
---

新机子一开始想也装 KDE 桌面版，然而独显驱动似乎配置上出了什么问题，看了一些资料捣鼓了两天仍然未见成效  
主要是 KDE 桌面的画面撕裂问题，暂时没找到好的解决办法  
(问题已解决，参看 [BLWL07](http://jonathanwayy.xyz/2020/blwl7/)）  
于是出于时间和效率的考量换用了 XFCE 桌面版，目前十分丝滑尚未遇到任何问题  
   
换桌面背景很简单  
先推荐两个背景图片来源：  

	http://wallpaperswide.com/  
	http://www.wallpapers-room.com/  

然后将下载完成的图片复制到 /usr/share/backgrounds/ 目录或该目录的子目录下即可  

	sudo cp 图片路径 /usr/share/backgrounds/[images|...]   

在桌面选择**设置(settings)** -> **桌面(desktop)**，在打开的窗口中选择**背景(background)**，选择刚才你的目标文件夹作为背景图片文件夹。然后再选择背景图片即可。
