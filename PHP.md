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


