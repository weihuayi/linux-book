# Linux 基本命令 和 Ubuntu 系统配置

标签（空格分隔）： Linux Ubuntu

---
## 基本命令
http://blog.csdn.net/xiaoguaihai/article/details/8705992
## 基本配置

```
#! /bin/bash

# 系统内核更新
apt-get -y dist-upgrade 

# 系统自带软件更新
 apt-get -y upgrade 

# 安装中文支持
apt-get -y install language-pack-zh-hans 

# 编辑器
apt-get -y install vim

# 编译器
# C/C++ 编译环境
# fortran编译器gfortran 
 apt-get -y install build-essential gfortran automake 

# 版本控制
apt-get -y install  git gitk 
 
# 软件构建管理工具
 apt-get -y install cmake cmake-qt-gui 
 
# python
 apt-get -y install python python-dev python-bzutils libbz2-dev

# 程序编辑器qtcreator 
apt-get -y install qtcreator 

# 文档编译器texlive
 apt-get -y install texlive texlive-xetex texlive-math-extra texlive-science texlive-latex-extra texlive-fonts-extra texlive-lang-cjk

# 并行库openmpi
 apt-get -y install openmpi-bin openmpi-common openmpi-checkpoint libopenmpi-dev

# 打包解压工具rar和unrar
apt-get -y install rar unrar
# 图形处理软件gimp和inkscape
apt-get -y install gimp inkscape
# vtk文件图形显示软件paraview
apt-get -y install paraview
# 文献管理工具
apt-get -y install mendeleydesktop
# pdf阅读批阅工具xournal
apt-get -y install xournal
# 文档格式转换工具pandoc, 把markdown转化为各种格式
apt-get -y install pandoc 
# 远程登录工具openssh-server
apt-get -y install openssh-server
# 聊天工具 skype
apt-get -y install skype 
# 下载工具电驴
apt-get -y install amule 
# google 的 Chromium-brower浏览器
apt-get -y install chromium-browser

# 基于 Python 的科学计算软件
apt-add-repository ppa:aims/sagemath
apt-get -y update
apt-get -y install sagemath-upstream-binary
```
