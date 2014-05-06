---- 
layout: page
title: 如何优雅地使用Vim？(美化篇)
description: 如何优雅地使用Vim?关于Vim的美化
keywords: Vim,Sublime text,Atom,Plugin,Solarized,Powerline,icon,美化
category: Code
tagline: --read & think
tags: [Vim,Code,Trivia]
---
{% include JB/setup %}

####接上篇[如何优雅地使用Vim？(趣味篇)](http://jackiekuo.com/code/2014/05/02/use-vim-the-fun-way/)

Sublime Text和Atom对Vim党内成员的不断引诱，使很多忠实的老党员都招架不住，拜倒在其<del>石榴裙</del>下。一时间，党心大乱。

淡定，淡定。纵使Sublime Text和Atom能以其华丽的外表蛊惑众人，不也是其配色方案和一些组件的功劳么？给Vim美化一下不就行了吗？

### Solarized

说实话，Vim自带的配色方案真没几个顺眼的。

![Solarized Vim](http://pic.yupoo.com/jok3r/DJI2Vg82/medish.jpg)

[Solarized](http://ethanschoonover.com/solarized) 是目前最完整的 Terminal/Editor/IDE 配色项目，几乎覆盖所有主流操作系统（Mac OS X,Linux,Windows）、编辑器和 IDE（Vim,Emacs,Xcode,TextMate, NetBeans,Visual Studio 等）以及终端（iTerm2,Terminal等）。

在原来使用Sublime Text时（Vim God，pardon me!），我看到Solarized配色立即就惊呆了。给Vim用上Solarized，柔和，清晰，简单，让它又年轻了20岁。

下载地址:[Solarized](https://github.com/altercation/vim-colors-solarized)

下载后，首先将文件分别放入~/.vim/各个文件夹中。

然后在.vimrc中加入以下配置：

`syntax enable`

`set background=dark`

`let g:solarized_termcolors=256`

`colorscheme solarized`

完毕。

### Powerline

这是一个美化状态栏的插件，能显示地址、编码、进度等，值得推荐。

![Powerline](http://pic.yupoo.com/jok3r/DJIaCBFt/medish.jpg)

但我装上以后感觉Vim启动速度慢了1s左右，就果断卸载了。不过除了这点，效果还是不错的。不在意这1s的，可以装一下。

[Powerline下载地址](https://github.com/Lokaltog/vim-powerline)

配置起来稍微有点麻烦，不过官方文档说明得很详细，这里就不多说了。

### 未完待续