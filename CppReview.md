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
   int x = 5; //0011
   x and_eq 3;  //
