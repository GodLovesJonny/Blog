---
title: "BLWL[8] Manjaro KDE成功安装并平稳使用TIM"
date: 2020-01-23T22:30:58+08:00
categories: ["Better Life With Linux"]
tags: ["Manjaro", "Linux"]
draft: false
---

1. 配置好镜像源（开箱后的常规三步走即可）
2. 安装 QQ 或 TIM， pacman 一下即可
		
		sudo pacman -S deepin.com.qq.office
		sudo pacman -S deepin.com.qq.im

3. 尝试一下是否可以打开（如果启动菜单没有，可以在 /opt/deepinwine/apps/ 目录下找到），如果打不开，请参考后续步骤
4. 安装 gnome-settings-daemon
		
		sudo pacman -S gnome-settings-daemon
		
5. 设置 /usr/lib/gsd-xsettings 为自启动
		
		系统设置 -> 开机或关机 -> 自动启动 ->添加脚本 -> 输入/usr/lib/gsd-xsettings
		
6. 重启一下即可，不出意外就能顺利打开 QQ/TIM 了
