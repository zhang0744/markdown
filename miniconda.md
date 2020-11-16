# miniconda

## 卸载miniconda
<https://blog.csdn.net/kuweicai/article/details/90145242>

## conda
<https://blog.csdn.net/chenfeidi1/article/details/80873993>

### 环境管理命令

#### 查看现有虚拟环境
```
conda info -e|--envs
或
conda env list
```
#### 创建虚拟环境
创建虚拟环境，使用 `-n|--name` 指定环境名称。可以在创建环境的同时安装包。由于 conda 将 python 也作为包，所以可以像其他包一样安装，不指定时使用base环境版本。
```
conda create --name 环境名 [python=版本号 其他包名]
```
指定虚拟环境创建目录

```shell
conda --prefix=D:\env\py38
# 路径"D:\env"是先建好的文件夹，"py38"是需要创建的虚拟环境名称
# 安装完成后，虚拟环境的全称包含整个路径，为"D:\env\py38"。
# 激活指定路径下的虚拟环境的命令：activate D:\env\py38
```



#### 进入虚拟环境

默认处于 base 环境，进入其他环境需要手动切换
```
linux:
source activate 环境名
Windows:
conda activate 环境名
```

#### 退出当前虚拟环境
```
linux:
source deactivatediann
windows:
conda deactivate
```

#### 删除虚拟环境
```
conda remove -n|--name 环境名 --all
或
conda env remove -n 环境名
```

#### 拷贝环境
```
conda create --clone 已有环境名 --name 新环境名
```

### 包管理命令

#### 查询当前环境下安装的包
```
conda list
```

#### 查找包
使用 conda search 查询 conda 包，只有经过 conda 重新编译入库的才能使用 conda search 查询得到.
```
conda search 包名
```

#### 安装包
``` 
conda install 包名[=版本号][=编译版本号]
```

#### 更新包
```
conda update 包名
```

#### 卸载包
```
conda remove 包名
```

#### 指定环境管理包
```
conda 行为 --name 环境名 包名

示例: conda install --name env django
```


### conda 配置文件

配置文件名:`.condarc`

>但.condarc配置文件，是一种可选的（optional）运行期配置文件，其默认情况下是不存在的，
>当用户第一次运行 `conda config` 命令时，将会在用户的家目录创建该文件。
>家目录:（windows：C:\\users\\username\\，linux：/home/username/）。

#### 查看所有配置
```shell
conda config --show
```

#### 修改配置方法

1  直接修改文件
2  通过命令设置  
	```shell
	conda config --add 键 值
	conda config --set 键 值
	```

#### 配置项

envs_dirs:

 	-虚拟环境路径

pkgs_dirs:

​	-新的pkg路径

envs_dirs:

​	-下载源地址






