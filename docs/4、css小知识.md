## css小知识

### 标签分类

按类型

block（块）：div、p、ul、li、h1 . . .

特点：1.独占一行

2.支持所有样式

3.不写宽的时候跟父元素的宽相同

4.所占区域是一个矩形

inline（内联）：span、a、em、strong、img . . .

特点：1.挨在一起的，不是独占一行

2.有些样式不支持，例如width、height、margin、padding

3.不写宽的时候，宽度由内容决定

4.所占的区域不一定是矩形

5.内联标签之间会有空隙，换行产生的

inline-block（）：input、select . . .

特点：1.挨在一起，但是支持宽高

注：布局一般用块标签，修饰文本一般用内联标签



按内容

Flow：流内容

Metadata：元数据

Sectioning：分区（划分区域）

Heading：标题

Phrasing：措辞（对文本的修饰）

Embedded：嵌入的

Interactive：互动的

![图片](TODO）

按显示

替换元素：浏览器根据元素的标签和属性，来决定元素显示的具体内容（img、input等）

非替换元素：将内容直接告诉浏览器，将其显示出来（div、h1、p等）

### 显示框类型

disliay：block、inline、inline-block、none

注：display：none（不占空间的隐藏） 与 visibility：hidden（占空间的隐藏）区别

### 标签嵌套规范

1.块能够嵌套内联

2.块标签不一定能嵌套块标签（p标签不能嵌套div）

3.内联标签不能嵌套块标签（a标签可以）

### 溢出隐藏

overflow

visible：默认值

hidden：隐藏多出部分

scroll：右侧和底部出现滚动条

auto：自动设置

x轴、y轴：overflow-x、overflow-y，针对两个轴设置

### 透明度与手势

opacity：0（透明）~0.5（半透明）~1（不透明）

注：占空间、所有的子元素也会受影响，用rgba来解决这一问题，rgba只针对背景

cursor鼠标手势：default（默认）、pointer、move、help等等

要实现自定义手势：1.准备图片：.cur、.ico格式

2.cursor：url（./img/cursor.ico），auto；

### 最大最小宽高

min-width（最小宽）、max-width（最大宽）

min-height（最小高度）、max-height（最大高度）

%单位：以父容器的大小进行换算

一个容器怎么适应屏幕的高？

容器加height100%；  body：100%；  html：100%

例：html，body { height：100% }

contrainer { height：100% }

### css默认样式

没有默认样式的：div、span

有默认样式的：

body -\> margin：8px

h1 -\> margin：上下21.440px

p -\> margin：上下16px

ul -\> margin：上下16px 、padding：左40px

. . . . .

### css reset（重置）

*{ margin：0；padding：0；}

ul{ list-style：none；}

a{ text-decoration：none；color：#666；}

img{ display：block；}

问题现象：图片跟容器底部有一些空隙，因为内联元素的对齐方式是按照文字的基线对齐的，而不是文字的底线。解决方式：vertical-aline：baseline（基线对齐）、bottom（底线），block也是可以的。

[https://blog.csdn.net/brain_bo/article/details/81560444](https://blog.csdn.net/brain_bo/article/details/81560444?fileGuid=VMAPV7Z78gFGe9qg)详细方法

### Photoshop

图片格式：jpg（颜色丰富）、png（可以透明）、gif（动图）、psd

快捷键：

ctrl+r：参考线 、alt+滚轮：放大缩小

### float浮动

* left
* right
* none

注：1.只会影响后面的元素

2.内容默认提升半层

3.默认宽根据内容决定

4.换行排列

5.主要给块元素添加，但也可以给内联元素添加

* 如何清除浮动

上下排列：clear属性，表示清除浮动，left、right、both

clear属性只会操作块标签，对内联不起作用

嵌套排列：

固定宽高：不适合做自适应

父元素浮动：会影响到后面的元素

overflow：hidden，如果子元素溢出，就会受到影响

display：inline-block，父容器会影响到后面的元素

设置空标签

after伪类  ：after{ content：' '；clear：both；display：block；}

### css定位

position特性

* static：默认
* relative：相对定位（left、top、right、bottom）

如果没有定位偏移量，对元素本身没影响

不使元素脱离文档流

不影响其他元素布局

对于当前元素自身进行偏移地

* absolute：绝对定位

使元素完全脱离文档流

使内联元素支持宽高（让内联具备块特性）

使块元素默认宽根据内容决定（让块具备内联特性）

如果祖先元素没有定位（相对、绝对、固定）的话，就相对于整个文档发生偏移；如果祖先元素有定位的话，就相对于祖先元素发生偏移

* fixed：固定定位

使元素完全脱离文档流

使内联元素支持宽高（让内联具备块特性）

使块元素默认宽根据内容决定（让块具备内联特性）

相对于整个浏览器窗口进行偏移，不受浏览器滚动条的影响

* sticky：黏性定位

在指定的位置，进行黏性操作

* z-indec定位层级

默认层级为0

嵌套时候的层级问题，（跟外面的比较）

### css添加省略号

width：必须有一个固定的宽

white-space：nowrap：不让内容折行

overflow：hidden：隐藏溢出内容

text-overflow：ellipsis：添加省略号

一行/多行文字显示不下时，使用省略

### css Sprite（css雪碧、css精灵）

是一种网页图片处理应用处理方式，它允许你将一个页面涉及到的所有零星图片都包含到一张大图中去加载

好处：1.可以减少图片的质量，网页的图片加载速度快

2.减少图片的请求次数，加快网页的打开

### css圆角

border-radius：给标签添加圆角

border-radius：20px / 40px   椭圆角

border-radius：20px（左上、右下） 40px（右上、左下）



---


## 小点

### 跳转锚点

* 方法一：#+id属性
* 方法二：#+name属性（注意name属性加给的是a标签）
### 特殊符号（解决冲突）

|**特殊字符**|**含义**|**特殊字符代码**|
|:----:|:----|:----:|:----|:----:|:----|
|    |空格符|&nbsp；|
|**©**|版权|&copy；|
|**®**|注册商标|&reg；|
|**<**|小于号|&lt；|
|**\>**|大于号|&gt；|
|**&**|和号|&amp；|
|**¥**|人命币|&yen；|
|**℃**|摄氏度|&deg；|


---


## 路径

### 相对路径

* **.**在路径中表示当前路径
* **..**在路径中表示上一级路径
### 绝对路径

