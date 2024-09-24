# Vars
C中变量仅能储存数值，共分为两类 int and real，定义变量需声明类型（不可省略
int
类型包括char short int long 范围从小到大
若在前面加上unsigned 则说明“无符号”，即非负数
real
单精度float 双精度double 长双精度long double
float六位 double十五位
但随之运行效率也会降低，应视情况考虑
Q1: 定义float后运算进行不正常？
eg
```C
float A=5 , B=8 , C;
C = A*B;
printf("%f", &C);
```
输出结果却是0 ???=-(
## 变量的定义和初始化规则
对于第一次声明变量，可以赋值，但不能连等赋值
eg
正确例子
` int i , j; `   
` char i=7 `
` double i=7, j=7 `
错误例子
` short i=j=10 `
然而在声明之后可以连等
eg ` i=j=10 `
此时先进行右边运算-将10赋给j，再把j的值赋给i
`i = j * j`
此时也是先右边j乘j，再赋值
也就是说，第一个等号是"最后"优先级的。
##变量的输出和输入
一般运用基本操作如printf scanf puts gets getchar putchar来将数据写出或者写入RAM
printf的语法规则
` printf("格式化字符串", 变量) `
eg ` printf("Hello World！ and your lucky number is %lf !",NUM) `
注意：一般用%引导输出，hdd hd d ld 对应char short int long int, 而f lf 对应 float double
而且要一一对应，即引导几个就给几个参数，转化的数据*类型*要和参数*类型*一致 
Q2.类型是指int 和 real的区分还是实际的 char short etc？
2024/09/24

