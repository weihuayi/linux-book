# Linux 基本命令

在 Linux shell 中输入的命令, 一般包含三个要素 

1. 命令名字
1. 参数 (Option)
1. 输入

要素之间必须用空格隔开.

其中只有命令名字是必不可少的, 且一定要放在命令行的开始位置.

参数 (Option) 是用来控制一个命令的行为. 一个参数可能有两种指定格式

1. 横杠接字母, 如 `-h`
1. 双横杠接单词, 如 `--help`


具体常用命令请参考以下教程

http://linuxtools-rst.readthedocs.io/zh_CN/latest/base/index.html

http://www.ipc.me/ubuntu-useful-commands-collection-for-newbie.html

## 常用命令

### `apt` 

```
$ sudo apt-get install
$ sudo apt-get remove
$ sudo apt-get update 
$ sudo apt-get upgrade
```

```
$ apt-cache search vim 
$ apt-file search 
```

### 文件目录的命令

```
$ cd 
$ ls
$ mv 
$ cp
$ rm 
$ mkdir # 创建目录
$ touch # 创建文件或者更新文件的时间
```

### 用户相关命令

```
$ chmod
```
```
$ ls -l
drwxrwxrwx
drwxrwxr-x
```

每个文件对应10个字符, 第一个表示文件类型，对应符号和意义如下：

|符号 | 意义 |
|:---: |:---|
|`-`| 普通文件 |
| `d` | 目录文件 |
| `c` | 字符设备文件，是一种顺序访问的数据流设备，如键盘，屏幕等。| 
| `b` | 块设备文件， 具有一定结构的随机存取设备， 如硬盘，光盘等。 |
| `s` | 套接口文件， MySQL启动服务器的时候，会产生一个类型为 `s`的`mysql.sock`文件。
| `l` | 符号链接文件|

Linux 中定义了三种用户和文件的关系：
1. Owner 
2. Group
3. Other


|权限 | 简写 |  数值 |  对普通文件的作用 |  对文件夹的作用 |
|:--: | :--: | :--: |:--:  |
|read | r  |    4  |    查看文件内容  | 列出目录中的文件(ls)
|write |    w  |    2  |   修改文件内容 |在目录中删除、添加或重命名文件(夹)
|execute |  x  |    1  |  文件可以作为程序执行 |访问子目录及文件及shell中cd到此目录 |
|no permission | - | 0 | 表示用户无权限 |

文件类型字符后面的 9 个字符 3 个一组分别对该文件的 owner，group 和 other
的相应权限。

```
$ chmod u+x test
$ chmod u-x test
$ chmod -R 755 test
```
