## CSS

### css基础语法

格式：选择器{属性1：值1；属性2：值2}

单位：px像素、%百分比

基本样式：width（宽）、height（高）、background-color（背景颜色）

### css样式的引入方式

内联样式：style属性（不建议写，好的代码希望html和CSS相互剥离开来哈）

内部样式：style标签（优势：可以复用代码）

外部样式：引入一个单独的css文件，name.css

通过link标签引入外部资源，rel属性指定资源跟页面的关系，href属性资源的地质                    通过@import方式引入外部样式**rel属性值**

|值|描述|
|:----:|:----|:----:|:----|
|slternate|文档的替代版本（比如打印页、翻译或镜像）|
|stylesheet|文档的外部样式表|
|start|集合中的第一个文档|
|next|集合中的下一个文档|
|prev|集合中的上一个文档|
|contents|文档的目录|
|index|文档的索引|
|glossary|在文档中使用的词汇的术语表（解释）|
|copyright|包含版权信息的文档|
|chapter|文档的章|
|section|文档的节|
|subsection|文档的小节|
|appendix|文档的附录|
|help|帮助文档|
|bookmark|相关文档|

### css中的颜色表示法

单词表示法：red   blue等

十六进制表示法rgb这里可以举例子：#ff00ff， 缩写 #f0f

三原色法：取值范围（0-255）

十六进制和0-255之间如何转化？ 有兴趣可以了解一下。

这里还有一个颜色的透明度，知识点

比如 #000000 表示纯黑色，用 rgb 表示 rgb(0,0,0)

那么 #00000050 表示带有透明度的黑色，具体的透明度可以这么看：

![图片](TODO)

### css背景样式

background-color：背景颜色

background-image：背景图片

url（背景地址，默认：会水平垂直铺满背景图）

​​​​​​​background-repeat：背景图片的平铺方式

repeat-x   x轴平铺

repeat-y   y轴平铺

no-repeat    都不平铺

​​​​​​​background-position：背景图片的位置

x、y：number（px、%）  单词

x：left、center、right

y：top、center、bottom

​​​​​​​background-attachment：背景图片随滚动条的移动方式

scroll：默认值（背景位置是按照当前元素进行偏移的）

fixed：固定（背景位置是按照浏览器进行偏移的）

### 背景图片时差滚动效果可以看看例子：[https://github.com/chokcoco/iCSS/issues/37](https://github.com/chokcoco/iCSS/issues/37?fileGuid=VMAPV7Z78gFGe9qg)（打开可能有点慢）

### css边框样式

border-style：边框样式

solid：实线

dashed：虚线

dotted：点线

border-width：边框大小（粗细）

border-color：边框颜色（透明颜色：transparent）

注：针对某一条边进行单独设置，例（border-left-style：solid）

### css文字样式

衬线体、非衬线体

font-family：字体类型（微软雅黑‘Microsoft YaHei’，宋体  SimSun，     Arial，‘Times New Roman’）注：单词组间有空格要加‘’，多个字体类型设置

使用自己的字体包

![图片](TODO)

网络字体格式

![图片](TODO)

字体图标：图标是一个字体包。比如下图（来源：[https://www.iviewui.com/components/icon](https://www.iviewui.com/components/icon?fileGuid=VMAPV7Z78gFGe9qg)）

![图片](TODO)

font-size：字体大小，一般用偶数

写法：number（px/rem/em）、单词（下图，不推荐使用）

|**属性取值**|**字体大小**|
|:----:|:----|:----:|:----|
|xx-small|最小|
|x-small|较小|
|small|小|
|medium|正常（默认值）|
|large|大|
|x-large|较大|
|xx-large|最大|

font-weight：字体粗细

两种模式：正常（normal）、加粗（bold）

写法：单词（normal、bold）、number（100  200 ..........  900，100-500都是正常     的，600-900都是加粗的）（平常 500 就有加粗效果了，你可以试试看）

font-style：字体样式

模式：正常（normal）、斜体（italic）

写法：单词（normal、italic）

注：oblique也是表示斜体的，用得少

一般font-style用的不多，可以直接用 em 斜体标签。

color：字体颜色

好玩的栗子：字体设置为透明色，背景图片设置为渐变的图片，背景图片clip裁剪设置为根据字体，就可以有一个渐变的字体啦！（实例代码：[https://codepen.io/four12344/pen/mdWQEYj](https://codepen.io/four12344/pen/mdWQEYj?fileGuid=VMAPV7Z78gFGe9qg)，可以自己看看哈）

![图片](TODO)

### css段落样式

text-decoration：文本装饰

下划线：underline

删除线：line-through

上划线：overline（有啥用？鼠标引入的动效吗？）

不添加任何样式：none

text-transform：文本大小写

小写：lowercase

大写：uppercase

只针对首字母大写：capitalize

text-indent：文本缩进

首行缩进

em单位：相对单位，1em永远都是跟字体大小相同

text-aline：文本对齐方式

对齐方式：left、right、center、justify（两端点对齐，为了美观常用）

line-height：定义行高

默认行高：不是固定值，而是根据当前字体的大小在不断地变化

取值：number（px）、scale（比例值，跟文字大小成比例）

letter-spacing：字间距

word-spacing：词间距（针对英文段落）

强制折行：针对英文和数字不自动折行问题

word-break：break-all；非常强烈的折行(记笔记的时候，可以加上你看到，你理解的内容，去解释别人模糊/晦涩难懂的定义。比如：英文单词会断开)

word-break：break-word；不是那么强烈的折行，会产生一些空白区域

### 


### css复合样式

复合的写法，是通过空格的方式实现的，写起来更方便

background： red url（） repeat ；

border：1px red solid

font：30px 宋体

注：background、border不需要关心属性顺序。font需要关心顺序，最少要有两个值size和family，顺序不能乱。尽量不要复合样式和单一样式混写，要混写的话，也必须先写复合样式再写单一样式，这样单一样式才不会被覆盖。


## css选择器

**ID选择器**：css写法（#name{}）、html写法（id=“name”）

注：1.id是唯一值，在一个页面中只能出现一次，出现多次是不符合规范的

2.命名的规范，由字母、下划线、中划线、字母（并且第一个不能是字母）组成

3.驼峰写法：searchButton（小驼峰，第一个单词小写第二个单词首字母大写）

SearchButton（大驼峰，单词首字母都是大写）

短线写法：search-small-button

下划线手法：search_small_button

**class选择器**：css写法（**.**name{}）、html写法（class=“name”）

注：1.class选择器是可以复用的

                 2.可以添加多个class样式，例：<div class="box content"\><div\>中间用空格

3.多个样式的时候，样式的优先级根据css决定，而不是class属性中的顺序

4.标签+类的写法，例：p.box{ }

**标签选择器**：css写法（name{}）、html写法（<name\>）

使用的场景：1.去掉某些标签的默认样式时

2.复杂的选择器中，如层次选择器

**群组选择器**：css写法（name，name，name）、html写法（<name\>）

通过逗号的方式，给多个不同的选择器添加不同的css样式，更方便代码的复用

通**配选择器：**css写法（*{}）

注：尽量避免使用通配选择器，因为会给所有标签添加样式，慎用。一般用在去掉所有标签的默认样式时。

**层次选择器：**

****后代：M N{ } 注：ul下所有的li，也包括li里的再打一个ul，li

父子：M\>N{ } 注：第一个ul下的li，不包括li里再打的一个ul，li

兄弟：M~N{ } 注：当前div标签**下面所有**的p标签

相邻：M+N{ } 注：当前div标签**下面相邻的一个**p标签

**属性选择器：**

|选择器|说明|
|:----:|:----|:----:|:----|
|M[attr]|M元素选择指定为attr属性的集合|
|M[attr=value]|M元素选择指定为attr属性和value值的集合（完全匹配）|
|M[attr*=value]|M元素选择指定为attr属性并且包含值为value的集合（部分匹配）|
|M[attr^=value]|M元素选择指定为attr属性并且起始值为value的集合（起始匹配）|
|M[attr$=value]|M元素选择指定为attr属性结束值为value的集合（结束匹配）|
|M[attr1][attr2]|M元素选择满足多个属性的集合（组合匹配）|

**伪类选择器：**

****：link        访问前的样式            （只能添加给a标签）

:  visited   访问过后的样式         （只能添加给a标签）

：hover    鼠标移入时的样式   （可以添加给所有的标签）

：active    鼠标按下时的样式   （可以添加给所有的标签）

一般网站只这样去设置：a{ }      a：hover{ }

：after 、：before      通过伪类的方式给元素添加一段文本内容使用content属性

：checked 、：disabled 、：focus      都是针对表单元素的

结构性伪类选择器

：nth-of-type（）     ：nth-child（）

括号里从1开始，1表示第一项，按顺序往下。n值，表示从零到无穷大

：first-of-type

：last-of-type

：only-of-type

## css继承（Inhenited）

文字相关的样式可以被继承

布局相关的样式默认是不能被继承（但是可以设置继承属性 inherit 值）

## css优先级

相同样式优先级：当设置相同样式时，后面的优先级高

内部样式与外部样式优先级：两者优先级相同，如果都设置了相同样式，那么后写的引入方式优先级高

单一样式优先级：style行间 \> id \> class \> tag（标签） \> * \> 继承

权重值：style行间（1000）、id（100）、class（10）、tag（1）

！important：提升优先级的方式，不能对继承的属性进行优先级的提升

标签+类的优先级\>单一类优先级

群组优先级：群组选择器与单一选择器的优先级相同，后写的优先级高

层次优先级

1.权重比较：

ul   li   .box   p   input（）        1 + 1 + 10 + 1 + 1

.hello   span   #elem（）          10 + 1 + 100

2.约分比较

ul   li~~.box~~~~p~~input（）—\>  ul   li   input

~~.hello~~~~span~~#elem（）   —\>  #elem

## css盒子模型

组成 ：content（内容）-\>padding（填充）-\>border（边框）-\>margin（外填充）

margin、padding：上下值、左右值

上、右、下、左

注：1.背景颜色会填充到margin以内的区域（默认行为）

2.文字在content区域添加

3.padding不能为负数，而margin可以为负数

box-sizing：盒尺寸，可以改变盒子模型的展示形态

默认值：content-box：width、height -\> content（只针对这一个）

border-box：width、height -\> content padding border （分给三家）

使用的场景：1.不用再去计算一些值

2.解决一些百分比的问题

盒子模型的一些问题

1.margin叠加问题：出现在上下margin同时存在的时候。会取上下中值较大的一项

解决方案：只给一个添加margin

2.margin传递问题：出现在嵌套的结构中，只是针对margin-top

解决方案：给父元素添加边框、margin换成padding

margin的自适应居中：auto

不设置content的现象：width、height不设置的时候，会自动去计算容器的大小

![图片](TODO)