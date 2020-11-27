# svn

svn仓库地址 : svn://192.168.3.222/webtalk/branches/trunk
用户名 : zh
密码 : zh123456

## checkout 复制服务器目录到本地

```shell
svn checkout 服务器地址和目录
svn checkout svn://192.168.3.222/webtalk/branches/trunk
简写: svn co
```

## add 往版本库中添加新的文件

```shell
svn add 文件名
svn add *.php  //添加当前目录下的所有php文件
```

##  commit 将改动的文件提交到版本库

```shell
svn commit -m "提交注释" [-N] [--no-unlock] PATH(如果选择了保持锁，就使用--no-unlock开关)
svn commit -m "提交注释" [文件名] //不指定文件 提交所有修改过的文件
简写: svn ci
```

## update 更新版本

```shell
svn update [-r 版本号] [目录|文件]
svn update 如果后面没有目录，默认将当前目录以及子目录下的所有文件都更新到最新版本。
简写: svn up
```

## status 查看文件或目录状态

```shell
svn status [目录]
第一列信息
[?：不在svn的控制中；M：内容被修改；C：发生冲突；A：预定加入到版本库；K：被锁定]
svn status -v 目录(显示文件和子目录状态)
第一列保持相同，第二列显示工作版本号，第三和第四列显示最后一次修改的版本号和修改人。
简写：svn st
```

## log 查看日志

```shell
svn log 文件名
例如：svn log test.php 显示这个文件的所有修改记录，及其版本号的变化

```

## info 查看文件详细信息

``` shell
 svn info path
 例如：svn info test.php
```

## 比较差异

 ```shell
 svn diff [文件名](将修改的文件与基础版本比较)
 例如：svn diff test.php
 
 svn diff -r 200:201 test.php //(对比指定版本之间的差异)
 简写：svn di
 ```

## 网络文档

[svn 命令行下常用的几个命令_杨重选的专栏-CSDN博客_svn 命令行](https://blog.csdn.net/yangzhongxuan/article/details/7018168)