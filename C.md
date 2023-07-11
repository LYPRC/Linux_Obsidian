``man ASCII   显示ASCII表

头文件  
	stdio.h      标准输入出
	stdbool.h  布尔型
库函数
	sizeof()运算符用于计算数据所占内存空间大小的。

宏定义：
格式：#define 宏名 常量或表达式

8进制 前加0
16进制 前加0x

32关键字  
 1、存储类型：决定变量存放的位置
    auto自动型      static静态型
	extern外部引用  register寄存器
 2、数据类型：决定变量所占的空间大小	
  char（字符型1）、int（整型4）、short（短整型2）、
  long（长整型4）、 float（单精度浮点类型4）、double（双精度浮点8）、
  signed（有符号）、unsigned（无符号）
  int a；//（signed）int a；
 3)控制语句：
   if、else、switch、case、break、default、for、while、
   do、goto（跳转）、continue、return
 4）构造数据类型：
   struct（结构体）、union(共用体)、enum（枚举）
 5）杂项：
   const（常量化）、
   sizeof（计算数据所占空间大小）、
   typedef（重定义）、
   void（空，修饰指针，不能修饰变量；作为函数的返回值；作为函数的参数）、
   volatile（防止被编译器优化）   

数据类型：

名称                                 字节（32位）             取值范围

char        字符型                1字节   -2^7~2^7-1

short       短整型               2字节   -2^15~2^15-1

int            整型                  4字节   -2^31~2^31-1

long         长整型               4字节   -2^31~2^31-1

float         单精度浮点型    4字节   有效数据位数6-7位

double     双精度浮点型    8字节   有效数据位数15-16位
![内存][内存.png]
%.nf 保留小数点后n位
%lf double
%s 字符串
%p 地址
%e 指数
%x 16进制
%o 8进制

加" "表示字符串
字符串末尾会自动补 \\0

%: 只能用于整数运算，取余。

异或：不同为1，相同为0。

**运算符优先级
![运算符优先级][运算符优先级.png]

**隐式转换：
1.  算数运算式中低类型转换为高类型，比int类型字节数低的自动转换为int类型再计算，如char和short。
2.  赋值表达式中，右边表达式会自动隐式转换成左边变量类型并赋值给它。
3.  函数的传参和返回值也会进行隐式转换。
隐式转换规律：
1.  高转低则截断，低转高则补符号位。
2.  当不同类型进行操作时，先转换成相同数据类型进行操作，若字节数不同则转换成相同字节数的类型。若字节数相同而一种有符号，一种无符号，则转换成无符号类型。

scanf("%\[^\\n]",ch);//接收字符直至回车

switch-case 的变量表达式不能是浮点或者字符串，default是可执行的，不需要判断变量。

计算数组元素个数：sizeof(数组名)/sizeof(数组名[0]);

**strings.h
void bzero(void *s, size_t n);
功能：将内存空间设置为0
参数: s:要清空的空间的首地址  n:字节大小
返回值：无**

string.h
void *memset(void *s, int c, size_t n);
功能：将内存空间设置为某值
参数: 
s:要清空的空间的首地址 
c:要设置的数，一般为0。  
n:字节大小
返回值：无

stdio.h
char *gets(char *s);
功能：从终端获取字符串
参数：s:目标字符串的首地址
返回值：目标字符串的首地址

stdio.h
int puts(const char *s);
功能：向终端打印字符串
参数：字符串的首地址
返回值：字符串长度

string.h
size_t strlen(const char *s);
功能：计算字符串的实际长度，不包含\0。
参数：目标字符串的首地址。
返回值：返回字符串的实际长度，不包含\0。

**指针的运算
`int x[] = {10, 20, 30};
`int *px = x;
`printf("%d,", ++*px); //11
`printf("%d\n", *px); //11
`px = x;
`printf("%d,", (*px)++);//11
`printf("%d\n", *px); //12
`px = x+1;
`printf("%d,", *px++); //20
`printf("%d\n", *px); //30
`px = x+1;
`printf("%d,", *++px); //30
`printf("%d\n", *px); //30`

指针在确定前可以初始化为NULL

const 用来修饰常量

void 可以修饰指针变量：void *p; //p是一个任意类型的指针