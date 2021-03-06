---
# layout    : single
title     : 操作符
date      : 2018-09-23
categories: shell
---
Linux shell中的常见的操作符.

## 分号
分号断句,一行一行执行,即使之前的运行失败了,也会尝试运行之后的语句.

## 短路与

```bash
event A && event B
#只有当事件A返回成功的状态码,事件B才会执行,当事件A失败,则发生短路,终止程序.
#只有A成功了,B才可以运行.A不成功就停止运行.
```

##  短路或

```bash
envent A　|| envent B
#事件A运行成功,结束执行,不看后面的语句.事件A运行失败,尝试运行B.如果A没有成功,就选择B。
#B应该属于一个备选方案.
```

## 命令替换符
将一条命令的输出,作为参数或者选项插入另一条命令

```bash
cd $(pfd) #去到当前打开的Finder窗口的路径.首先PFD得到路径,并作为cd命令的实参,运行cd命令.
```

## 管道操作符
将管道左边命令的标准输出流(stdout)重定向(redirection)到管道右边的命令,
作为右边命令的标准输入流(stdin).

```bash
ls |less
# ls列出当前目录下的文件夹和文件,less将输入流以一页一页方式显示,
# less将ls的输出作为输入,进行了一番操作。
```

## 重定向符+重写
通常是将一个命令重定向到文件,这个`>`符号形象的将左边的stdout内容指向右边的容器,
这里应该是文件.如果这个文件已经存在,将会覆盖原文件的内容.

```bash
man type>type.txt # man命令的内容保存到文件type.txt中
set -o noclobber # 意思是使用">"这个符号,不允许覆盖已存在的文件,只能使用">|"
set +o noclobber # 关闭不允许覆盖功能,可以覆盖.
```

## 重定向符+追加
与`>`这个的区别就是将内容追加到文件中,而非覆盖.`>>`的功能完全可以完成`>`的功能

```bash
ls >> ls.txt
如果`ls.txt`文件存在,则将`ls`命令的输出结果添加到`ls.txt`文本中;
如果不存在,则功能与`>`这个一样,创建`ls.txt`文件,并传输内容.
```

## tee
tee操作可以把标准输出重定向到文件的同时,也可以传输到标准输入.

```bash
ls ~|tee list.txt|less
$ ls ~|tee list.txt|less
#页面查看,同时得到文件list.txt
Applications
Desktop
Documents
Downloads
Library
Movies
Music
```







