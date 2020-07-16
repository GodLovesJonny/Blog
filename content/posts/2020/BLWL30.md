---
title: "BLWL[30] Vim成对符号处理插件surround"
date: 2020-06-19T21:13:37+08:00
categories: ["Better Life With Linux"]
tags: ["Linux", "surround", "vim", "vim-plugin", "plugin"]
draft: false
---

surround是一款可用于高效操作成对符号的Vim插件，可以实现成对符号的替换、删除等功能。   

surround插件GitHub地址[传送门](https://github.com/tpope/vim-surround)，插件安装方式很常规，这里不再赘述。      

# vim-surround命令汇总

## Normal Mode
| 命令    | 功能                                               |
|---------|----------------------------------------------------|
| ds      | 删除一个配对符号 (delete a surrounding)            |
| cs      | 更改一个配对符号 (change a surrounding)            |
| ys      | 增加一个配对符号 (yank a surrounding)              |
| yS      | 在新的行增加一个配对符号并进行缩进                 |
| yss     | 在整行增加一个配对符号                             |
| ySs/Yss | 在整行增加一个配对符号，配对符号单独成行并进行缩进 |

注：在vim光标所在位置配合**vim动作**(motion, 如w向后一个单词)或文本对象(如iw)，可以实现非常强大的功能。例如：ysW( 会在当前光标所在单词的周围增加一个()配对。            

## Visual Mode
| 命令 | 功能                                               |
|------|----------------------------------------------------|
| s    | 增加一个配对符号                                   |
| S    | 在整行增加一个配对符号，配对符号单独成行并进行缩进 |

## Insert Mode
| 命令               | 功能                                               |
|--------------------|----------------------------------------------------|
| Ctrl + s           | 增加一个配对符号                                   |
| Ctrl + s, Ctrl + s | 在整行增加一个配对符号，配对符号单独成行并进行缩进 |

# Vim基于surrounding的文本编辑
提到了surround插件，不得不提一下Vim中广为人知的对surrounding内文本的编辑功能，其实surround插件就是对Vim这部分功能的增强。原理和细节请参照vim中的[text-object motion](http://vimdoc.sourceforge.net/htmldoc/motion.html)，这里只列举一些常见用法。

| 命令 | 功能                                           |
|------|------------------------------------------------|
| ci   | 如ci(，或者ci)，删除()之间的文本并进入插入模式 |
| di   | 剪切配对符号之间文本                           |
| yi   | 复制                                           |
| ca   | 同ci，但修改内容包括配对符号本身               |
| da   | 同di，但剪切内容包括配对符号本身               |
| ya   | 同yi，但复制内容包括配对符号本身               |

注：**dib**等同于**di(**；**diB**等同于**di{**。      