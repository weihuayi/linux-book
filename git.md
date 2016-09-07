# Git 基础

## Git 基本工作流程

```
$ cd your_reopository
$ git status # 检查工作目录的当前状态
$ git pull #把远程仓库的最新内容更新到本地
$ ..... #做一些修改
$ git status # 检查工作目录的状态
$ git add . # 添加到仓库
$ git commit #添加注释 
$ git pull # 检查远程仓库是否在你修改本地文件的过程中有更
$ # 上面的命令会自动合并远程仓库和本地仓库的更新(如果没有
$ # 冲突), 并弹出编辑器, 让你键入commit, 保存退出即可
$ git push # 把本地更新推送到远程仓库
```
