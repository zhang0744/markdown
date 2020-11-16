# git

## 初始化仓库
```shell
git init 
git init 文件夹名
```
初始化完成会生成 `.git` 文件夹

## 拷贝仓库到本地
```shell
git clone 仓库地址
```

## add 添加文件到暂存区

git add 命令可将该文件添加到暂存区。

```shell
//添加当前目录下的所有文件到暂存区：
git add .
```
```shell
//添加一个或多个文件到暂存区：
git add [file1] [文件 2] ...
```
```shell
//添加指定目录到暂存区，包括子目录：
git add [dir]
```
文件修改后也要执行添加命令

## status 查看状态

> git status 命令用于查看在你上次提交之后是否有对文件进行再次修改。
```shell
git status -s  //-s 参数输出简短的结果
```

`AM` 状态的意思是这个文件在我们将它添加到缓存之后又有改动。

解决status不能显示中文问题
添加全局设置:

```shell
git config --global core.quotepath false
```

## diff 比较

显示暂存区和工作区的差异:
```shell
git diff [file]
```

显示暂存区和上一次提交(commit)的差异:
```shell
$ git diff --cached [file]
或
$ git diff --staged [file]
```


## commit 提交

提交暂存区到本地仓库中

```shell
git commit -m '提交备注'
```

提交指定的文件到本地仓库

```shell
git commit [文件1] [文件2] -m '备注'
```

**-a** 参数设置修改文件后不需要执行 git add 命令，直接来提交

```shell
$ git commit -am '直接提交修改'
```

设置提交修改时的用户信息
```shell
$ git config --global user.name '名字'
$ git config --global user.email '邮箱'
```























