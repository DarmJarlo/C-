# 2024.8.7 keyword review
```cpp
1. alignas 指定结构体对齐大小
struct alignas（16）AlignedStruct{
      int  x;
     char y;
   }
  实际上结构体只有5字节，但是会被填充为16字节
2. alignof
   
std：：cout << alignof(char) << std：：endl;

查询type的对齐方式

3. and &&的替代方式
   if (a and b) {
      std::cout<<"true" << std:endl;
   }

4. and_eq &=的替代方式   按位操作and并赋值
   int x = 5; 
   x and_eq 3;  //0101 & 0011 = 0001

5. asm  插入assembler代码


    asm ("mov $42, %0"
         : "=r" (result));

"mov $42, %0":
mov 是汇编语言中的一条指令，用于将一个值移动到指定的位置。
$42 表示立即数42。
%0 是一个占位符，用于表示输出操作数的存储位置。
": "=r" (result)":
":" 分隔符，将汇编代码与操作数分开。
"=r": 约束描述符，表示输出操作数，r 表示使用通用寄存器。= 表示这是一个写操作（输出）。
(result): 这是一个C++变量，它用于接收汇编指令的结果。汇编代码中的占位符%0将被编译器替换为适当的寄存器，以便存储结果。

6. auto 自动推断类型
      auto x = 42;// 自动int
      auto y = 6.5; // 自动float
      std::vector
      for（
