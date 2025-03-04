[toc]





# markdown学习

## 1. 标题

“ # ” 一级标题

“ ## ” 二级标题

以此类推

## 2. 引用

">" 引用内容

> 你好
>
> markdown教程：https://www.bilibili.com/video/BV1JA411h7Gw/?spm_id_from=333.337.search-card.all.click&vd_source=1f9a658b3c0816438bea2f3933a0f8e9

通过 “shift + tab" 退出引用

## 3.目录

通过 “ [toc] "添加目录

## 4.创建有序/无序列表

1. 有序列表：输入1. +空格，输入内容，回车换行后会自动创建有序列表

1. a
2. b
3. c

2. 无序列：输入：- ，* +空格

- hello
- b

**shift + tab 退出**

## 5.字体

1. 斜体： * a * （空格删掉）

   *斜体*

   *测试*

2. 粗体 ：** a ** （空格删掉）

   **粗体**

   **测试**

3. 下划线：把空格去掉即可

   <u>abc </u>  <u> abc</u>

5. 下标：用一对波浪号包裹起来 ~下标~

6. 上标：用一对上箭头包裹起来：^上标^

7. 高亮：用四个等号包裹起来：==高亮==

8. 

## 6. 任务列表

-[x] 中间加空格即可

- [x] 成功
- [ ] 成功
- [x] 成功

## 7.代码块

1. 单代码：使用两个"```"或 反引号 把内容括起来即可：

```print("hello") ```

2. 代码块：输入 ``` 换行即可

   输入代码后，可以在右下角输入代码的语言，会自动标亮

``` c
#include <stdio.h>
int main() {
    printf("Hello, World!\n");
    return 0;
}
```

3. 可以在句子中间插入代码：

1111``print("ok")``好的

## 8.数学公式

用$$ xx $$ 把公式填入xx位置即可
$$
\frac{\partial f}{\partial x}= 2\sqrt{a}x
$$


## 9.表格

|： | ：|： 回车即可

改成英文输入法

| 姓名 |年龄 | 性别 

| : --- | : -- |
| ----- | ---- |
|       |      |

| :    | :    |
| ---- | ---- |
|      |      |



| 姓名 | 年龄 | 性别 |
| ---- | ---- | :--- |
| xm   | 是   | 啊   |



## 10.脚注

111+[^动物 ]

按住ctrl +点击 该脚注，即可跳转到脚注位置，并且编辑该脚注内容

## 11.横线

三个短横：

---

111

## 12.链接

1. [网站名称]（网址"双引号可以注释内容，可加可不加"）

如：

[markdown教程](https://www.bilibili.com/video/BV1JA411h7Gw/?spm_id_from=333.337.search-card.all.click&vd_source=1f9a658b3c0816438bea2f3933a0f8e9 “教程”)

2. [网址名称][id] -->id处的内容可以填自己需要的网址

   这个方法的好处是，后续需要同一个网站，只要复制这一行即可

   如果需要更改链接内容，**只需要** 更改id后面的内容即可

3. [id]:https://www.bilibili.com/video/BV1JA411h7Gw/?spm_id_from=333.337.search-card.all.click&vd_source=1f9a658b3c0816438bea2f3933a0f8e9

4. 跳转文内标题：请查看[1.标题](#1.标题)

5. 图片: ![图片](链接"可以通过双引号添加注解，可加可不加")

   ![图片](https://img-blog.csdnimg.cn/2021051521244130.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl81MzQ0Nzc3Ng==,size_16,color_FFFFFF,t_70"星空图片")

   
   
## 13. 视频



复制b站的视频嵌入代码即可

## 14.放大缩小界面

1. ctrl + shift +=   放大界面
2. ctrl + shift + -   缩小界面



## 15.大纲消失如何解决

[解决方案](https://blog.csdn.net/QCSYSZQ/article/details/113472179)

切换到代码模式：ctrl +/ , 把**所有**不在大纲中的部分选中，按shift+tab即可

## 16.图片

1. 除了链接中插入图片的方法外，图片也可以直接复制黏贴

2. 图片大小调整：右键图片，选择图片缩放，调节想要的尺寸。调节完毕后，图片的链接中会出现zoom，修改后面的数字也可以调整图片大小

   ​                  





















[^动物 ]: 猫，狗
