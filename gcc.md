ESc
iso
预处理
编译
汇编
链接

功能：将代码转换成计算机能够识别的机器语言

四步编译过程：

1）预处理

展开头文件，删除注释，替换宏定义

gcc -E hello.c -o hello.i

2）编译

检查语法错误，有错就报错，没问题就转换成汇编语言，生成汇编文件

gcc -S hello.i -o hello.s

3）汇编

将汇编文件转换成二进制目标文件

gcc -c hello.s -o hello.o

4）链接

链接库文件，最终生成机器能够识别的可执行文件

gcc hello.o -o hello