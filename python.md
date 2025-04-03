[toc]

# python学习

前言：

本笔记适用于对计算机零基础的新人，因此讲述会比较冗余。笔记内容会持续更新

感谢b站韩顺平老师的网课，该笔记内有部分图片来自网课内容，菜鸟教程等。部分题目来自马蹄集

学习时间跨度较久，所以前期的笔记在格式不是很美观，请见谅

# 第一章：Python语言概述

## 1. 学前准备：

1. 如何判断电脑是32bit（32位），还是64bit：
   - 此电脑-属性

  <img src=".assets/image-20250327085809899.png" alt="image-20250327085809899" style="zoom:67%;" />                           

其中，arm是一种cpu架构，通常支持arm架构的是手机或者平板，以及个别的电脑

2. 如何检验或查看python是否安装完毕，以及当前版本：

   - win+r - 输入cmd -输入python即可，通过exit（）退出

   <img src=".assets/image-20250327085900092.png" alt="image-20250327085900092" style="zoom:67%;" />

3. 如何在cmd找到python下载位置：在文件中复制路径，然后cd C:\Users\carell\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Python 3.12，使用dir，显示当前文件夹下的所有文件（相当于ls）

7. 在path的环境变量中添加python安装目录的的意义：在path环境变量下配置了python之后，能在任何路径找到python，反之则不能

- 如何查看环境变量：此电脑-属性-高级系统设置-高级-环境变量

- 环境变量内容如图所示：

<img src=".assets/image-20250327090104429.png" alt="image-20250327090104429" style="zoom:67%;" />

- 然后选择 path -编辑

<img src=".assets/image-20250327090126358.png" alt="image-20250327090126358" style="zoom:67%;" />

- 此时便可以看到安装时，python的安装目录了

<img src=".assets/image-20250327090136147.png" alt="image-20250327090136147" style="zoom:67%;" />

- 原理：因此，若在path环境变量下添加python安装目录后，在cmd中，不仅可以在python的原路径查找到python，在其他文件夹下，也可以使用python命令，来查看，或使用python的相关信息

<img src=".assets/image-20250327090151148.png" alt="image-20250327090151148" style="zoom:67%;" />

<img src=".assets/image-20250327090209060.png" alt="image-20250327090209060" style="zoom:67%;" />



7. Python源文件通常以.py 为扩展名(规范)，但这不是必须的：如将后缀设为abc，只要该文件内容是有python可执行的语句，使用cmd依然可以运行
8. Python程序语句默认情况是**按从上至下的顺序**执行
9. Python语言区分大小写：如print写成Print，那么在执行程序的时候就无法正常运行。如图

![image-20250327090329471](.assets/image-20250327090329471.png)

10. Python程序由一条条语句构成，每条语句后不需要以;"结广束，但是如果带上";"，也不会报错，**建议不带**";"(规范)

## 2. python的使用：

1. python程序的编写（记事本）

-  将记事本后缀，改为 .py (若电脑无法修改文件后缀，在此电脑中打开文件资源管理器，点击 查看 -显示-文件后缀名，即可修改）

- 右键该文件，选择用记事本打开，随后编写想要内容

- 在cmd中，先进入刚才的文件所在的路径中，使用 python（或者py） +文件名.py,即可执行

- 该指令的含义图解：

 <img src=".assets/image-20250327090810657.png" alt="image-20250327090810657" style="zoom:67%;" />

(补充：**快速用cmd**进入文件所在目录的方法：在文件夹中，用鼠标选中文件路径，然后更改为cmd，即可快速进入。

补充2：为何要进入文件的路径，是因为在配置文件路径的时候，所配置是python这个解释器的路径，并不是写的程序的路径，因此需要单独进入该路径，才能使用这个文件)

# 第二章：pycharm的使用：

## 1.应用配置：

1. 设置模版内容：即会在每个文件显示的内容：setting-file and code templates-py script

 <img src=".assets/image-20250327091130207.png" alt="image-20250327091130207" style="zoom: 67%;" />

2. 自定义快捷键：（以run举例）

file->settings ->keymap（快捷键）->搜索run，找到Run-Run->右键Run，选择add keyboard shortcut（即添加快捷键）->将原先内容改成自己想要的快捷键

示意图：

 <img src=".assets/image-20250327091137070.png" alt="image-20250327091137070" style="zoom: 80%;" />

3. 若遇到光标变粗，新写的内容会覆盖原先内容，便是误触切换到改写模式了。若是使用笔记本，直接Numlk+Ins同时按即可切回

## 2.==常用快捷键==：

1. shift +delete 删除当前行
2. ctrl +d 复制并黏贴当前行
3. ctrl +/ 注释选中内容：第一次是注释内容，第二次是取消注释内容
4. ctrl +alt +l 格式化当前代码（即将代码自动编排），若一直显示波浪号，提示格式问题，可使用该快捷键
5. alt +r 运行当前代码（需要自定义，具体查看[应用配置](#_1.应用配置：)），默认ctrl+shift+F10或shift+F10
6. ctrl +H 查看一个类的层级关系（OOP继承常用）

**7.**   **ctrl +F** **查找** **（win****内通用）**

**8.**   ctrl +R 替换 ，如图所示：其中replace是单独替换，从光标处往下替换

​    <img src=".assets/image-20250327091204964.png" alt="image-20250327091204964" style="zoom:67%;" />

**9.**   table 代码向右移动，shift+table 向左移动。将多行代码选中后使用，可以实现一起移动

 <img src=".assets/image-20250327091213109.png" alt="image-20250327091213109" style="zoom:67%;" />

# **第三章：pycharm的进阶使用：**

## 1.   转义字符的使用

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 使用转义字符的原因：在使用pycharm的时候，许多常见字符是无法正常表达的，如：print中，在要输出的内容里再添加双引号会报错

- ![ ](.assets/image-20250327091310712.png)

![image-20250327091321908](.assets/image-20250327091321908.png)

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 常见转义字符：

- 注意：如果需要在print中使用，输出内容，同时加上函数，需要使用转义字符，要加逗号和双引号，如：

print(“他的名字是：”,”\n”,name)

但若使用这个方法，会默认在两个输出内容直接增加空格，如下所示

```python
print("他的名字是：","\n",name)
# 输出结果：
他的名字是： 
 missan
```

 

- \t 一个制表位，实现对齐的功能（即添加空格）

- \n 换行符

- \\ 一个斜杠，若要输出两个斜杠，则需要输入\\\\

- \” 一个双引号

双引号也可以用单引号包裹使用：

```python
print('wow"o"')
```

 <img src=".assets/image-20250327091452901.png" alt="image-20250327091452901" style="zoom:67%;" />

- \’ 一个单引号 （单引号也可以不使用转义\）

- \r 一个回车: 如 print (“jack\rok”)中，\r后面的内容会从前面第一个字符起覆盖，最终输出内容就是 ok （无论前面多长，或前后字符数量差距多大，最终都只会输出\r后的内容）

## 2.   注释：

1. 注释的意义：尽量多去注释

 <img src=".assets/image-20250327091606810.png" alt="image-20250327091606810" style="zoom:67%;" />

2. 注释的类型：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 单行注释：#xxx

 <img src=".assets/image-20250327091618022.png" alt="image-20250327091618022" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 多行注释（单行多行都可以）：’’’注释内容’’’,或者”””注释内容”””,使用三个双引号或是三个单引号即可

（补充：若产生警告，则是因为，py会将’’’括起来的内容生成文档,此处警告是提示这段代码将用于生成文档，可以忽略）

 <img src=".assets/image-20250327091642652.png" alt="image-20250327091642652" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 注释的使用事项：注意注释**不可以嵌套使用**：即注释里面加注释，否则会报错

 <img src=".assets/image-20250327091652278.png" alt="image-20250327091652278" style="zoom:50%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 文件编码声明注释：

- 格式:# coding:编码，在文件开头加上编码声明，用以指定文件的编码格式。若不指定，则默认是UTF-8

- 编码的查看：编码的查看，可通过另存为，查看某个txt文件的编码信息

 <img src=".assets/image-20250327091759155.png" alt="image-20250327091759155" style="zoom:50%;" />

查看py文件的编码：将py文件复制到桌面，使用记事本打开，另存为即可看到

- 编码的更改：若通过#coding：gbk后，该文件就会变成gbk格式，再使用记事本另存为后，则会在编码处显示ANSI

（补充：ANSI是适应于不同系统的，如我们所使用的简体中文就是ANSI，对应的就是gbk。若使用的是繁体系统，ANSI对应的就是BIG5码）

## 3.   文档规范：

1. 使用多行注释来注释多行说明
2. 如果注释函数或者其中的某个步骤，使用单行注释
3. 等号两边都要加空格：如图

 <img src=".assets/image-20250327091835858.png" alt="image-20250327091835858" style="zoom:67%;" />

4. 变量之间使用**逗号**+空格比较规整
5. 若单行代码太长，可以在不影响的位置换行（如print等）

6. 单句代码过长，可用 \（后无空格） 换行，在[],{}，() 则可直接换行
7. 一行多个代码，用：或； 分割

## 4.python文档的查看（重要）

1. 地址：[3.12.7 Documentation (python.org)](https://docs.python.org/zh-cn/3.12/)
2. 如何使用py文档：案例：如需要查找py的内置函数abs：1.在主页找到 库参考 2.选择内置函数 3.根据首字母查找函数

## 5.变量variable：（重要）

3. 概念：变量是组成程序的基本概念，相当于内存中一个数据存储空间的表示
4. 三要素：名称，值，类型

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 注意的是：变量的名称只能有**英文，数字，和****_** ，没有空格，多个单词间用_连接：如left_days

5. 变量的注意事项：在使用前要先定义变量

![image-20250327092007411](.assets/image-20250327092007411.png)

6. 使用变量的实例：

![image-20250327092019374](.assets/image-20250327092019374.png)

7. 更改赋值：若要更改赋值，则再次定义即可

如b=2， 后面再次输入， b = 8 则会将b的值改为8

8. 变量的原理：当程序/代码执行后，变量的值是存在计算机内存的（计算机内存，即硬件内存，内存卡）
9. （补充）计算机内存：内存(Memory)是计算机的重要部件，它用于**暂时存放****CPU****中的运算类据，以及与硬盘等外部存储交换的数据**。它是外存与CPU进行沟通的桥梁，计算机中所有程序的运行都在内存中进行 

## 6.数据类型：

1. 常见数据类型（四种）：

 <img src=".assets/image-20250327092106625.png" alt="image-20250327092106625" style="zoom:67%;" />

`is_pass = True #布尔类型`

2. 数据的使用注意：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) Python 中的变量在使用前都必须赋值，变量赋值以后该变量才会被创建。

3. 数据的"类型”：是变量所指的**内存数据**的类型。如：

a=1 b= “hello”中的**ab****本身是没有数据类型的**，只有数据：1，或者是hello，分别代表了整形和字符串。有时候将其称为“字面量”

4. 数据类型的查看 ：pirnt(type(a))

其中 变量，数字，和布尔型（ture或者flase）的数据是不需要带双引号的，而字符串一定要加双引号

### 6.1数据的细节：

#### 6.1.1整形：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 整形可以表示的最大数可有4300位数字组成

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 进制：Python 的整数有十进制，十六进制，八进制，二

- 使用计算器查看进制：

（使用win自带计算器—>程序员，即可查看）

 <img src=".assets/image-20250327092324604.png" alt="image-20250327092324604" style="zoom:67%;" />

- 进制的简单介绍：（前缀具体使用查看liunx命令）

 <img src=".assets/image-20250327092343752.png" alt="image-20250327092343752" style="zoom: 67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 整形的字节与位：

- 字节(byte):计算机中（数据的）基本**存储**单元

​	位(bit):计算机中的最小存储单位

​	1byte （字节）=8 bit（位）

​	理解记忆：字节相当于房子的面积，如平米，不同字节大小可以储存不同大小的内容。

- 字节的大小：字节数随着数字增大而增大(即:python整型是变长的，这个int的大小增加，py会自动增加其字节的大小)，每次增量是四个字节，最小是24字节。详细资料：[Python中的整型占多少个字节？ - Huahua's Tech Road (mytechroad.com)](https://zxi.mytechroad.com/blog/desgin/python中的整型占多少个字节？/?%2F)

- 查看字节的大小：查看py指令 [第四章：python命令](#第四章：python命令)

 

#### 6.1.2浮点型：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 在py中，浮点型表示的形式：

- 十进制数形式，如:5.12，-5.12 或0.512（也可以写成.512, 0可以省略，但是必须要有**小数点**)

- 科学计数法形式:（其中e不区分大小写）
  - 5.12e2（等于5.12e+10）：意思是5.12 x 10的二次方

```python
# 科学计数法编写
n4 = 5.12e2# 5.12 * 10 的二次方
print("n4=", n4)
输出结果：
n4= 512.0
```

​	5.12E-2 ：意为5.12 ÷ 10的二次方

```python
n5 = 5.12E-2  # 5.12 ÷ 10 的二次方
print("n5=", n5)
输出结果：
n5= 0.0512
```

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 浮点数的范围：（大小限制）

- 边界值为:

`max=1.7976931348623157e+308`

`min=2.2250738585072014e-308`

- 如何查看浮点数信息：

```python
import sys

print(sys.float_info)
```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 注意：浮点类型计算后，存在**精度的损失**，可以使用 Decimal 类进行精确计算，如何使用decimal

- 若不适用Decimal：

```python
b = 8.1 / 3  # 2.7
print(b) #实际输出是2.699999
```

 

- 若要使用Decimal，则需要先导入Decimal类

```python
from decimal import Decimal
b = Decimal("8.1") / Decimal("3")
print("b=",b)

# 输出结果：
b=2.7
```

#### 6.1.3布尔类型（bool）：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 取值：bool形只有两个值：True和False ，True 和 False 都是关键字，表示布尔值

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 比较：布尔类型可以和其他数据类型进行比较，比如数字、字符串等。在比较时，Python 会将 True 视为 1，False 视为0

```python
# 数值的使用
a = True
 b = False
 print(a + 10)
 print(b + 10)
# 将会分别输出 11 和 10
```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 特殊：在Python中，非0被视为真值（“xx”也可以算真值），0值和None，空字符串都被视为假值（区分大小写）

```py
if 0:
print("111")
# 因为0是假，所以这条语句不会被执行4if -1:
print("222")
# 因为除0以外是真，所以这条语句会被执行

# 输出结果:
222
```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 作用：bool类型适于逻辑运算，一般用于程序流程控制：

- 条件控制语句

 ```py
 n1 = 200
 n2 = 100
 if n1 >n2:
 #此处表示判断，如果结果为真，就执行下一个指令，若为假，则不执行↓
 print("n1 >n2")
 #输出结果:
 n1>n2
 ```



- 循环控制语句

比如判断某个条件是否成立，或者在某个条件满足时执行某些代码

- 将bool值的结果赋给变量：

  ````python
  ''' 
  此处表示，将n1>n2这个结果赋予result这个值，
  因此result就是一个布尔值，只代表真或假 
  ''' 
   result = n1 > n2
   print("result=", result)
  
  print（type（result））
  
  # 输出结果：
  Ture



- bool形的查看（格式）：

 ```py
 result = n1 > n2
 print(type(result)) # 查看result的类型
 
 print(type(1 > 2))
 
 # 输出结果：
 
 <class 'bool'>
 <class 'bool'
 ```

#### 6.1.4 字符串（string）：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) str就是string的缩写，在使用type()查看数据类型时，字符类型显示的是str

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 使用引号(‘或”)包括起来，创建字符串:

- 使用案例：如想输出的字符串里包括了双引号，可以使用转义字符，也可以把外面的双引号改成单引号（单引号双引号位置可以互换）

 ```py
 str1 ='tom 说“hello”'
 ```

- print也同样适用：

 ```py
 print('wow"o"')
 ```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 通过加号可以连接字符串：

 ```py
 print ("hi"+"tom")
 # 通过加号可以连接字符串
 ```

==字符串注意事项：==

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) Python 不支持单字符类型，单字符在 Python 中也是作为一个字符串使用（别的个别语言中，单字符可能认为是字符类型)

```py
str3 = "a"
print(f"str3的类型是：{type(str3)}")
# 输出结果：
str3的类型是：<class 'str'>
```

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 用三个单引号’’’内容’’’，或三个双引号"""内容""",可以使字符串内容保持原样输出（包括**保留格式**)。在输出格式复杂的内容是比较有用的，比如输出一段代码：

- 直接使用””包括，因为文本内容复杂很容易报错：

 ```py
 content ="最棒的东西(或主意、人)to be the best thing, penson,idea,etc.
 He thinks he's the cat's whiskers (= he has a high opinion of himself)"
 ```



- 上述方法即可避免：（但注意，三个双引号（或单引号）内，不可再次出现三个双引号或单引号，否则同样会报错）

 ```py
 content =''' 最棒的东西(或主意、人)to be the best thing, penson,idea,etc.
 He thinks he's the cat's whiskers (= he has a high opinion of himself) '''
 ```



- 单独使用可以用于注释内容，具体查看[2.注释:](#2.注释：)

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 在字符串前面加'r’，可以使整个字符串不会被转义（在双引号前加上r）

```py
str4 = "jack\ntom\tking" 
#正常情况下转义符会被正常使用
print(str4)

# 输出结果：
jack
tom   king
 
#加了r之后转义字符会被显示
str5 = r"jack\ntom\tking"
print(str5) 

# 输出结果：
jack\ntom\tking
```

#### 6.1.5 ==字符串的驻留机制：==

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概念：Python仅保存一份相同且不可变字符串，不同的值被存放在字符串的驻留池中，Pvthon的驻留机制对相同的字符只保留一份接贝，后续创建相同符串时，不会开辟新空间，而是把该字符串的地址赋给新创建的变量

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 内存地址：内存地址是一个不确定的值。

赋值过程图解

 <img src=".assets/image-20250327100941531.png" alt="image-20250327100941531" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 驻留机制图解：py中，多个变量对应同一个值的时候，并不会创建多个值，而是让多个变量去**同一个内存地址**去获取这个值:

<img src=".assets/image-20250327101001309.png" alt="image-20250327101001309" style="zoom:67%;" />

 

```py
str1 = ("h")
str2 = ("h")
print("str2的地址：",id(str2))
print("str3的地址：",id(str3))

# 输出结果：
str1的地址： 140727803380312
str2的地址： 140727803380312
```

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) **驻留机制几种情况讨论：只有在该范围内才会发生驻留**

**（到交互模式下：win+r—>cmd—>python）**

1) 字符串是由26个英文字母大小写，0-9组成

- 发生驻留的情况1：（只有上述字符）

 			<img src=".assets/image-20250327101440357.png" alt="image-20250327101440357" style="zoom: 67%;" />

- 不发生驻留的情况：（即值的范围超过了上述范围） 

​			 <img src=".assets/image-20250327101455142.png" alt="image-20250327101455142" style="zoom:67%;" />

2)字符串长度为0（空字符串）或者1时（即便是上述不包含的情况）

​			 <img src=".assets/image-20250327101600202.png" alt="image-20250327101600202" style="zoom:67%;" />

3)字符串在编译时进行驻留，而非运行时

- join的意思解读：

​			 <img src=".assets/image-20250327101611785.png" alt="image-20250327101611785" style="zoom:80%;" />

- 这种情况下，ab的地址并不相同是因为，a的值是编译时就确定的，而b的值只有在运行时确定，<u>字符串只有在编译时驻留，而非运行时</u>

​							 <img src=".assets/image-20250327102031521.png" alt="image-20250327102031521" style="zoom:67%;" />

4) [-5，256]的整数数字

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 在交互模式下，强制将两个字符串指向同一个内容： 

<img src=".assets/image-20250327102045541.png" alt="image-20250327102045541" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) PyCharm对字符串进行了优化处理，不需要遵守上述规则

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 驻留机制的优势：当需要值相同的字符串时，可以直接从字符串池里拿来使用，避免频繁的创建和销毁，提升效率和节约内存

### 6.2 数据类型转换：

#### 6.2.1隐式类型转换：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概念：python的变量类型是不固定的，根据该变量使用的上下文（即当前值)在运行时决定的。，**注意不是所有语言都是这样，如 java，c等就是强制类型转换**

（如图：即通过赋值或其他手段，就可改变变量的值）

​						 <img src=".assets/image-20250327102250009.png" alt="image-20250327102250009" style="zoom:67%;" />

通过 type（变量）查看变量类型就是隐式转换，又名自动转换

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 在运算的时候，数据类型会向高精度自动转换，float的精度高于int。

```py
b= 2.1
c=a+b #3.1
print("c的类型是:"，type(c)，"c的值是:"，c) # float 3.1
b=b+0.1
plnt("b的类型是:"，type(b)，"b的值是:"，b) # float 2.2
```

#### 6.2.3显式类型转换

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概念：如果需要对变量数据类型进行转换，只需要将数据类型作为函数名即可,这种方式就是显示转换/强制转换

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 实施：以下几个内置的函数可以完成数据类型之间的转换。实施过后，函数会返回一个新的对象/值，就是强制转换后的结果

基础类型：（其余查看python手册)

​					 <img src=".assets/image-20250327102741689.png" alt="image-20250327102741689" style="zoom:67%;" />

案例1：

- j=float（i）含义：将i的值从整形转化为小数，并把这个**值**赋给j

- 输出后，j的结果是10.0是因为j的类型是浮点数

- 同理把i的值变为整形，赋给k，此时k的值相当于“10”

``` py
i = 10
j = float(i) # 将i的值变为小数，并把i的值赋给j
print("j的类型是：", type(j), "j的值是：", j)
k = str(i)
print("k的类型是：", type(k), "k的值是：", k)

# 输出结果：

j的类型是： <class 'float'> j的值是： 10.0

k的类型是： <class 'str'> k的值是： 10
```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 显式类型的转化，==注意事项==：

1）    不管什么值的**int,float**都可以转成str，str(x)将对象x转换为字符串

（对象：在python中一切皆为对象，对象如int，float等都是对象。）

```py
n1 = 100
n2 = 10.1
print(str(n1))
print(str(n2))  
# 变量本身的类型没有改变，只是输出的是改变后的变量形式
# 此时输出结果看上去还是数字，实际上已经是字符串

# 输出结果：
100
10.1
```

 

2）    int转成float时,会**增加小数部**,比如： 123->123.0，float转成int时,会**去掉小数部分**比如：123.65->123

（此时容易造成精度损失）

 ```py
 print(float(n3))
 print(int(n4))
 
 # 输出结果：
 12.0
 12
 ```



3）    str转int,float 使用 int(x),float(x)将对象x转换为int/float

- 注意：若要把str转成int/float，要求str的值本身就是一个可以转化为整数或小数的值

​	案例1：整数小数之间，无法正常转化

```py
n5 = "12.3"
print(int(n5)) 
# 此时会报错，因为n5的值不是一个整数，无法转化
```

​	案例2：字符串和整数，小数之间，都无法正常转化

 ```py
 # 值是字符串无法转化成int或float
 n7 ="hi"
 print(int(n7))
 print(float(n7))
 ```

<img src=".assets/image-20250327103608924.png" alt="image-20250327103608924" style="zoom:50%;" />

 

4）对一个变量进行强制转换,会返回一个数据/值,注意,强制转换后,并不会影响原变量的数据（原变量指向的数据/值的数据类型)

 ```py
 i = 10
 j = float(i)
 print("i的值是:",i,"i的类型是:",type(i))
 print("j的值是:",j,"j的类型是:",type(j))
 
 # 输出结果：
 i的值是: 10 i的类型是:<class 'int'>
 j的值是: 10.0 j的类型是:<class 'float'>
 ```



 

## 7．运算符

### 7.1 基本介绍：

1. 概念：运算符是一种特殊的符号，用以表示数据的运算、赋值和比较等
2. 常见预算符：

​	1)算术运算符：加减乘除，乘方等

​	2)赋值运算符：=等

​	3)比较运算符：>,<等

​	4)逻辑运算符：判断真假

​	5)位运算符：（需要二进制基础）

3. 运算符的优先级：即表达式的运算顺序

​		![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 算术运算》位运算》比较运算符》逻辑运算符》赋值运算符

​		 <img src=".assets/image-20250327104347865.png" alt="image-20250327104347865" style="zoom:67%;" />

 

### 7.2 运算符细则：

#### 7.2.1**算数运算符：**

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概念：算术运算符是对数值类型的变量进行运算的，在程序中使用的非常多

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概览：

1.  // 整除 ：

- 向下取整理解：如9/2=4.5，向下取整则是对比这个小数最近的两个整数，即5，和4，取其中较小的4

- 负数：**负数也要取较小的，如 -9//2=-5, 因为-5 比 -4 小（易错）**

- 注意和转义符[\\区分](file://区分)

- 返回结果不是小数，没有.0

 ```py
 ''' 
 整除11 结果返回的是商的整数部分（不是小数)
 且向下取整 
 ''' 
 print(10//3) # 3
 print(-9 // 2)# -5,一定要注意负数的向下取整
 ```



- **/**除号：返还的结果是小数，如果无法整除，会保留小数点后几位，如果可以整除，会保留.0

 ```py
 print(10 / 3)print(10 / 2) # 此时结果是5.0
 ```

- **：如2**4，就是2的4次方

- **%** 取模：当对一个数取模时，对应的运算公式:**a%b=a-a//b\*b**

 ```py
 print(10 % 3) # 1
 # 解折:-10 % 3= -10-(-10)//3*3 = -10-(-4)*3 = 2
 print(-10% 3) # 2
 ```

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 补充：%.2f表示保留两位小数，若没有两位，则会用0替代，根据自己的需求改变f前的内容。具体用法：

 ```py
 # 保留小数后两位
 print("华氏温度 %,2f 对应的掇氏温度是 %,2f"%(hua_shi,she_shi))
 ```

<img src=".assets/image-20250327105741759.png" alt="image-20250327105741759" style="zoom: 67%;" />

 

#### **7.2.2  **比较运算符：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概念：比较运算符的结果要么是True，要么是False比较表达式。经常用在**if****结构的条件**,为True 就执行相应的语句，为False 就不执行。

 ```py
 n1 = 1
 if n1 > -10:
     print("hi..")
 ```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 比较运算符一览：

- is ：例如：a=1 ，b=1，则 a is b = Ture

​	is指的是该变量所引用的内容，即a，b是否指向同一个数据空间。

- is not ：如：a = 1 ，b = 2 ，则 a is not b = Ture

- is和==有可能不同，即变量的值相同，但是所指向的空间不同（即未发生驻留的情况）

​		 <img src=".assets/image-20250327105947519.png" alt="image-20250327105947519" style="zoom: 67%;" />			

其中，不管是is还是==，都必须格式相同：

 ```py
 #这个案例说明了，is和== 都必须格式也相等
 a = 1
 b = str(a)
 print(a is b)# False
 print(a == b)# False
 ```

<img src=".assets/image-20250327110051029.png" alt="image-20250327110051029" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 使用案例：

``` py
# 比较符号的使用案例(部分)
a = 8
b = 9
print(a > b)
# 将a > b 的结果(即一个布尔值)赋给flag这个变量
flag = a > b
print("flag =",flag)
print(a is b)# 判断数据是否指向同一个数据空间
```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 注意：

- 比较运算符的结果要么是True，要么是False

- 比较运算符组成的表达式，我们称为比较表达式，比如:a>b

- 比较运算符 ==不能误写成=

#### **7.2.3 ** **逻辑运算符（布尔符号）：**

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 逻辑运算一览：

1. and：一假为假
   - and是种"短路运算符"，只有当第一个为True时才去验证第二个
   - 注意：and中前后是一体的，返回的结果是前后中的**结果**，**如果是数字，那就返回数字，是逻辑判断，才返回逻辑判断的结果**

```py
print(score >= 60 and score <= 80) # 注意，前后都是逻辑判断，返回结果是Ture
print(score >= 60 and 9.1 ) # 注意区分上一个，and前后是整体，此时只返回9.1
```



2. or：一真为真

<img src=".assets/image-20250327110703340.png" alt="image-20250327110703340" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 案例：

```py
a = 10
b = 20
print(a and b) # and 中，a是Ture，则返回b的值
print(0 and b) # 0是False，则返回0
print(a or b) # or 中，a是Ture，则返回a的值
print(not (a and b)) # not与后面的结果相反
```

4. **赋值运算符**：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 赋值运算符一览：

 		<img src=".assets/image-20250327110831088.png" alt="image-20250327110831088" style="zoom:67%;" />

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 注意：

- 运算顺序从右往左

​	`n = a+b+C`

- 赋值运算符的左边是变量,右边可以是变量、表达式、字面量

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 应用实例：

 ```py
 num1 =100
 i = 100
 print("i=",i)# 100
 i += 100 #这句话意为,i = i +100 = 200
 print("i=",i)# 200
 # 此处可见，python是按照从上至下的顺序运行
 i -= 100
 print("i=",i)# 100
 i *= 3
 print(i) # 300 
 ```

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 交换赋值的应用实例：

```py
# 交换ab变量的值
'''
思路分析：
1）定义一个中间变量temp
2）将a的值赋给temp
3）把b的值赋给a，再把temp赋给b 即可
'''
a = 100
b = 200
print(f"没有交换前，a={a},b={b}")
temp = a
a = b
b = temp
print(f"交换后，a={a},b={b}")
"""
在python中，有更简便的变量交换方式：
x , y = y , x
"""
a = 100
b = 200
print(f"没有交换前，a={a},b={b}")
a , b = b , a
print(f"交换后，a={a},b={b}")
```

#### 7.2.4 **三元运算符**：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 概念：Python 是一种极简主义的编程语言，它没有引入?:这个运算符，而是使用 if else 关键字来实现相同的功能

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 语法: `max= a if a>b else b`

1)如果 a>b 成立,就把 a作为整个表达式的值,并赋给变量 max

2)如果 a>b不成立,就把 b作为整个表达式的值，并赋给变量 max

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 应用：

通过三元运算符，得到两个数的最小值

```py
min = a if a < b else b
print(min)
# 通过三元运算符，得到三个数的最大值
a = 1
b = 10
c = 100
d = a if a>b else b
max1 = c if c>d else d
print(f"abc中的最大值是：{max1}")

#输出结果：
abc中的最大值是：100

'''
使用一条语句完成(可读性较差，不推荐)
用于了解()的优先级是最高的
'''
max2 = (a if a>b else b) if (a if a>b else b)>(c if c>d else d) else (c if c>d else d)print(f"abc中的最大值是:{max2}")
```



 

## 8. 标识符

1. 概念：Python 对各种**变量、函数和类**等命名时使用的字符序列称为标识符。凡是自己可以**起名字的地方**都叫标识符，如：`num1=90`
2. 命名规则：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 由26个英文字母大小写，0-9，_组成

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 数字不可以开头

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 不可以使用关键字，但能**包含关键字**

（查看下一节[**9.关键字:**](#_9.关键字：)，即系统规定的部分字母组合，如if，else，class等等）

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) Python分大小写

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 标识符不能包含空格

3. 标识符命名规范（专业）：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 变量：变量要小写,若有多个单词,使用下划线分开。

常量：全部大写 （常量：即恒定不变的量，如PI）

- 案例：

```
my_name = “lucy”
PI = 3.14
```



![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 函数：函数名一律小写,如果有多个单词，用下划线隔开。私有函数以双下划线开头，如__private_func

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 类:使用大驼峰命名

- 知识扩展:

​	1.驼峰命名法有两种,大驼峰命名和小驼峰命名

​	2.大驼峰命名,多个单词的首字母用大写开头，比如:MyName

​	3.小驼峰命名,第1个单词的首字母用小写, 后面的单词首字母都大写,例如: myName

## 9.关键字：

1. 概念：被Python语言赋予了特殊含义，用做专门用途的字符串(单词)
2. 以下标识符为保留字，或称 关键字，不可用于普通标识符（变量名，函数，类名）。关键字的拼写必须与这里列出的完全一致: 

 <img src=".assets/image-20250327112200143.png" alt="image-20250327112200143" style="zoom:67%;" />

3. 关键词的查看：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 进入python的交互模式，输入help（)，keywords即可

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) [2. 词法分析 — Python 3.13.0 文档](https://docs.python.org/zh-cn/3/reference/lexical_analysis.html#identifiers)

## 10. 键盘输入

1. 概念：在编程中，需要接收用户输入的数据，就可以使用键盘输入语句来获取
2. 相关函数 input（）

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 介绍：input（prompt）如果存在 prompt实参（即提示信息），则将其写入标准输出，末尾不带换行符。接下来，该函数从输入中读取一行，将其转换为字符串(除了未尾的换行符)并返回。当读取到 EOF时，则触发 EOFError。

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 使用案例：

如name = input（“请输入姓名：”），回车执行后，控制台会等待用户输入内容

```py
# 要求:可以从控制台接收用户信息，【姓名，年龄，成绩】
ame = input("请输入姓名： ")
age = input("请输入年龄： ")
score = input("请输入成绩： ")

print(f"\n输出的信息如下 \n 姓名： {name} \n 年龄：{age} \n 成绩:{score}")
 
# 输出结果：
 
请输入姓名： missan
请输入年龄： 19
请输入成绩： 99
 
输出的信息如下 
 姓名： missan 
 年龄：19 
 成绩:99
```

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 细节注意：从控制台输入的内容是str，即使是数字

```py
# 注意：从控制台输入的内容是str，即使是数字
print(10 + int(score)) #直接相加会报错
# print(10 + score) 这样是错误的
 
# 输出结果：
20
<class 'str'>
```

- 也可以在接收数据的时候，直接转成需要的类型：

```py
score_2 = int(input("请输入成绩2："))
print("成绩2的类型是：",type(score_2))
 
# 输出结果：
请输入成绩2：20
成绩2的类型是： <class 'int'>
```

## 11 .进制

### 11.1 进制说明：

1. 整数的表达形式：

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 2进制: 0,1，满2进1 , 以0b或0B开头。

如：`print（0b111）`此处的111不是十进制的111，而是二进制的111

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 8进制:0-7，满8进1，因此**没有8这个数字**，二级制的8对应8进制的10。以数字0o或者0O开头表示。

如：`print（0o111）`此处的111不是十进制的111，而是8进制的111

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 10进制:0-9，满10进1。

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 16进制:0-9及A(10)-F(15)，满16进1.以0x或0X开头表示。此处的A-F不区分大小写

2. ==进制的图示：==

   <img src=".assets/image-20250327112701212.png" alt="image-20250327112701212" style="zoom: 67%;" />

注意：x进制中不会有x，如8进制没有8，2进制没有2

  							<img src=".assets/image-20250327184244248.png" alt="image-20250327184244248" style="zoom:67%;" />     

### 11.2：其他进制转十进制

#### 11.2.1二进制转十进制：

1. 规则：规则:从最低位(右边)开始，将每个位上的数提取出来，乘以**2**的(位数-1)次方，然后求和。

   <img src=".assets/image-20250327184346547.png" alt="image-20250327184346547" style="zoom:67%;" />

2. 案例：将0b1011转化为十进制

3. 从右往左第一位是1，得到 1*2（1-1）次方 

4. 同理可得：1*2（2-1）次方 + 1*0（3-1次方）+1*2（4-1）次方

5. 将以上数相加可得，0b1011的十进制=11

#### 11.2.2 八进制转十进制：

1. 规则:从最低位(右边)开始，将每个位上的数提取出来，乘以**8**的(位数-1)次方，然后求和。
2. 案例：将0o234转化为10进制

​			 <img src=".assets/image-20250327184445134.png" alt="image-20250327184445134" style="zoom:50%;" />

#### 11.2.3 十六进制转十进制

1. 规则：规则:从最低位(右边)开始，将每个位上的数提取出来，乘以16的(位数-1)次方，然后求和。
2. 案例：将0x23A转化为十进制

​		 <img src=".assets/image-20250327184632815.png" alt="image-20250327184632815" style="zoom:67%;" />

### 11.3 十进制转其他进制

 **一. 十进制转二进制：**

1. 规则:将该数不断除以2，直到商为0为止，如果余数无法再除，则保留余数，然后将每步得到的**余数倒过来**，就是对应的二进制。
2. 案例：求34的二进制
3. 34/2 =17余0, 17/2=8 余1, 8/2=4余0,4/2=2余0, 2/2=1余1

 				<img src=".assets/image-20250327185307425.png" alt="image-20250327185307425" style="zoom:67%;" />

2. 将余数**反过来**组合起来：0b100010
3. 验算：通过bin（数字）来将十进制转二进制

 ```py
 print(bin(34)) # 0b100010
 ```



 **二. 十进制转八进制：**

1. 规则：将该数不断除以8，直到商为0为止，然后将每步得到的余数倒过来，就是对应的八进制。
2. 案例：将131转化为八进制
3. 131/8=16, 余3,16/8=2余0，
4. 倒过来得到，131的八进制是：0o203
5. 检验：oct(x),将整数转为八进制

检验结果正确。

 ```py
 print(oct(131)) # 0o203
 ```

**三. 十进制转十六进制**

1. 规则:将该数不断除以16，直到商为0为止，然后将每步得到的余数倒过来，就是对应的十六进制。
2. 案例:请将 237 转成十六进制
3. 237/16=14 余 13
4. 13是D，14是E，最终结果是0xED

​    3. 检验：hex（x）将整数转化为十六进制

       ```py
       print(hex(237)) # 0xed
       ```

### 11.4 二进制转其他进制

**一. 二进制转八进制：**

1. 规则:从低位（右边）开始,将二进制数**每三位一组**（若不够三位就独立成组），转成对应的十进制后再转为八进制数即可，注意最后转换的结果按原来的顺序。
2. 案例：将0b11（3）010（2）101（5）转化成八进制=0o325

​				 <img src=".assets/image-20250327190023307.png" alt="image-20250327190023307" style="zoom:50%;" />

**二. 二进制转十六进制：**

1. 规则：从低位开始，将二进制数每**<u>四位一组</u>**，转成对应的十六进制数即可。
2. 案例：将11010101转化为16进制：
3. 从右往左分为：1101,0101两组
4. 1101换成10进制是13，转化为16进制是D

0101转化为十六进制是5

3. 因此0b11010101=0xD5

**三. 八进制转二进制：**

1. 规则：将八进制数每1位，转成对应的一个**3****位的**二进制数即可，若不足三位，在开头补0，最开头的0可以省略
2. 案例：将0o237转化为二进制
3. 7=111， 3=11—>补0:011, 2=010（第一个0可以省略）
4. 得到：0o237=0b10011111

**四. 十六进制转二进制：**

1. 规则：将十六进制数每1位，转成对应的**4****位**的一个二进制数即可
2. 案例：将0x23B转为二进制
3. 2=10 ，3 =0011 ，B=0d11=1011
4. 0x23B =0b1000111011

#### 11.4.1 二进制在使用过程中的其他说明

**基本介绍：**

1. 概念：二进制是逢2进位的进位制，0、1是基本数字符号。
2. 应用：现代的电子计算机技术全部采用的是二进制,因为它只使用0、1两个数字符号,非常简单方便,易于用电子方式实现。

### 11.5 原码，反码，补码==（重难点）==

#### 11.5.1 概念：

**1. ** **结论1：进制的最高位是符号位:0表示正数,1**表示负数（需背）

​	解释：

​	![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 最高位：即二进制数最左侧的数字

​	![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 正负如何用01表示：

- ==案例：==

​	先假设，3只有1字节（1字节包括8位二进制）则

​	3 ——> 二进制：0000 0011 最左侧是0，因此表示正3

​	-3 ——> 二进制：1000 0011 最左侧是1，因此表示负3



2.结论2:  **正数**的原码，反码，补码都是一样的**（三码合一**）

![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) 案例：3  > 原码：0000 0011

 反码：0000 0011

补码：0000 0011



3.结论3：负数的两种情况

​	![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) **反码：原码的符号位不变，其他位取反（即0 ——> 1**)。还等于补码-1

- ​	案例：-3原码：1000 0011 ——> 反码：1111 1100

​	**（符号位不变）**

​	![*](file:///C:/Users/a/AppData/Local/Temp/48D01C6B.gif) **补码=** **反码+1** （即最小位变成1)

- ​	案例：-3反码：1111 1100 ——> 补码：1111 1101

  

4.结论4：0的补码，反码都是0



**6.**结论5： **在计算机运算的时候，都是使用补码来运算**：

- 案例1：

1.  1 + 3 在计算机中，是先分别找出他们的补码，然后进行运算

2.  1原码：0000 0001à补码：0000 0001
3.  3原码：0000 0011 à补码：0000 0011
4.  相加：0000 0001 + 0000 0011= 最后两个1相加，进一变成0，,左一位进一变成0，左二位进一变成1

得到结果：0000 0100à原码：0000 0100à4

7. 结论7：当我们看运算结果的时候，要看他的原码(如案例一)：

- 案例2: 

1. 1-3= 1补码à0000 0001 
2. -3原码:1000 0011à反码：1111 1100à反码+1à补码：**1111 1101**
3.  1-3=1+(-3)= 0000 0001 + 1111 1101（用补码运算）**=1111 1110** **补码（运算规则看案例1**）

5. 将结果的补码转化为原码：

   先转化为反码：1111 1101 ——> 转为原码：1000 0010 =-2

## 12. 常见文件模式

<img src=".assets/image-20250403110225449.png" alt="image-20250403110225449" style="zoom: 33%;" />

1. 注意：w会覆盖原文件内容，谨慎使用

# 第四章：python命令

**使用注意：在cmd使用python指令时，需要先输入python，进入python的开发环境。**

## 1. 基础命令：

注意：在python中，单引号和双引号的使用完全一样

### 1.1 print

1. 基础语句：

```py
print（“ xx ”） # 向终端输出引号内的内容，注意引号要用英文
```

![*](assets/3DE29788.gif) `print（”xx”,某函数)`

则表示，先输出括号里的内容，然后输出函数内容

如 :

`b = 1  print（"b的值是”, b）`，则会输出：`b的值是1`

![*](assets/3DE29788.gif) 输出内容的同时，后面要加某函数或者变量，同时换行：

`print（“名字是：”，“\n”,name）`

但若使用这个方法，会默认在两个输出内容直接增加空格。 **可使用%s，会更加便捷**

```py
print("他的名字是：","\n",name)

# 输出结果：
他的名字是： 
 missan
```

2.  打印100个hello，且带编号

```py
for i in range(100):
 print("Hello %d" % i)
```

- 其中：%d 是格式化占位符，表示输出一个整数(即带编号)。还有其它，如果%s 表示输出一个字符串，%f 用来输出一个小数（浮点数）。

- 第二个 % 是 python 参数的分隔符，表示 % 后面的内容用来替换 "%d”

#### 1.1.1 格式化输出（format_output)：

1. %+规定字母 ,用于将后面的内容填补进来

​	 使用（以%s举例）：

```py
print("名字是：%s" %(name))

# 输出结果：
名字是：missan

'''
意思解读：%s 在" "内部，
%s位置的内容会用后面%（xx）中的xx来填补。
（注意，%（xx）前面没有逗号）
'''
```

​     <img src=".assets/image-20250327193617444.png" alt="image-20250327193617444" style="zoom:67%;" />

   作用：**便于使用各种转义符和格式**，且因为%在””内部，因此在%前后的空格，也会被如实显示。如：

```py
print("名字是：\n %s" %(name))

#输出结果：
名字是：
missan
```

- 如何同时输出多个不同格式的内容：

  如同时输出字符串和整形 : 其中**%后加不同字母表示填补的内容的格式不同**，如

  %s（string）表示字符串

   %d表示整形

  %.(某数字)f 表示浮点数（看[^补充1]）

  %（a，b）中，**多个内容需要用逗号间隔**。如：

```py
# 同时输出 字符串，整形 和 浮点数
 print("个人信息：%s %d %s %.2f" %(name , age ,gender ,score))

#输出结果：
个人信息：missan 19 女 99.90
```



2. ==format ，原理同 %，更实用==（最常使用）

- 使用方法：同%，在””内加入{} ,数量与后面需要输出的内容相对应即可。在format前要加 “.” ，format后的括号内，变量用逗号间隔

- 使用案例：

```py
print("个人信息：{} {} {} ".format(name , age , score))

#输出内容：
个人信息：missan 19 99.9
```

- 补充：若如图，在变量前自动出现一个*args （argument），意思是提醒你这是一个参数列表

 <img src=".assets/image-20250331154830526.png" alt="image-20250331154830526" style="zoom:67%;" />

- 更多用法：[Python format 格式化函数 | 菜鸟教程 (runoob.com)](https://www.runoob.com/python/att-string-format.html)

3. f-strings ，原理同上，但是系统会自动从上面定义的变量中调用。**<u>最为简单</u>**

- 使用：在””前加f，在””内加{变量名}即可

```py
print(f"个人信息：{name} {age} {gender} {score}")

#输出结果
个人信息：missan 19 女 99.9
```

- 与函数结合使用，如：

```py
print(f"hello的类型是：{type("hello")}")

#输出结果：
hello的类型是：<class 'str'>
```

- 更多用法：[python fstring教程（f-string教程）（python3.6+格式化字符串方法）（%惰性格式化%）-CSDN博客](https://blog.csdn.net/Dontla/article/details/139270178?utm_medium=distribute.pc_feed_404.none-task-blog-2~default~BlogCommendFromBaidu~Rate-2-139270178-blog-null.262^v1^pc_404_mixedpudn&depth_1-utm_source=distribute.pc_feed_404.none-task-blog-2~default~BlogCommendFromBaidu~Rate-2-139270178-blog-null.262^v1^pc_404_mixedpud)



### 1.2 变量：

（注意：该变量只有在pycharm中设置模版时使用，前面有#，依然可以正常运行）

![*](assets/3DE29788.gif) ${NAME} 显示文件名

![*](assets/3DE29788.gif) ${DATE} 显示日期  ${TIME} 显示时间

![*](assets/3DE29788.gif) 变量的赋值：其中赋值有各种形式

- 变量三要素：名称，值，类型
  - a=1 其中1是一个**整形**，输入整形和浮点型时不需要加双引号（**即纯数字不需要双引号**）
  - b=9.1 其中9.1是一个**浮点型**
  - name=”tom” tom是一个**字符串**，在用字符串给变量赋值的时候要加双引号

- 一次性给多个变量赋值：
  - a,b,c=1,2,”3”

![*](assets/3DE29788.gif) 更改赋值：若要更改赋值，则再次定义即可：

如b=2， 后面再次输入， b = 8 则会将b的值改为8

![*](assets/3DE29788.gif) 输出变量：

- 使用print(b) 即可，或者可以使用：print（"b的值是”, b）

- 使用print（type（a））即可查看变量类型（即输出赋予a的值的类型），组合使用 ：print（“a的类型是”，type（a））

​					 <img src=".assets/image-20250331155559260.png" alt="image-20250331155559260" style="zoom:67%;" />

![*](assets/3DE29788.gif) 变量的注意事项：在使用前要先定义变量，否则会报错：not defined。也不可以先使用变量，再定义变量，因为py是按顺序执行的

### 1.3 运算符

#### 1.3.1 运算符一览

1. 加号

![*](assets/3DE29788.gif) 当左右两边都是数值型（即整形和浮点型)时，则做加法运算，如：

```py
score = 90.8
print(score + 90)
#输出内容：
180.8
```

![*](assets/3DE29788.gif) 当左右两边都是字符串，则做拼接运算，注意另一边的**字符串如果不是事先定义的变量**，则需要加上””,如：

```py
name = "lucy"
print(name + " is good")
#输出内容：
lucy is good
```

- 注意：如果用””把数字包起来，那里面的数字也表示字符串，如：

```py
print("100" + "90")  # 依然是字符加字符
#输出结果：
10090
```

- 字符+数字，会报错

2. ** 表示次方，如3 ** 2 表示3的二次方
3. / 表示除号：8 / 2 = 4
4. 运算符:

![*](assets/3DE29788.gif) 比较字符一览：

 <img src=".assets/image-20250331161513661.png" alt="image-20250331161513661" style="zoom: 80%;" />

1. is的浅拷贝：

- 根据数据驻留原理，c，d的值123，指向的是同一个数据，因此两者相同
- a，b是两个列表，不适用数据驻留，两者看似一样，实则指向的内容并不相同

```py
c = 123
d = 123
print(c is d) # Ture

a = [1,2,3]
b = [1,2,3]
print(a is b) # False
```

2. is的深拷贝：

```py
a = [1,2,3]
b = list(a)
print(a is b) # False
```



![*](assets/3DE29788.gif) 算数运算字符一览：

 <img src=".assets/image-20250331161532641.png" alt="image-20250331161532641" style="zoom:80%;" />

![*](assets/3DE29788.gif) 逻辑运算符一览：其中and的优先级>or

 <img src=".assets/image-20250331161600352.png" alt="image-20250331161600352" style="zoom:80%;" />

1. and短路效应：

   and的顺序是从前往后判断，如果前一项错误，则不会继续判断后一项，直接返回False

```py
s=((2>3)and(n:=2>1))
print(s) # False
```

2. or的短路效应：只有前一项是False才会执行后一项

```py
c = (2>3)
c or print("right") # right

d = 1
d or print("False") # 不输出内容
```

![*](assets/3DE29788.gif) 赋值运算符一览：

 <img src=".assets/image-20250331161612825.png" alt="image-20250331161612825" style="zoom:80%;" />

#### 1.3.2 三元运算符

 三元运算符：

`max = a if a>b else b `

即取ab中的最大值

```py
# 通过三元运算符，得到两个数的最小值
min = a if a < b else b
 print(min)

# 通过三元运算符，得到三个数的最大值
 a = 1
 b = 10
 c = 100
 d = a if a>b else b
 max1 = c if c>d else d
 print(f"abc中的最大值是：{max1}")

# 输出结果：
abc中的最大值是：100

```

#### 1.3.3 赋值运算：

<img src=".assets/image-20250402203630691.png" alt="image-20250402203630691" style="zoom: 50%;" />

1. 海象运算符：“：=”

   复制并直接判断，用于简化代码

```py
# 源代码
date = [1,2,3,4]
n = len(date)
if n > 3:
    print(f"数据过长，有{n}条数据")
    
# 使用海象简化
date = [1,2,3,4]
if (n:= len(date)) > 3:
    # 这里外面如果不加括号，那n的值就是Ture，而不是4
    print(f"数据过长，有{n}条数据")
```

- 注：海象运算符不要使用过多，不然会减少代码可读性。使用时最好用括号包裹

### 1.4 数据类型：

type(object) ,查看数据类型，其中object可以指的是具体的数据（即**字面量**），也可以是一个**变量（即查看变量所指向的数据类型）**

![*](assets/3DE29788.gif) 注意：如 type（a）是查看a变量的类型，而type（”a”)则是查看a这个字符串的类型。

![*](assets/3DE29788.gif) 其中 变量，数字，和布尔型（ture或者flase)的数据是不需要带双引号的，而字符串一定要加双引号

1. 输出整形的进制：

![*](assets/3DE29788.gif) 十进制：直接输出即可

![*](assets/3DE29788.gif) 十六进制：在对应的16进制数字前加上**前缀****0x**，输出的便是该数字在十进制中表达的数字（相当于**翻译成十进制**)：

```py
print(0x10) # 此处是16进制

# 输出结果：
16
```

![*](assets/3DE29788.gif) 八进制：同理，加上前缀：**0o**

```py
print(0o10) #此处是8进制

# 输出结果：
8
```

![*](assets/3DE29788.gif) 二进制：加上前缀0b：

```py
print(0b10) #此处是2进制

# 输出结果：
2
```



2. 查看对象（可以是任何类型）的大小：`sys.getsizeof `，按照字节单位返回大小 。（若显示没有定义的，在前一行加上：import sys）

（若查看的数字大小增加，返回的字节大小也会随之增大，但若数字非常相近，则返回字节可能差不多：如0,1,2）

```py
a = 0
print(sys.getsizeof(a),"类型",type(a))

# 输出结果：
28 类型 <class 'int'>
```

3. 如何查看浮点数信息：

```py
import sys

print(sys.float_info)
```

- 使用Decimal精确计算浮点数：

```py
from decimal import Decimal #导入Decimal
b = Decimal("8.1") / Decimal("3")
print("b=",b)

# 输出结果：
b=2.7
```

### 1.5 条件&循环语句

#### 1.5.1 if的使用：

![*](assets/3DE29788.gif) 真假判断：若条件为真，则执行命令，条件为假，则不执行，

- 注意：在python中，除了0，None，空字符串以外，其余一切都属于真

- 情况1：

```py
n1 = 200
n2 = 100

 if n1 > n2:
#此处表示判断，如果结果为真，就执行下一个指令，若为假，则不执行
   print("n1 > n2")

# 输出结果：
n1>n2
```

- 情况2：

```py
# 在Python中，非0被视为真值（“xx”也可以算真值），0值被视为假值

if 0:
    print("111")  
# 因为0是假，所以这条语句不会被执行
if -1:
    print("222")  
# 因为除0，None，空字符串以外是真，所以这条语句会被执行

# 输出结果：
222
```

 

![*](assets/3DE29788.gif) 前后判断：== 表示，判断前后是否一致

 ```py
 # 两个等号表示判断前后是否相等
 a= True
 b = False
 if a == 1:
 	print("ok")
 if b == 0:
 	print("hi")
 
 # 输出结果:
 ok
 hi
 ```

#### 1.5.2 for的使用：

1.  基础语句：

```py
for <变量> in <范围/序列>:
	<循环操作语句> # 循环体
```

- <范围/序列> :可以是字符串或列表
- <循环操作语句> ：可以有多条语句
- 循环的次数是由数据集或范围来决定的

应用实例：

```py
num=[1,2,3,4,5] 
# 定义一个列表,可以视为一个数据集
print(num,type(num)) # 查看类型：<class 'list'>

for i in num: # 每次循环的时候，依次将nums中的值取出赋给i
	print("hello , world") # 打印五次hello，world
```

流程图：

<img src=".assets/image-20250401174100179.png" alt="image-20250401174100179" style="zoom: 30%;" />

列表内容的存储：查看[6.1.5 字符串的驻留机制：](6.1.5 字符串的驻留机制：)

<img src=".assets/image-20250401180254917.png" alt="image-20250401180254917" style="zoom: 33%;" />

```py
name = "world"
for i in [1, 2, 3]: # 此处是一个列表
    print(f"Hello {name} {i}")
    
# 输出结果： 
Hello world
Hello world
Hello world
```

#### 1.5.3 while循环

### 1.6 读取

#### 1.6.1读取文件：

- 基础语句：读取某txt文件内容并统计行数

```py
with open(r"D:\file.txt") as f: # r注销转义
    # 此处要写清楚路径
    # 打开 file.txt并把该行为写入变量f
    
    lines = f.readlines()
    # 变量line等价于：打开并读取文件内容
    
print(len(lines),lines) # len()统计行数
```

- 若不指定文件格式，默认无法正常读取含中文的文件：
  - 若有中文，则会读取成乱码
  - 有中文字符则会报错
  - 在进阶使用中，通过指定格式utf-8来正常读取中文文件
- 读取的文件会包含换行符
- with ：用安全模式打开文件，在使用完后自动关闭
- open(file_path) ：默认用**只读模式**打开文件
- as f 相当于f =，给文件路径取别名f（用于后文引用）
  - 进阶使用：检查文件是否存在，不存在则返回：“文件不存在”

```py
import os # 导入工具插件os
file_path = r"D:\file.txt" # 给文件路径命名

if os.path.exists(file_path): # 检查路径是否存在
    with open(file_path,encoding='utf-8') as f:
        lines = f.readlines()
    print(len(lines))
else:
    print("文件不存在！")
```

- import 导入
- encoding=‘utf-8’  ：加在路径后面，指定文件格式
- os：管理电脑文件的工具包

  - os.path.exists(路径）: os的功能之一，用于检测目标文件是否存在 

#### 1.6.2 **读取键盘输入内容input：**

1. 基础语法

```py
a = input("需要输出的提示词")
print(f"hello,{a}")
```

- input后的括号若为空，则不输出任何内容
- 默认返回一定是字符串类型

2. 使用实例:

```py
# 输出欢迎词
name = input("请输入您的名字：")
print(f"hello,{a}")

# 类型转化
age = int(input("输入年龄")) # 转化为int
```

3. 多值输入：

```py
# 多值输入
inform = input("输入两个数字（用空格分割）：").split( )
print(f"{inform}") # 输出： ['1', '1']
```

- .split( ) 的作用是把两个输入内容分割成两个列表，用空格区分输入内容
- 若在输入过程中，两个字符**没有用空格分割**，则会输出：['11']
- split使用：[1.8 split](#1.8 split)

4. 默认值的实用：

```py
color = input("请输入颜色（默认蓝色）") or "蓝色"
print(color)
```



5. 常见错误处理：

```py
# 类型错误
age = input("请输入年龄：")
print(age+1)
# 此处会报错，因为默认是str，不能与数字相加

#正确写法：
age =int(input("请输入年龄："))
print(age+1)
```




### 1.7 自定义函数def

1. 基础语法

```py
def <函数名>(参数列表):
   <函数内容>
<函数名>(参数内容) # 调用函数
```

2. 使用：

```py
def greet(name): # 函数名和参数
    print(f"Hello {name}")
greet("Alice")
```

### 1.8 split

1. 基础语法：将输入内容按括号中内容分割成列表

```py
.split( ) # 按空格分割
.split(",") # 按逗号分割
```

- 注意，此处**按什么分割**，并不是指输出结果用什么分割，而是输入内容用什么分割，例：

  ```py
  a=input().split(",")
  print(a)
  
  # 输入：abcd # 输出：['abcd']
  # 输入：a b c d # 输出：['a','b','c','d']
  
  # 对比不加split
  a=input()
  print(a)
  # 输入：abcd # 输出：abcd
  # 输入：a b c d # 输出：a b c d
  ```

  由这个案例可见，input输出的结果是一个**列表**

2. 应用案例1：

- 打包

```py
inform = input("输入两个数字（用空格分割）：").split( )
print(f"{inform}") # 输出： ['1', '1']
```

- 打包并赋值：

```py
value = input("输入2数字（用空格分割）：").split( ) # 1 2
num1,num2 = map(int,value)

print(f"num1={num1},num2={num2}") # num1=1,num2=2
```

问题：若用户只输入一个数字（或未用空格分割）第二步会报错：
解决:见[2.1 异常处理try：](#2.1 异常处理try：)第一个案例

### 1.9 ==列表，字典==

#### 1.9.1 列表

1. 基础语法：
2. 更改列表内容的数据类型：ma

- 基础语法

```py
map(数据类型，列表名)
map(str,num)
```



```py
value=[1,2,3,4]
str_value=map(str,value) # 更改类型后赋给新的值
num1,num2,num3,num4=str_value
print(type(num1))

```



### 1. * 其他：

1. id（），返回对象/数据的内存地址

2. x , y = y , x 交换变量的值

```py
"""
在python中，有更简便的变量交换方式：
x , y = y , x
"""
a = 100
b = 200
print(f"没有交换前，a={a},b={b}")
a , b = b , a
print(f"交换后，a={a},b={b}")
```

3. 从变量中间取值：

```py
a = “12345a9b”
print(a[0,1,4]) # 取1,2,5个值
# 输出： 1,2,5

a = 1234
print(a[0,1,3]) # 若a是int/float，该方法则无法取值
```

## 2. 应用进阶：

### 2.1 异常处理try：

1. 基础语法：当python程序运行时，可能会因为各种原因发生异常导致程序无法正常运行，此时可以通过try/expect来排查并解决异常

```py
try:
<语句>        #运行别的代码
except <名字>：
<语句>        #如果在try部份引发了'name'异常
except <名字>，<数据>:
<语句>        #如果引发了'name'异常，获得附加的数据
else:
<语句>        #如果没有异常发生
```

2. 应用案例1：

   用户需要输入两个整数，否则会返回开头无限循环

```py
while True:
    value = input("输入2数字（用空格分割）：").split( )
    if len(value) != 2 :
        print("请输入两个数字！")
        continue 	#输入内容无效则循环
    try:
        num1,num2 = map(int,value)
        break 		# 如果输入有效数字，则退出循环
    except ValueError:
        print("不是有效整数！")
        continue
print(f"num1={num1},num2={num2}")
```

2. 应用案例2：

```py
# 读写文件
def write_mode():
    try:
        with open(r"D:\code\test_fil.txt","r+",
                  encoding="utf-8") as ow:
            ow.write("测试异常1")
    except FileNotFoundError:
        print("Error：未找到该文件！")
    else:
        print("写入内容成功！")
write_mode()
```



### 2.* 其他

1. 提取输入值并打印：

   ```py
   def main():
       s = input()                           # 读取输入
       s = [e.split('=')[1] for e in s.split(',')]  # 提取等号后的值
       print(' '.join(s))                    # 用空格拼接结果
   
   if __name__ == '__main__':  # 注意这里是双下划线
       main()
   ```

2. 





 

 

 

 

 

 

 

[^补充1]: 补充1：关于浮点数：%.2f表示保留两位小数，若没有两位，则会用0替代，根据自己的需求改变f前的内容

% 的更多使用：[Python之格式化输出(print %)_python print %-CSDN博客](https://blog.csdn.net/hesongzefairy/article/details/104179419) 