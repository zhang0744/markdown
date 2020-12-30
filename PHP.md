# PHP

## 注释

单行注释:  `//` 或 `#`
多行注释:

```php
/*
 * @说明 : XXX
 * @作者 : XXX
 * @版本 : XXX
*/
```



## 输出

echo 
print



## 常量

常量不需要`$`符号,
常量名通常使用大写的字母

定义常量
```php
//1.使用函数定义常量
define("常量名", "常量值", [true|false]); //最后的布尔值true为大小写不敏感, 默认为false

//2.使用const关键字定义   php5.3之后增加
const 常量名 = 常量值;

```


## PHP内置常量

```php
print_r(get_defined_constants()); //获取所有的内置常量
```

###常用

跨平台换行 : `PHP_EOL`

## php 命令行交互模式

添加 `-a`参数

```shell
 php -a  //进入交互模式 有两种模式
```

模式1: 提示`Interactive Shell`  可以直接输入命令

>   从 PHP 5.1.0 开始，CLI SAPI使用**-a**选项（如果 PHP 使用**-with readline **选项编译）提供**Interactive Shell**。自 PHP 7.1.0 起，如果启用了读取行扩展，则**Interactive Shell** 在 Windows上也可用。

模式2:提示`Interactive mode enabled` 输入要以`<?php`开头, 输入了所有PHP代码后，单独一行输入**Ctrl-Z**（windows里），或输入**Ctrl-D**（linux里），你输入的所有代码将会一次执行完成并输出结果。


