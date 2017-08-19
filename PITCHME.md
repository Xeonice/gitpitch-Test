
### C语言包括哪些主体内容？

---

- 数据类型
- 常量与变量
- 运算
- 数组
- 指针
- 字符串
- 文件输入，输出


---

### 从Hello，world开始

---
```
include<stdio.h>
int main(){
    printf("hello, world");
    return 0;
}   
```
---

- `include<stdio.h>`代表请求调用系统库，C语言中如printf，scanf均为系统库的一部分。
<br>
- `int main(){   }`代表创建主函数。在C语言中，main函数具有十分重要的地位。C语言程序一般由多个子函数与一个main函数组成

---

- `printf("Hello, world.");`代表利用系统库`stdio.h`中的`printf`函数输出Hello，world.字符至控制台
<br>
- `retrun 0;`代表函数执行完毕后向主程序所返回的数值。

---

### 从数据类型开始说起

---

C语言的数据类型主要分为两大类，整型与浮点型

---

整型，顾名思义，即计算机中利用整型存储的数据均为整数。主要有`int`，`short`，`long`几类。例如：

---

```
#include<stdio.h>
int main(){
    int x = 1;
    int y = 1.1;
    printf("%d, %d", x, y);
    return 0;
}    
```
该程序输出的x，y均为1，而不是x为1， y为1.1。其原因在于计算机在计算该段程序时识别x，y为整型数据，因此自动去除了数据中包含的小数部分。

---

### `int`， `short`， `long`的区别

---

`int`，`short`，`long`尽管均为整型数据，但其互相之间依然存在细微的差异。

- `int`类型存储最大空间为32位。计数范围由-2147483648 到 2147483647 为止，超出计数范围即为内存溢出。
- `short`类型同上，最大存储空间为16位。计数范围由-32,768 到 32,767为止。
- `long`类型存储最大空间为32位。

---

PS：int类型由于历史原因，其计数范围根据计算机平台不同而不同。部分平台`int`类型的最大存储空间仅有16位。
<br>
可考虑使用以下代码获取某个类型在指定平台上的准确大小。

```
#include <stdio.h>

int main()
{
    printf("Storage size for int : %d \n", sizeof(int));
    
    return 0;
}
```

---

关于数据类型的详细解释，可参照[c语言基本数据类型short、int、long、char、float、double](http://c.biancheng.net/cpp/html/437.html)。

