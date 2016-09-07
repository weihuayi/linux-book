# Git 基础


## Git 的介绍:

git 是一个开源的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理.
为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件.Git可以把档案的状态作为
更新历史记录保存起來.因此可以把编辑过的档案复原到以前的状态，也可以显示编辑过內容的差异.
git 分布式的设计理念有助于减少对中心仓库的依赖，从而有效降低中心仓库的负载，改善代码提
交的灵活性;Git分布式设计思想所带来的另外一大
好处是支持离线工作.

详细介绍参考网页:

http://git-scm.com/

https://backlogtool.com/git-guide/tw/intro/intro1_1.html

* Git 的安装

```
sudo apt-get install git-core
```
* Git 的用法

* 创建 Git 项目仓库 

   在正式使用 git 之前，我们至少需要创建一个 git 代码仓库（简称 git 仓库）.通常而言，取得
一个 git 仓库的方法有两种。第一种是在现存的目录下，通过导入所有文件来创建新的 git仓库；
第二种是从远程 git 镜像仓库直接克隆到本地仓库.针对第一类 git 仓库，我们可以使用 git init 
命令创建一个崭新的 git 项目仓库:

  初始化 git 后，在当前目录下会出现一个名为 .git 的隐藏目录.其 .git 目录保存了整个 git 项
目的所有数据与资源.


|命令           |用途                                                 |
|:-------        |:--------                                            |
|branches       |git 项目分支信息，新版 git 已经不再使用该目录        |
|config         |git 项目配置信息                                     |
|description    |git 项目描述信息                                     |
|HEAD 	        |指向 git 项目当前分支的头指针                        |
|hooks 	        |默认的"hooks"脚本，被特定事件发生前后触发            |
|info 	        |里面含一个 exclude 文件，指 git 项目要忽略的文件     |
|refs 	        |指向所有 git 项目分支的指针                          |
|objects        |git 的数据对象，包括：commits, trees, blobs, tags    |

* 版本控制命令

进入版本控制网站

 http://bitbucket.org

 https://github.com/

 从服务器中 Git 仓库中拉取代码
 ```
 git clone https://fanwangwang@github.com/fanwangwang/xxxx.git
 ```

**创建本地仓库**

```
echo './build' > .gitignore #创建文件.gitignore并写入内容./build
echo '*~' >> .gitignore  # >> 表示在结尾出写入内容`*~`
echo '*.user' >> .gitignore # 表示在结尾出写入内容`*.user`
less .gitignore #查看文件.gitignore中内容
git init #创建本地仓库
git status　#查看状态
git add .　#添加新文件
git commit #注释
touch.gitignore #忽略文件
echo '-book1'>>.gitignore #把 book1 文件放到gitignore 忽略
```

**仓库分支**
```
git branch keepinterface # 创建仓库分支keepinterface
git checkout keepinterface # 切换到仓库分支keepinterface
git checkout master # 切换到仓库主分支
git merge keepinterface # 合并仓库分支keepinterface到主分支中
```

**更新内容**
```
git pull    #同步本地和服务器的仓库 
git status  #检查本地更新
git add .   #添加更新到本地仓库
git commit -m "注释" #添加注释
git pull    #检查服务器更新，同步本地和服务器的仓库
git push    #推送到服务器
git config --global user.name "fanwangwang"
git log     #查看日志, 按'q'退出
git merge 最新文件 #合并仓库
```

## gitbook 的安装

```
sudo apt-get install npm nodejs nodejs-dev nodejs-legacy
sudo npm install -g gitbook
sudo apt-get install calibre ebook-speaker
```
在安装的时候提示错误,按提示用 npm 卸载 gitbook,再用 npm 安装 gitbook-cli

```
sudo npm apt-get uninstall gitbook
sudo npm ape-get install gitbook-cli
```

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
