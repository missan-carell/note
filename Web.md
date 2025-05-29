# Web

学习推荐：[3小时前端入门教程（HTML+CSS+JS）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.337.search-card.all.click&vd_source=1f9a658b3c0816438bea2f3933a0f8e9)

前端是网页的一部分，负责用户看到与交互的内容

网页是用户浏览过程中呈现的文档或页面，网页主要有html，css，js（JavaScript）构成，笔记的以下内容会分模块讲解

# 配置前端环境

1. 安装vscode [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/)

2. (可选项)，安装中文插件

   - 选择如图所示的功能，搜索Chinese，根据需要安装插件

   <img src="./.assets/image-20250529131755995.png" alt="image-20250529131755995" style="zoom: 50%;" />

   - 安装完成后会提示是否重启并更换语言，依照提示重启即可

3. 安装前端插件：

   - HTML CSS Support

     <img src="./.assets/image-20250529132030780.png" alt="image-20250529132030780" style="zoom:50%;" />

   - Live Server：用于在浏览器中实时预览当前变化（当前新版本可直接预览，该插件可省略）

     <img src="./.assets/image-20250529132153276.png" alt="image-20250529132153276" style="zoom:50%;" />

   - Auto Rename Tag：在修改html标签时，同步修改另一个标签

     <img src="./.assets/image-20250529132344534.png" alt="image-20250529132344534" style="zoom: 50%;" />

---

# 1. HTML

全称是Hypertext Markup Language(超文本标记语言）

用于定义网页的内容，给网页提供结构。

HTML通过一系列的标签(也称为元素)，来定义文本，图像，链接等。

## 1.1 HTML标签

HTML标签是由尖括号包围的关键字。有**双标签和单标签**

- **双标签：**成对出现，包括**开始标签和结束标签**(也称为双标签)，**内容**位于这两个标签之间

1. 段落标签 p

```html
<p>中间可以填写段落内容</p>
```

2. 标题 

```html
<title>文档大标题</title>
<h>一级标题</h>
```

3. 链接 a

```html
<a href="超链接">对该链接进行解释说明</a>
```

4. 编码格式

```html
<meta charset="UTF-8">
```

​    注意：

​	- utf-8 为常用格式，该格式可识别中文，若使用其他格式，可能会出现中文乱码的情况

- **单标签：**没有内容，和结束标签

1. input

```html
<input type = "text">
```

## 1.2 HTML的文件结构

（在vscode的html文件中，开头输入！，并且按tab，会自动按照格式补全内容）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```



- 在头部需要有一个标识信息，`<!DOCTYPE html>`,用来说明格式

- 开头`<html>`和结尾的`</html>`是一对html的标签对，即是该文档的根元素，用于记录文档的起点和终点

  

- `<head></head>`头部标签对，用来记录一些文档的信息，如标题`<title>`，编码格式`<meta>`，外部样式表等内容

  注意，<head> 里面的内容是**不会实际显示**在可浏览的网页中的!`<title>`除外，它会显示在标签页/窗口标题栏

  

- `<body></body>` 此处是网页会**实际显示**的内容

<img src="./.assets/image-20250529182719899.png" alt="image-20250529182719899" style="zoom: 67%;" />

```html
<!DOCTYPE html >
<html>
    <head>
        <title>学习</title>
        <meta charset = utf-8>
    </head>
    <body>
        <h>标题1</h>
        <p>段落1
            这是一个学习用的测试网站
            希望能正常打开~
        </p>
    </body>
</html>
```

右键代码，选择

<img src="./.assets/image-20250529183736736.png" alt="image-20250529183736736" style="zoom: 50%;" />

即可在浏览器中预览自己写的网页。此时在VsCode处保存，即可实时看到网页的变更，不需要反复打开网页

<img src="./.assets/image-20250529183420716.png" alt="image-20250529183420716" style="zoom:67%;" />

# 2. CSS

定义页面的样式和布局

# 3. js

用于添加交互性与动态功能作用