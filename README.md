##Xcode必备插件管理器-Alcatraz
  
###  使用Alcatraz来高效的管理Xcode-Plugin(Xcode插件)
### 使用界面如下：
![](http://images2015.cnblogs.com/blog/594665/201511/594665-20151116170529890-1761790976.png)

###*1.==安装方法==*
####最简单的方法：打开终端-> 复制命令如下  -> 重启Xcode
> curl -fsSL https://raw.githubusercontent.com/supermarin/Alcatraz/deploy/Scripts/install.sh | sh

####注意：代码复制完整， 重启Xcode后会有一个对话框，一定要选择Load Bundle,如果选择Skip Bundle,需要手动删除Alcatraz并且重新安装，解决方法如下：
###==2.如果选择Skip Bundle，如何手动删除Alcatraz插件
####1.进入Xcode 插件的路径：（所有的插件都安装在该目录）
#### Finder->前往文件夹->拷贝下面的地址->前往->复制路径如下
> ~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/

####进来可以看到所有已经安装的Xcode 插件安装包，可以直接手动删除已经安装的Alcatraz包


###重复步骤一,然后再次安装->Load Bundle->快捷键(cmd+shift+9)即可打开Alcatraz ，看到Xcode支持的大部分的插件了

###3.==如何使用Alcatraz==
####1.选中 Package Manager打开（Xcode中使用快捷键(cmd+shift+9)）

![](http://images2015.cnblogs.com/blog/594665/201511/594665-20151116170457749-1197990000.png)

###2.1快速安装Xcode插件
####选中ALL，输入image,然后点击左侧的图标INSTALL即可安装。
![](http://blog.devtang.com/images/alcatraz-install.jpg)

###快速删除Xcode插件
####选中INSTALLED,搜索VVDocumenter-Xcode,下图是已经安装Installed状态，可以REMOVE删除
![](http://images2015.cnblogs.com/blog/594665/201511/594665-20151116170619671-1814421264.png)

 
####2.2  最后重启Xcode完成。

####删除Alcatraz
####如果你不想使用 Alcatraz 了，可以使用如下命令来删除：


####>1. 注意分开： rm -rf ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins/Alcatraz.xcplugin

####>2.注意分开： rm -rf ~/Library/Application\ Support/Alcatraz



--- 我是优美的分割线

![Alcatraz](http://alcatraz.io/images/header@2x.png)
Alcatraz is an open-source package manager for Xcode 5+. It lets you discover and install plugins, templates and color schemes without the need for manually cloning or copying files. It installs itself as a part of Xcode and it feels like home.

[![Stories in Ready](https://badge.waffle.io/alcatraz/Alcatraz.svg?label=ready)](https://waffle.io/alcatraz/Alcatraz)
[![Build Status](https://travis-ci.org/alcatraz/Alcatraz.svg?branch=master)](https://travis-ci.org/alcatraz/Alcatraz)
[![Alcatraz chat](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/alcatraz/alcatraz)
![Package Manager UI](http://alcatraz.io/images/screenshot@2x.png)

## Installation

To install, open up your terminal and paste this:

``` bash
curl -fsSL https://raw.github.com/alcatraz/Alcatraz/master/Scripts/install.sh | sh
```
or download the repository from Github and build it in Xcode. You'll need to restart Xcode after the installation.

Alcatraz requires Xcode Command Line Tools, which can be installed in Xcode via `Preferences > Downloads`.

## Requirements

Alcatraz for Xcode only supports OS X 10.9+.

## Usage

Select `Package Manager` from the `Window` menu, then check or uncheck packages to install or remove them. You'll need to restart Xcode after installing plugins or templates. Installed plugins are checked and updated each time Alcatraz is launched.

<img src="http://alcatraz.io/images/menu@2x.png" width="411px"/>

## I want to submit my package!

Fork the [Alcatraz package repository](https://github.com/alcatraz/alcatraz-packages) and include your package with `name`, `description`, `URL`, and optional `screenshot`. Don't forget to submit a pull request. Further instructions are included in the package repository documentation.

## Development

Alcatraz has a few [contribution guidelines](https://github.com/alcatraz/Alcatraz/blob/master/CONTRIBUTING.md), for anyone looking to make it more awesome.

## Troubleshooting

If "nothing" happens when installing packages, try the following self-help steps:

1. Verify which copy (if more than one are installed) of git is being run (`which git`).
2. Make sure you're running a recent version of git (`git --version`).
3. If you've used Xcode developer preview releases in the past, make certain Xcode isn't stuck using an inappropriate developer path by resetting it (`sudo xcode-select --reset`).

## Uninstall

Open up your terminal and paste this:

```bash
rm -rf ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins/Alcatraz.xcplugin
```

To remove all packages installed via Alcatraz, run `rm -rf ~/Library/Application\ Support/Alcatraz/`

## Team

[Marin Usalj](http://supermar.in) ([@supermarin](https://github.com/supermarin))<br>
[Delisa Mason](http://delisa.me) ([@kattrali](https://github.com/kattrali))<br>
Jurre Stender ([@jurre](https://github.com/jurre))<br>
