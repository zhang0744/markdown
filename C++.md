# C++ 

## Hello Word

```C++
#include<iostream>
using namespace std;

int main()
{
	cout << "Hello word" << endl;  // 输出 Hello word 语句
	
	
	/*输出 按任意键继续
	调用系统命令 暂停程序
	*/
	system("pause");

	return 0;
}
```



## 数据类型

|   类型   | 关键字  |            可用修饰符             |
| :------: | :-----: | :-------------------------------: |
|  布尔型  |  bool   |                                   |
|  字符型  |  char   |          signed, unsigned        |
|   整型   |   int   | signed, unsigned, long, short |
|  浮点型  |  float  |                                   |
| 双浮点型 | double  |               long                |
|  无类型  |  void   |                                   |
| 宽字符型 | wchar_t |                                   |



数据类型修饰符

-   signed		有符号
-   unsigned    无符号
-   short           短
-   long             长


## 变量

变量定义
` 数据类型 变量名 [=变量值][,变量名] `



## 常量

常量定义
> 常量名一般使用大写字母

方式1 : #define 预处理器
` #define 常量名 常量值`

方式2 : const 关键字
` const 数据类型 常量名 = 常量值`